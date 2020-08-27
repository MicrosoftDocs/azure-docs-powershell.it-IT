---
title: Accedere con Azure PowerShell
description: Come eseguire l'accesso con Azure PowerShell come utente, come entità servizio o con le identità gestite per le risorse di Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 7/7/2020
ms.openlocfilehash: 7ac723202ca9e81c8ef4cba5e844d46b98ba4b67
ms.sourcegitcommit: b94a3f00c147144b0ef7f8cf8d0f151e04674b89
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/25/2020
ms.locfileid: "88821628"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="6ecbf-103">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6ecbf-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="6ecbf-104">Azure PowerShell supporta diversi metodi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="6ecbf-105">Il modo più semplice per iniziare è con [Azure Cloud Shell](/azure/cloud-shell/overview), che esegue automaticamente l'accesso.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="6ecbf-106">Con un'installazione locale è possibile accedere in modo interattivo tramite il browser.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="6ecbf-107">Quando si scrivono script per l'automazione, l'approccio consigliato è quello di usare un'[entità servizio](create-azure-service-principal-azureps.md) con le autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="6ecbf-108">Quando si limitano il più possibile le autorizzazioni di accesso per il proprio caso d'uso, si contribuisce a proteggere le risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="6ecbf-109">Inizialmente viene effettuato l'eccesso alla prima sottoscrizione restituita da Azure, se si ha accesso a più sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-109">Initially, you're signed into the first subscription Azure returns if you have access to more than one subscription.</span></span> <span data-ttu-id="6ecbf-110">Per impostazione predefinita, i comandi vengono eseguiti su questa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-110">Commands are run against this subscription by default.</span></span> <span data-ttu-id="6ecbf-111">Per modificare la sottoscrizione attiva per una sessione, usare il cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="6ecbf-111">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="6ecbf-112">Per cambiare la sottoscrizione attiva e renderla permanente tra sessioni nello stesso sistema, usare il cmdlet [Select-AzContext](/powershell/module/az.accounts/select-azcontext).</span><span class="sxs-lookup"><span data-stu-id="6ecbf-112">To change your active subscription and have it persist between sessions on the same system, use the [Select-AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ecbf-113">Le credenziali vengono condivise tra più sessioni di PowerShell, purché si rimanga connessi.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-113">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="6ecbf-114">Per altre informazioni, vedere l'articolo relativo alle [Credenziali persistenti](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="6ecbf-114">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="6ecbf-115">Accedere in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="6ecbf-115">Sign in interactively</span></span>

<span data-ttu-id="6ecbf-116">Per accedere in modo interattivo, usare il cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="6ecbf-116">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="6ecbf-117">Quando si usa PowerShell versione 6 e successive, questo cmdlet presenta una stringa di token.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-117">When run from PowerShell version 6 and higher, this cmdlet presents a token string.</span></span> <span data-ttu-id="6ecbf-118">Per eseguire l'accesso, copiare questa stringa e incollarla in [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in un web browser.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-118">To sign in, copy this string and paste it into [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in a web browser.</span></span> <span data-ttu-id="6ecbf-119">La sessione di PowerShell verrà autenticata per connettersi ad Azure.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-119">Your PowerShell session will be authenticated to connect to Azure.</span></span> <span data-ttu-id="6ecbf-120">È possibile specificare il parametro `UseDeviceAuthentication` per ricevere una stringa di token in Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-120">You can specify the `UseDeviceAuthentication` parameter to receive a token string on Windows PowerShell.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ecbf-121">L'autorizzazione tramite le credenziali nome utente/password è stata rimossa in Azure PowerShell a causa delle modifiche apportate nelle implementazioni delle autorizzazioni di Active Directory e per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-121">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="6ecbf-122">Se si usa l'autorizzazione tramite credenziali per motivi di automazione, [creare invece un'entità servizio](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="6ecbf-122">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="6ecbf-123">Usare il cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext) per archiviare l'ID tenant in una variabile da usare nelle prossime due sezioni di questo articolo.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-123">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="6ecbf-124">Accedere con un'entità servizio <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="6ecbf-124">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="6ecbf-125">Le entità servizio sono account Azure non interattivi.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="6ecbf-126">Come per gli altri account utente, le relative autorizzazioni vengono gestite con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="6ecbf-127">Concedendo a un'entità servizio solo le autorizzazioni necessarie, viene garantita la sicurezza degli script di automazione.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="6ecbf-128">Per informazioni su come creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="6ecbf-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="6ecbf-129">Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="6ecbf-130">Saranno necessari anche l'ID applicazione dell'entità servizio, le credenziali di accesso e l'ID tenant associato all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="6ecbf-131">La modalità di accesso con un'entità servizio varia a seconda che sia stata configurata per l'autenticazione basata su password o basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-131">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="6ecbf-132">Autenticazione basata su password</span><span class="sxs-lookup"><span data-stu-id="6ecbf-132">Password-based authentication</span></span>

