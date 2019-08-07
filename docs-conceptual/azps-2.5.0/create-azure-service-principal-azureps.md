---
title: Usare le entità servizio di Azure con Azure PowerShell
description: Informazioni su come creare e usare entità servizio con Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: 4c47d2bac2c63f13ac0ebbccda3e2eed12cd658f
ms.sourcegitcommit: a261efc84dedfd829c0613cf62f8fcf3aa62adb8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2019
ms.locfileid: "68807398"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Creare un'entità servizio di Azure con Azure PowerShell

Gli strumenti automatici che usano i servizi di Azure devono sempre avere autorizzazioni limitate. Invece di consentire alle applicazioni l'accesso come utenti con privilegi completi, Azure offre le identità servizio.

Un'entità servizio di Azure è un'identità creata per l'uso con applicazioni, servizi in hosting e strumenti automatici per l'accesso alle risorse di Azure. Questo accesso è limitato dai ruoli assegnati all'entità servizio e consente quindi di definire quali risorse siano accessibili e a quale livello. Per motivi di sicurezza è sempre consigliabile usare le identità servizio per gli strumenti automatici, invece di consentire loro di accedere con un'identità utente.

Questo articolo illustra i passaggi per la creazione, l'acquisizione di informazioni correlate e il ripristino di un'entità servizio con Azure PowerShell.

## <a name="create-a-service-principal"></a>Creare un'entità servizio

Creare un'entità servizio con il cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal). Quando si crea un'entità servizio, si sceglie il tipo di autenticazione per l'accesso che verrà usata dall'entità.

> [!NOTE]
>
> Se l'account in uso non è autorizzato a creare un'entità servizio, `New-AzADServicePrincipal` restituirà un messaggio di errore contenente "I privilegi non sono sufficienti per completare l'operazione". Per creare un'entità servizio, contattare l'amministratore di Azure Active Directory.

Sono disponibili due tipi di autenticazione per le entità servizio: autenticazione basata su password e autenticazione basata su certificato.

### <a name="password-based-authentication"></a>Autenticazione basata su password

Senza altri parametri di autenticazione, viene usata l'autenticazione basata su password e viene creata automaticamente una password casuale. Se si intende implementare l'autenticazione basata su password, si consiglia questo metodo.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

