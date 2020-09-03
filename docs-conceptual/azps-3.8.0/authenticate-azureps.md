---
title: Accedere con Azure PowerShell
description: Come eseguire l'accesso con Azure PowerShell come utente, come entità servizio o con le identità gestite per le risorse di Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/18/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 10deb367456574a29b5b9c301e0e1a6b10d95c14
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241475"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="657f1-103">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="657f1-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="657f1-104">Azure PowerShell supporta diversi metodi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="657f1-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="657f1-105">Il modo più semplice per iniziare è con [Azure Cloud Shell](/azure/cloud-shell/overview), che esegue automaticamente l'accesso.</span><span class="sxs-lookup"><span data-stu-id="657f1-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="657f1-106">Con un'installazione locale è possibile accedere in modo interattivo tramite il browser.</span><span class="sxs-lookup"><span data-stu-id="657f1-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="657f1-107">Quando si scrivono script per l'automazione, l'approccio consigliato è quello di usare un'[entità servizio](create-azure-service-principal-azureps.md) con le autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="657f1-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="657f1-108">Quando si limitano il più possibile le autorizzazioni di accesso per il proprio caso d'uso, si contribuisce a proteggere le risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="657f1-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="657f1-109">Dopo l'accesso, i comandi vengono eseguiti sulla sottoscrizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="657f1-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="657f1-110">Per modificare la sottoscrizione attiva per una sessione, usare il cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="657f1-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="657f1-111">Per modificare la sottoscrizione predefinita usata per l'accesso con Azure PowerShell, usare [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="657f1-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="657f1-112">Le credenziali vengono condivise tra più sessioni di PowerShell, purché si rimanga connessi.</span><span class="sxs-lookup"><span data-stu-id="657f1-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="657f1-113">Per altre informazioni, vedere l'articolo relativo alle [Credenziali persistenti](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="657f1-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="657f1-114">Accedere in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="657f1-114">Sign in interactively</span></span>

<span data-ttu-id="657f1-115">Per accedere in modo interattivo, usare il cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="657f1-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="657f1-116">Quando si usa PowerShell versione 6 e successive, questo cmdlet presenta una stringa di token.</span><span class="sxs-lookup"><span data-stu-id="657f1-116">When run from PowerShell version 6 and higher, this cmdlet presents a token string.</span></span> <span data-ttu-id="657f1-117">Per eseguire l'accesso, copiare questa stringa e incollarla in [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in un web browser.</span><span class="sxs-lookup"><span data-stu-id="657f1-117">To sign in, copy this string and paste it into [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in a web browser.</span></span> <span data-ttu-id="657f1-118">La sessione di PowerShell verrà autenticata per connettersi ad Azure.</span><span class="sxs-lookup"><span data-stu-id="657f1-118">Your PowerShell session will be authenticated to connect to Azure.</span></span> <span data-ttu-id="657f1-119">È possibile specificare il parametro `UseDeviceAuthentication` per ricevere una stringa di token in Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="657f1-119">You can specify the `UseDeviceAuthentication` parameter to receive a token string on Windows PowerShell.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="657f1-120">L'autorizzazione tramite le credenziali nome utente/password è stata rimossa in Azure PowerShell a causa delle modifiche apportate nelle implementazioni delle autorizzazioni di Active Directory e per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="657f1-120">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="657f1-121">Se si usa l'autorizzazione tramite credenziali per motivi di automazione, [creare invece un'entità servizio](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="657f1-121">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="657f1-122">Usare il cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext) per archiviare l'ID tenant in una variabile da usare nelle prossime due sezioni di questo articolo.</span><span class="sxs-lookup"><span data-stu-id="657f1-122">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="657f1-123">Accedere con un'entità servizio <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="657f1-123">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="657f1-124">Le entità servizio sono account Azure non interattivi.</span><span class="sxs-lookup"><span data-stu-id="657f1-124">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="657f1-125">Come per gli altri account utente, le relative autorizzazioni vengono gestite con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="657f1-125">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="657f1-126">Concedendo a un'entità servizio solo le autorizzazioni necessarie, viene garantita la sicurezza degli script di automazione.</span><span class="sxs-lookup"><span data-stu-id="657f1-126">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="657f1-127">Per informazioni su come creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="657f1-127">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="657f1-128">Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="657f1-128">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="657f1-129">Saranno necessari anche l'ID applicazione dell'entità servizio, le credenziali di accesso e l'ID tenant associato all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="657f1-129">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="657f1-130">La modalità di accesso con un'entità servizio varia a seconda che sia stata configurata per l'autenticazione basata su password o basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="657f1-130">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="657f1-131">Autenticazione basata su password</span><span class="sxs-lookup"><span data-stu-id="657f1-131">Password-based authentication</span></span>

<span data-ttu-id="657f1-132">Creare un'entità servizio da usare negli esempi di questa sezione.</span><span class="sxs-lookup"><span data-stu-id="657f1-132">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="657f1-133">Per altre informazioni sulla creazione di entità servizio, vedere [Creare un'entità servizio di Azure con Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="657f1-133">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="657f1-134">Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="657f1-134">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="657f1-135">Questo cmdlet presenta una richiesta di nome utente e password.</span><span class="sxs-lookup"><span data-stu-id="657f1-135">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="657f1-136">Usare il valore di `applicationID` dell'entità servizio come nome utente e convertire il relativo `secret` in testo normale per la password.</span><span class="sxs-lookup"><span data-stu-id="657f1-136">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="657f1-137">Per gli scenari di automazione, è necessario creare le credenziali dal `applicationId` e dal `secret` dell'entità servizio:</span><span class="sxs-lookup"><span data-stu-id="657f1-137">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="657f1-138">Assicurarsi di adottare procedure valide per l'archiviazione delle password quando si automatizzano le connessioni dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="657f1-138">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="657f1-139">Autenticazione basata su certificati</span><span class="sxs-lookup"><span data-stu-id="657f1-139">Certificate-based authentication</span></span>

<span data-ttu-id="657f1-140">Per l'autenticazione basata su certificato, è necessario che Azure PowerShell sia in grado di recuperare informazioni da un archivio certificati locale in base a un'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="657f1-140">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="657f1-141">Quando si usa un'entità servizio invece di un'applicazione registrata, aggiungere l'argomento `-ServicePrincipal` e specificare l'ID applicazione dell'entità servizio come valore del parametro `-ApplicationId`.</span><span class="sxs-lookup"><span data-stu-id="657f1-141">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="657f1-142">In PowerShell 5.1 è possibile gestire e controllare l'archivio certificati con il modulo [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="657f1-142">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="657f1-143">Per PowerShell Core 6.x e versioni successive la procedura è più complicata.</span><span class="sxs-lookup"><span data-stu-id="657f1-143">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="657f1-144">Gli script seguenti mostrano come importare un certificato esistente nell'archivio certificati accessibile a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="657f1-144">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="657f1-145">Importare un certificato in PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="657f1-145">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="657f1-146">Importare un certificato in PowerShell Core 6.x e versioni successive</span><span class="sxs-lookup"><span data-stu-id="657f1-146">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="657f1-147">Accedere con un'identità gestita</span><span class="sxs-lookup"><span data-stu-id="657f1-147">Sign in using a managed identity</span></span>

<span data-ttu-id="657f1-148">Le identità gestite sono una funzionalità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="657f1-148">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="657f1-149">Le identità gestite sono entità servizio assegnate alle risorse che vengono eseguite in Azure.</span><span class="sxs-lookup"><span data-stu-id="657f1-149">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="657f1-150">È possibile usare l'entità servizio di un'identità gestita per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse.</span><span class="sxs-lookup"><span data-stu-id="657f1-150">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="657f1-151">Le identità gestite sono disponibili solo nelle risorse in esecuzione in un cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="657f1-151">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="657f1-152">Questo esempio si connette usando l'identità gestita dell'ambiente host.</span><span class="sxs-lookup"><span data-stu-id="657f1-152">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="657f1-153">Se, ad esempio, viene eseguito in una macchina virtuale con un'identità del servizio gestita assegnata, il codice può accedere usando tale identità assegnata.</span><span class="sxs-lookup"><span data-stu-id="657f1-153">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="657f1-154">Accedere con un tenant non predefinito o come Cloud Solution Provider (CSP)</span><span class="sxs-lookup"><span data-stu-id="657f1-154">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="657f1-155">Se l'account è associato a più di un tenant, l'accesso richiede di specificare il parametro `-Tenant` al momento della connessione.</span><span class="sxs-lookup"><span data-stu-id="657f1-155">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="657f1-156">Questo parametro funziona con qualsiasi metodo di accesso.</span><span class="sxs-lookup"><span data-stu-id="657f1-156">This parameter works with any sign-in method.</span></span> <span data-ttu-id="657f1-157">Quando si accede, il valore del parametro può essere l'ID oggetto di Azure del tenant (ID Tenant) o il nome di dominio completo del tenant.</span><span class="sxs-lookup"><span data-stu-id="657f1-157">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="657f1-158">Per gli utenti [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), il valore `-Tenant`**deve** essere un ID tenant.</span><span class="sxs-lookup"><span data-stu-id="657f1-158">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="657f1-159">Accedere a un altro cloud</span><span class="sxs-lookup"><span data-stu-id="657f1-159">Sign in to another Cloud</span></span>

<span data-ttu-id="657f1-160">I servizi cloud di Azure offrono ambienti conformi alle normative di gestione dei dati a livello di area.</span><span class="sxs-lookup"><span data-stu-id="657f1-160">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="657f1-161">Per gli account nel cloud di un'area, impostare l'ambiente al momento dell'accesso con l'argomento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="657f1-161">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="657f1-162">Questo parametro funziona con qualsiasi metodo di accesso.</span><span class="sxs-lookup"><span data-stu-id="657f1-162">This parameter works with any sign-in method.</span></span> <span data-ttu-id="657f1-163">Ad esempio, se l'account si trova nel cloud della Cina:</span><span class="sxs-lookup"><span data-stu-id="657f1-163">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="657f1-164">Il comando seguente recupera un elenco degli ambienti disponibili:</span><span class="sxs-lookup"><span data-stu-id="657f1-164">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