<span data-ttu-id="6ecbf-133">Creare un'entità servizio da usare negli esempi di questa sezione.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-133">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="6ecbf-134">Per altre informazioni sulla creazione di entità servizio, vedere [Creare un'entità servizio di Azure con Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="6ecbf-134">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="6ecbf-135">Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="6ecbf-135">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="6ecbf-136">Questo cmdlet presenta una richiesta di nome utente e password.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-136">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="6ecbf-137">Usare il valore di `applicationID` dell'entità servizio come nome utente e convertire il relativo `secret` in testo normale per la password.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-137">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="6ecbf-138">Per gli scenari di automazione, è necessario creare le credenziali dal `applicationId` e dal `secret` dell'entità servizio:</span><span class="sxs-lookup"><span data-stu-id="6ecbf-138">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="6ecbf-139">Assicurarsi di adottare procedure valide per l'archiviazione delle password quando si automatizzano le connessioni dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-139">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="6ecbf-140">Autenticazione basata su certificati</span><span class="sxs-lookup"><span data-stu-id="6ecbf-140">Certificate-based authentication</span></span>

<span data-ttu-id="6ecbf-141">Per l'autenticazione basata su certificato, è necessario che Azure PowerShell sia in grado di recuperare informazioni da un archivio certificati locale in base a un'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-141">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="6ecbf-142">Quando si usa un'entità servizio invece di un'applicazione registrata, aggiungere l'argomento `-ServicePrincipal` e specificare l'ID applicazione dell'entità servizio come valore del parametro `-ApplicationId`.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-142">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="6ecbf-143">In PowerShell 5.1 è possibile gestire e controllare l'archivio certificati con il modulo [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="6ecbf-143">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="6ecbf-144">Per PowerShell Core 6.x e versioni successive la procedura è più complicata.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-144">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="6ecbf-145">Gli script seguenti mostrano come importare un certificato esistente nell'archivio certificati accessibile a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-145">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="6ecbf-146">Importare un certificato in PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="6ecbf-146">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="6ecbf-147">Importare un certificato in PowerShell Core 6.x e versioni successive</span><span class="sxs-lookup"><span data-stu-id="6ecbf-147">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="6ecbf-148">Accedere con un'identità gestita</span><span class="sxs-lookup"><span data-stu-id="6ecbf-148">Sign in using a managed identity</span></span>

<span data-ttu-id="6ecbf-149">Le identità gestite sono una funzionalità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-149">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="6ecbf-150">Le identità gestite sono entità servizio assegnate alle risorse che vengono eseguite in Azure.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-150">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="6ecbf-151">È possibile usare l'entità servizio di un'identità gestita per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-151">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="6ecbf-152">Le identità gestite sono disponibili solo nelle risorse in esecuzione in un cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-152">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="6ecbf-153">Questo esempio si connette usando l'identità gestita dell'ambiente host.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-153">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="6ecbf-154">Se, ad esempio, viene eseguito in una macchina virtuale con un'identità del servizio gestita assegnata, il codice può accedere usando tale identità assegnata.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-154">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="6ecbf-155">Accedere con un tenant non predefinito o come Cloud Solution Provider (CSP)</span><span class="sxs-lookup"><span data-stu-id="6ecbf-155">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="6ecbf-156">Se l'account è associato a più di un tenant, l'accesso richiede di specificare il parametro `-Tenant` al momento della connessione.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-156">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="6ecbf-157">Questo parametro funziona con qualsiasi metodo di accesso.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-157">This parameter works with any sign-in method.</span></span> <span data-ttu-id="6ecbf-158">Quando si accede, il valore del parametro può essere l'ID oggetto di Azure del tenant (ID Tenant) o il nome di dominio completo del tenant.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-158">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="6ecbf-159">Per gli utenti [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), il valore `-Tenant`**deve** essere un ID tenant.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-159">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="6ecbf-160">Accedere a un altro cloud</span><span class="sxs-lookup"><span data-stu-id="6ecbf-160">Sign in to another Cloud</span></span>

<span data-ttu-id="6ecbf-161">I servizi cloud di Azure offrono ambienti conformi alle normative di gestione dei dati a livello di area.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-161">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="6ecbf-162">Per gli account nel cloud di un'area, impostare l'ambiente al momento dell'accesso con l'argomento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-162">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="6ecbf-163">Questo parametro funziona con qualsiasi metodo di accesso.</span><span class="sxs-lookup"><span data-stu-id="6ecbf-163">This parameter works with any sign-in method.</span></span> <span data-ttu-id="6ecbf-164">Ad esempio, se l'account si trova nel cloud della Cina:</span><span class="sxs-lookup"><span data-stu-id="6ecbf-164">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="6ecbf-165">Il comando seguente recupera un elenco degli ambienti disponibili:</span><span class="sxs-lookup"><span data-stu-id="6ecbf-165">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
