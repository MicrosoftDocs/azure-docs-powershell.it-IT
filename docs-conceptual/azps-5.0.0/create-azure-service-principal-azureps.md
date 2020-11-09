---
title: Usare le entità servizio di Azure con Azure PowerShell
description: Informazioni su come creare e usare entità servizio con Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 20a58253e3f9435a9d33c700435f77fbb42df7ea
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/05/2020
ms.locfileid: "93365144"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Creare un'entità servizio di Azure con Azure PowerShell

Gli strumenti automatici che usano i servizi di Azure devono sempre avere autorizzazioni limitate. Invece di consentire alle applicazioni l'accesso come utenti con privilegi completi, Azure offre le identità servizio.

Un'entità servizio di Azure è un'identità creata per l'uso con applicazioni, servizi in hosting e strumenti automatici per l'accesso alle risorse di Azure. Questo accesso è limitato dai ruoli assegnati all'entità servizio e consente quindi di definire quali risorse siano accessibili e a quale livello. Per motivi di sicurezza è sempre consigliabile usare le identità servizio per gli strumenti automatici, invece di consentire loro di accedere con un'identità utente.

Questo articolo illustra i passaggi per la creazione, l'acquisizione di informazioni correlate e il ripristino di un'entità servizio con Azure PowerShell.

