---
title: Accedere con Azure PowerShell
description: Come eseguire l'accesso con Azure PowerShell come utente, come entità servizio o con le identità gestite per le risorse di Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/18/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: bad681ddf6003ea7cd6f3ac90b2bff07ff277ec9
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409296"
---
# <a name="sign-in-with-azure-powershell"></a>Accedere con Azure PowerShell

Azure PowerShell supporta diversi metodi di autenticazione. Il modo più semplice per iniziare è con [Azure Cloud Shell](/azure/cloud-shell/overview), che esegue automaticamente l'accesso. Con un'installazione locale è possibile accedere in modo interattivo tramite il browser. Quando si scrivono script per l'automazione, l'approccio consigliato è quello di usare un'[entità servizio](create-azure-service-principal-azureps.md) con le autorizzazioni necessarie. Quando si limitano il più possibile le autorizzazioni di accesso per il proprio caso d'uso, si contribuisce a proteggere le risorse di Azure.

Dopo l'accesso, i comandi vengono eseguiti sulla sottoscrizione predefinita. Per modificare la sottoscrizione attiva per una sessione, usare il cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext). Per modificare la sottoscrizione predefinita usata per l'accesso con Azure PowerShell, usare [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).

> [!IMPORTANT]
> Le credenziali vengono condivise tra più sessioni di PowerShell, purché si rimanga connessi.
> Per altre informazioni, vedere l'articolo relativo alle [Credenziali persistenti](context-persistence.md).

## <a name="sign-in-interactively"></a>Accedere in modo interattivo

Per accedere in modo interattivo, usare il cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).

```azurepowershell-interactive
Connect-AzAccount
```

Quando si usa PowerShell versione 6 e successive, questo cmdlet presenta una stringa di token. Per eseguire l'accesso, copiare questa stringa e incollarla in [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in un web browser. La sessione di PowerShell verrà autenticata per connettersi ad Azure. È possibile specificare il parametro `UseDeviceAuthentication` per ricevere una stringa di token in Windows PowerShell.

> [!IMPORTANT]
> L'autorizzazione tramite le credenziali nome utente/password è stata rimossa in Azure PowerShell a causa delle modifiche apportate nelle implementazioni delle autorizzazioni di Active Directory e per motivi di sicurezza. Se si usa l'autorizzazione tramite credenziali per motivi di automazione, [creare invece un'entità servizio](create-azure-service-principal-azureps.md).

Usare il cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext) per archiviare l'ID tenant in una variabile da usare nelle prossime due sezioni di questo articolo.

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a>Accedere con un'entità servizio <a name="sp-signin"/>

Le entità servizio sono account Azure non interattivi. Come per gli altri account utente, le relative autorizzazioni vengono gestite con Azure Active Directory. Concedendo a un'entità servizio solo le autorizzazioni necessarie, viene garantita la sicurezza degli script di automazione.

Per informazioni su come creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).

Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzAccount`. Saranno necessari anche l'ID applicazione dell'entità servizio, le credenziali di accesso e l'ID tenant associato all'entità servizio. La modalità di accesso con un'entità servizio varia a seconda che sia stata configurata per l'autenticazione basata su password o basata su certificato.

### <a name="password-based-authentication"></a>Autenticazione basata su password

Creare un'entità servizio da usare negli esempi di questa sezione. Per altre informazioni sulla creazione di entità servizio, vedere [Creare un'entità servizio di Azure con Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Questo cmdlet presenta una richiesta di nome utente e password. Usare il valore di `applicationID` dell'entità servizio come nome utente e convertire il relativo `secret` in testo normale per la password.

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Per gli scenari di automazione, è necessario creare le credenziali dal `applicationId` e dal `secret` dell'entità servizio:

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Assicurarsi di adottare procedure valide per l'archiviazione delle password quando si automatizzano le connessioni dell'entità servizio.

### <a name="certificate-based-authentication"></a>Autenticazione basata su certificati

Per l'autenticazione basata su certificato, è necessario che Azure PowerShell sia in grado di recuperare informazioni da un archivio certificati locale in base a un'identificazione personale del certificato.

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

Quando si usa un'entità servizio invece di un'applicazione registrata, aggiungere l'argomento `-ServicePrincipal` e specificare l'ID applicazione dell'entità servizio come valore del parametro `-ApplicationId`.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

In PowerShell 5.1 è possibile gestire e controllare l'archivio certificati con il modulo [PKI](/powershell/module/pkiclient). Per PowerShell Core 6.x e versioni successive la procedura è più complicata. Gli script seguenti mostrano come importare un certificato esistente nell'archivio certificati accessibile a PowerShell.

#### <a name="import-a-certificate-in-powershell-51"></a>Importare un certificato in PowerShell 5.1

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a>Importare un certificato in PowerShell Core 6.x e versioni successive

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation)
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag)
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite)
$store.Add($Certificate)
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a>Accedere con un'identità gestita

Le identità gestite sono una funzionalità di Azure Active Directory. Le identità gestite sono entità servizio assegnate alle risorse che vengono eseguite in Azure. È possibile usare l'entità servizio di un'identità gestita per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse. Le identità gestite sono disponibili solo nelle risorse in esecuzione in un cloud di Azure.

Questo esempio si connette usando l'identità gestita dell'ambiente host. Se, ad esempio, viene eseguito in una macchina virtuale con un'identità del servizio gestita assegnata, il codice può accedere usando tale identità assegnata.

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Accedere con un tenant non predefinito o come Cloud Solution Provider (CSP)

Se l'account è associato a più di un tenant, l'accesso richiede di specificare il parametro `-Tenant` al momento della connessione. Questo parametro funziona con qualsiasi metodo di accesso. Quando si accede, il valore del parametro può essere l'ID oggetto di Azure del tenant (ID Tenant) o il nome di dominio completo del tenant.

Per gli utenti [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), il valore `-Tenant`**deve** essere un ID tenant.

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Accedere a un altro cloud

I servizi cloud di Azure offrono ambienti conformi alle normative di gestione dei dati a livello di area. Per gli account nel cloud di un'area, impostare l'ambiente al momento dell'accesso con l'argomento `-Environment`. Questo parametro funziona con qualsiasi metodo di accesso. Ad esempio, se l'account si trova nel cloud della Cina:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Il comando seguente recupera un elenco degli ambienti disponibili:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