L'oggetto restituito contiene il membro `Secret`, ovvero un oggetto `SecureString` contenente la password generata. Assicurarsi di conservare questo valore in un posto sicuro per eseguire l'autenticazione con l'entità servizio. Il valore __non__ verrà visualizzato nell'output della console. Se si perde la password, [reimpostare le credenziali dell'entità servizio](#reset-credentials).

Il codice seguente consentirà di esportare il segreto:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

Per le password definite dall'utente, l'argomento `-PasswordCredential` accetta oggetti `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`. Questi oggetti devono avere valori validi di `StartDate` e `EndDate` e accettano `Password` in testo non crittografato. Quando si crea una password, assicurarsi di seguire le [regole e limitazioni per le password di Azure Active Directory](/azure/active-directory/active-directory-passwords-policy). Non usare password vulnerabili o già usate in precedenza.

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

L'oggetto restituito da `New-AzADServicePrincipal` contiene i membri `Id` e `DisplayName`, che possono essere entrambi usati per l'accesso con l'entità servizio.

> [!IMPORTANT]
>
> L'accesso con un'entità servizio richiede l'ID del tenant in cui è stata creata. Per ottenere il tenant attivo quando è stata creata l'entità servizio, eseguire il comando seguente __immediatamente dopo__ averla creata:
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a>Autenticazione basata su certificati

Le entità servizio che usano l'autenticazione basata su certificato vengono create con il parametro `-CertValue`. Questo parametro accetta una stringa ASCII con codifica Base64 del certificato pubblico, rappresentato da un file PEM oppure da un file CRT o CER con codifica di testo. Le codifiche binarie del certificato pubblico non sono supportate. Queste istruzioni presuppongono che sia già disponibile un certificato.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

È anche possibile usare il parametro `-KeyCredential`, che accetta oggetti `PSADKeyCredential`. Questi oggetti devono avere valori validi di `StartDate` e `EndDate`. Inoltre, il membro `CertValue` deve essere impostato su una stringa ASCII con codifica Base64 del certificato pubblico.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

L'oggetto restituito da `New-AzADServicePrincipal` contiene i membri `Id` e `DisplayName`, che possono essere entrambi usati per l'accesso con l'entità servizio. I client che accedono con l'entità servizio devono anche accedere alla chiave privata del certificato.

> [!IMPORTANT]
>
> L'accesso con un'entità servizio richiede l'ID del tenant in cui è stata creata. Per ottenere il tenant attivo quando è stata creata l'entità servizio, eseguire il comando seguente __immediatamente dopo__ averla creata:
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a>Ottenere un'entità servizio esistente

L'elenco delle entità servizio per il tenant attualmente attivo può essere recuperato con [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal). Per impostazione predefinita, questo comando restituisce __tutte__ le entità servizio di un tenant, quindi per le organizzazioni più grandi la restituzione di risultati può richiedere tempi lunghi. In alternativa, è consigliabile usare gli argomenti di filtro facoltativi sul lato server:

* `-DisplayNameBeginsWith` richiede entità di servizio che abbiano un _prefisso_ corrispondente al valore specificato. Il nome visualizzato di un'entità servizio è il valore impostato con `-DisplayName` durante la creazione.
* `-DisplayName` richiede una _corrispondenza esatta_ del nome di un'entità servizio.

## <a name="manage-service-principal-roles"></a>Gestire i ruoli delle entità servizio

Azure PowerShell include i cmdlet seguenti per gestire le assegnazioni dei ruoli:

* [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
* [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
* [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

Il ruolo predefinito per un'entità servizio è quello **Collaboratore**. Questo ruolo ha autorizzazioni complete per la lettura e la scrittura in un account di Azure. Il ruolo **Lettore** è più restrittivo e offre l'accesso in sola lettura.  Per altre informazioni sul controllo degli accessi in base al ruolo e i ruoli, vedere [Controllo degli accessi in base al ruolo: ruoli predefiniti](/azure/active-directory/role-based-access-built-in-roles).

Questo esempio aggiunge il ruolo **Lettore** e rimuove il ruolo **Collaboratore**:

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> I cmdlet per l'assegnazione dei ruoli non accettano l'ID oggetto entità servizio. Accettano l'ID applicazione associato, generato al momento della creazione. Per ottenere l'ID applicazione per un'entità servizio, usare `Get-AzADServicePrincipal`.

> [!NOTE]
> Se l'account non ha le autorizzazioni per assegnare un ruolo, verrà visualizzato un messaggio di errore che segnala che l'account non è autorizzato a eseguire l'azione 'Microsoft.Authorization/roleAssignments/write'. Per gestire i ruoli, contattare l'amministratore di Azure Active Directory.

L'aggiunta di un ruolo _non_ limita le autorizzazioni assegnate in precedenza. Quando si limitano le autorizzazioni di un'entità servizio, il ruolo __Collaboratore__ deve essere rimosso.

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
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

Per le istruzioni su come importare un certificato in un archivio certificati accessibile a PowerShell, vedere [Accedere con Azure PowerShell](authenticate-azureps.md#sp-signin)

## <a name="reset-credentials"></a>Reimpostare le credenziali

Se si dimenticano le credenziali per un'entità di servizio, usare [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) per aggiungerne una nuova. Questo cmdlet accetta gli stessi argomenti e tipi di credenziali di `New-AzADServicePrincipal`. Senza argomenti di credenziali, viene creato un nuovo oggetto `PasswordCredential` con una password casuale.

> [!IMPORTANT]
> Prima di assegnare nuove credenziali, è consigliabile rimuovere quelle esistenti per evitare che vengano usate per l'accesso. A questo scopo, usare il cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