> [!WARNING]
> Quando si crea un'entità servizio con il comando [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal), l'output include credenziali che è necessario proteggere. Assicurarsi di non includere tali credenziali nel codice oppure archiviarle nel controllo del codice sorgente. In alternativa, è consigliabile usare [identità gestite](/azure/active-directory/managed-identities-azure-resources/overview) per evitare la necessità di usare le credenziali.
>
> Per impostazione predefinita, [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) assegna il ruolo di [Collaboratore](/azure/role-based-access-control/built-in-roles#contributor) all'entità servizio nell'ambito della sottoscrizione. Per ridurre il rischio di un'entità servizio compromessa, assegnare un ruolo più specifico e limitare l'ambito a una risorsa o a un gruppo di risorse. Per altre informazioni, vedere [Procedura per aggiungere un'assegnazione di ruolo](/azure/role-based-access-control/role-assignments-steps).

## <a name="create-a-service-principal"></a>Creare un'entità servizio

Creare un'entità servizio con il cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal). Quando si crea un'entità servizio, si sceglie il tipo di autenticazione per l'accesso che verrà usata dall'entità.

> [!NOTE]
> Se l'account in uso non è autorizzato a creare un'entità servizio, `New-AzADServicePrincipal` restituisce un messaggio di errore contenente "I privilegi non sono sufficienti per completare l'operazione".
> Per creare un'entità servizio, contattare l'amministratore di Azure Active Directory.

Sono disponibili due tipi di autenticazione per le entità servizio: autenticazione basata su password e autenticazione basata su certificato.

### <a name="password-based-authentication"></a>Autenticazione basata su password

> [!IMPORTANT]
> Il ruolo predefinito di un'entità servizio di autenticazione basata su password è **Collaboratore**. Questo ruolo ha autorizzazioni complete per la lettura e la scrittura in un account di Azure. Per informazioni sulla gestione delle assegnazioni di ruolo, vedere [Gestire i ruoli delle entità servizio](#manage-service-principal-roles).

Senza altri parametri di autenticazione, viene usata l'autenticazione basata su password e viene creata automaticamente una password casuale. Se si intende implementare l'autenticazione basata su password, si consiglia questo metodo.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

L'oggetto restituito contiene il membro `Secret`, ovvero un oggetto `SecureString` contenente la password generata. Assicurarsi di conservare questo valore in un posto sicuro per eseguire l'autenticazione con l'entità servizio. Il valore _non_ verrà visualizzato nell'output della console. Se si perde la password, [reimpostare le credenziali dell'entità servizio](#reset-credentials).

Il codice seguente consentirà di esportare il segreto:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

Per le password definite dall'utente, l'argomento `-PasswordCredential` accetta oggetti `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`. Questi oggetti devono avere valori validi di `StartDate` e `EndDate` e accettano `Password` in testo non crittografato. Quando si crea una password, assicurarsi di seguire le [regole e limitazioni per le password di Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).
Non usare password vulnerabili o già usate in precedenza.

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

L'oggetto restituito da `New-AzADServicePrincipal` contiene i membri `Id` e `DisplayName`, che possono essere entrambi usati per l'accesso con l'entità servizio.

> [!IMPORTANT]
> L'accesso con un'entità servizio richiede l'ID del tenant in cui è stata creata. Per ottenere il tenant attivo quando è stata creata l'entità servizio, eseguire il comando seguente _immediatamente dopo_ averla creata:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a>Autenticazione basata su certificati

> [!IMPORTANT]
> Quando viene creata, a un'entità servizio di autenticazione basata su certificato non è assegnato alcun ruolo predefinito. Per informazioni sulla gestione delle assegnazioni di ruolo, vedere [Gestire i ruoli delle entità servizio](#manage-service-principal-roles).

Le entità servizio che usano l'autenticazione basata su certificato vengono create con il parametro `-CertValue`. Questo parametro accetta una stringa ASCII con codifica Base64 del certificato pubblico, rappresentato da un file PEM oppure da un file CRT o CER con codifica di testo. Le codifiche binarie del certificato pubblico non sono supportate. Queste istruzioni presuppongono che sia già disponibile un certificato.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

È anche possibile usare il parametro `-KeyCredential`, che accetta oggetti `PSADKeyCredential`. Questi oggetti devono avere valori validi di `StartDate` e `EndDate`. Inoltre, il membro `CertValue` deve essere impostato su una stringa ASCII con codifica Base64 del certificato pubblico.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

L'oggetto restituito da `New-AzADServicePrincipal` contiene i membri `Id` e `DisplayName`, che possono essere entrambi usati per l'accesso con l'entità servizio. I client che accedono con l'entità servizio devono anche accedere alla chiave privata del certificato.

> [!IMPORTANT]
> L'accesso con un'entità servizio richiede l'ID del tenant in cui è stata creata. Per ottenere il tenant attivo quando è stata creata l'entità servizio, eseguire il comando seguente _immediatamente dopo_ averla creata:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a>Ottenere un'entità servizio esistente

L'elenco delle entità servizio per il tenant attivo può essere recuperato con [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal). Per impostazione predefinita, questo comando restituisce _tutte_ le entità servizio in un tenant. Per le organizzazioni di grandi dimensioni, la restituzione dei risultati potrebbe richiedere molto tempo. In alternativa, è consigliabile usare gli argomenti di filtro facoltativi sul lato server:

- `-DisplayNameBeginsWith` richiede entità di servizio che abbiano un _prefisso_ corrispondente al valore specificato. Il nome visualizzato di un'entità servizio è il valore impostato con `-DisplayName` durante la creazione.
- `-DisplayName` richiede una _corrispondenza esatta_ del nome di un'entità servizio.

## <a name="manage-service-principal-roles"></a>Gestire i ruoli delle entità servizio

Azure PowerShell include i cmdlet seguenti per gestire le assegnazioni dei ruoli:

- [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
- [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
- [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

Il ruolo predefinito di un'entità servizio di autenticazione basata su password è **Collaboratore**. Questo ruolo ha autorizzazioni complete per la lettura e la scrittura in un account di Azure. Il ruolo **Lettore** è più restrittivo e offre l'accesso in sola lettura. Per altre informazioni sul controllo degli accessi in base al ruolo e i ruoli, vedere [Controllo degli accessi in base al ruolo: ruoli predefiniti](/azure/active-directory/role-based-access-built-in-roles).

Questo esempio aggiunge il ruolo **Lettore** e rimuove il ruolo **Collaboratore** :

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> I cmdlet per l'assegnazione dei ruoli non accettano l'ID oggetto entità servizio. Accettano l'ID applicazione associato, generato al momento della creazione. Per ottenere l'ID applicazione per un'entità servizio, usare `Get-AzADServicePrincipal`.

> [!NOTE]
> Se l'account in uso non ha le autorizzazioni per assegnare un ruolo, viene visualizzato un messaggio di errore che segnala che l'account non è autorizzato a eseguire l'azione "Microsoft.Authorization/roleAssignments/write". Per gestire i ruoli, contattare l'amministratore di Azure Active Directory.

L'aggiunta di un ruolo _non_ limita le autorizzazioni assegnate in precedenza. Quando si limitano le autorizzazioni di un'entità servizio, il ruolo **Collaboratore** deve essere rimosso.

È possibile verificare le modifiche visualizzando l'elenco dei ruoli assegnati:

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a>Accedere con un'entità servizio

Testare le credenziali e le autorizzazioni della nuova entità servizio eseguendo l'accesso. Per accedere con un'entità servizio, è necessario il valore di `applicationId` associato e il tenant in cui è stata creata.

Per accedere con un'entità servizio usando una password:

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

Per l'autenticazione basata su certificato, è necessario che Azure PowerShell sia in grado di recuperare informazioni da un archivio certificati locale in base a un'identificazione personale del certificato.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

Per le istruzioni su come importare un certificato in un archivio certificati accessibile a PowerShell, vedere [Accedere con Azure PowerShell](authenticate-azureps.md#sp-signin)

## <a name="reset-credentials"></a>Reimpostare le credenziali

Se si dimenticano le credenziali per un'entità servizio, usare [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) per aggiungere credenziali nuove con una password casuale. Questo cmdlet non supporta le credenziali definite dall'utente per la reimpostazione della password.

> [!IMPORTANT]
> Prima di assegnare nuove credenziali, è consigliabile rimuovere quelle esistenti per evitare che vengano usate per l'accesso. A questo scopo, usare il cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a>Risoluzione dei problemi

Se viene visualizzato l'errore _"New-AzADServicePrincipal: Esiste già un altro oggetto con lo stesso valore per la proprietà identifierUris"_ , verificare che non sia già presente un'entità servizio con lo stesso nome.

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Se l'entità servizio esistente non è più necessaria, è possibile rimuoverla usando l'esempio seguente.

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Questo errore può verificarsi anche quando in precedenza è stata creata un'entità servizio per un'applicazione Azure Active Directory. Se si rimuove l'entità servizio, l'applicazione rimane disponibile. Questa applicazione impedisce di creare un'altra entità servizio con lo stesso nome.

È possibile usare l'esempio seguente per verificare che non esista un'applicazione Azure Active Directory con lo stesso nome:

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

Se esiste un'applicazione con lo stesso nome ma non è più necessaria, è possibile rimuoverla usando l'esempio seguente.

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

In caso contrario, scegliere un nome alternativo per la nuova entità servizio da creare.
