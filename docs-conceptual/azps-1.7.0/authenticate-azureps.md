---
title: Accedere con Azure PowerShell
description: Come eseguire l'accesso con Azure PowerShell come utente, come entità servizio o con le identità gestite per le risorse di Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/20/2019
ms.openlocfilehash: 897bc20721305c03a0545bc236fa91292861ef1e
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/09/2019
ms.locfileid: "59363722"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="de9ce-103">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="de9ce-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="de9ce-104">Azure PowerShell supporta diversi metodi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="de9ce-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="de9ce-105">Il modo più semplice per iniziare è con [Azure Cloud Shell](/azure/cloud-shell/overview), che esegue automaticamente l'accesso.</span><span class="sxs-lookup"><span data-stu-id="de9ce-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="de9ce-106">Con un'installazione locale è possibile accedere in modo interattivo tramite il browser.</span><span class="sxs-lookup"><span data-stu-id="de9ce-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="de9ce-107">Quando si scrivono script per l'automazione, l'approccio consigliato è quello di usare un'[entità servizio](create-azure-service-principal-azureps.md) con le autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="de9ce-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="de9ce-108">Quando si limitano il più possibile le autorizzazioni di accesso per il proprio caso d'uso, si contribuisce a proteggere le risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="de9ce-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="de9ce-109">Dopo l'accesso, i comandi vengono eseguiti sulla sottoscrizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="de9ce-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="de9ce-110">Per modificare la sottoscrizione attiva per una sessione, usare il cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="de9ce-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="de9ce-111">Per modificare la sottoscrizione predefinita usata per l'accesso con Azure PowerShell, usare [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="de9ce-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="de9ce-112">Le credenziali vengono condivise tra più sessioni di PowerShell, purché si rimanga connessi.</span><span class="sxs-lookup"><span data-stu-id="de9ce-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="de9ce-113">Per altre informazioni, vedere l'articolo relativo alle [Credenziali persistenti](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="de9ce-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="de9ce-114">Accedere in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="de9ce-114">Sign in interactively</span></span>

<span data-ttu-id="de9ce-115">Per accedere in modo interattivo, usare il cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="de9ce-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="de9ce-116">Quando viene eseguito, questo cmdlet visualizzerà una stringa del token.</span><span class="sxs-lookup"><span data-stu-id="de9ce-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="de9ce-117">Per accedere, copiare questa stringa e incollarla in https://microsoft.com/devicelogin in un browser.</span><span class="sxs-lookup"><span data-stu-id="de9ce-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="de9ce-118">La sessione di PowerShell verrà autenticata per connettersi ad Azure.</span><span class="sxs-lookup"><span data-stu-id="de9ce-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="de9ce-119">L'autorizzazione tramite le credenziali nome utente/password è stata rimossa in Azure PowerShell a causa delle modifiche apportate nelle implementazioni delle autorizzazioni di Active Directory e per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="de9ce-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="de9ce-120">Se si usa l'autorizzazione tramite credenziali per motivi di automazione, [creare invece un'entità servizio](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="de9ce-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a><span data-ttu-id="de9ce-121">Accedere con un'entità servizio <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="de9ce-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="de9ce-122">Le entità servizio sono account Azure non interattivi.</span><span class="sxs-lookup"><span data-stu-id="de9ce-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="de9ce-123">Come per gli altri account utente, le relative autorizzazioni vengono gestite con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="de9ce-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="de9ce-124">Concedendo a un'entità servizio solo le autorizzazioni necessarie, viene garantita la sicurezza degli script di automazione.</span><span class="sxs-lookup"><span data-stu-id="de9ce-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="de9ce-125">Per informazioni su come creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="de9ce-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="de9ce-126">Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="de9ce-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="de9ce-127">Saranno necessari anche l'ID applicazione dell'entità servizio, le credenziali di accesso e l'ID tenant associato all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="de9ce-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="de9ce-128">La modalità di accesso con un'entità servizio varia a seconda che sia stata configurata per l'autenticazione basata su password o basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="de9ce-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="de9ce-129">Autenticazione basata su password</span><span class="sxs-lookup"><span data-stu-id="de9ce-129">Password-based authentication</span></span>

<span data-ttu-id="de9ce-130">Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="de9ce-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="de9ce-131">Questo cmdlet presenterà una richiesta di nome utente e password.</span><span class="sxs-lookup"><span data-stu-id="de9ce-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="de9ce-132">Usare l'ID entità servizio per il nome utente.</span><span class="sxs-lookup"><span data-stu-id="de9ce-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="de9ce-133">Per gli scenari di automazione, è necessario creare le credenziali da un nome utente e una stringa sicura:</span><span class="sxs-lookup"><span data-stu-id="de9ce-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="de9ce-134">Assicurarsi di adottare procedure valide per l'archiviazione delle password quando si automatizzano le connessioni dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="de9ce-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="de9ce-135">Autenticazione basata su certificati</span><span class="sxs-lookup"><span data-stu-id="de9ce-135">Certificate-based authentication</span></span>

<span data-ttu-id="de9ce-136">Per l'autenticazione basata su certificato, è necessario che Azure PowerShell sia in grado di recuperare informazioni da un archivio certificati locale in base a un'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="de9ce-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>
```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="de9ce-137">In PowerShell 5 l'archivio certificati può essere gestito e controllato con il modulo [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="de9ce-137">In PowerShell 5, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="de9ce-138">Per PowerShell 6, la procedura è più complicata.</span><span class="sxs-lookup"><span data-stu-id="de9ce-138">For PowerShell 6, the process is more complicated.</span></span> <span data-ttu-id="de9ce-139">Gli script seguenti mostrano come importare un certificato esistente nell'archivio certificati accessibile a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="de9ce-139">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-5"></a><span data-ttu-id="de9ce-140">Importare un certificato in PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="de9ce-140">Import a certificate in PowerShell 5</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-6"></a><span data-ttu-id="de9ce-141">Importare un certificato in PowerShell 6</span><span class="sxs-lookup"><span data-stu-id="de9ce-141">Import a certificate in PowerShell 6</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="de9ce-142">Accedere con un'identità gestita</span><span class="sxs-lookup"><span data-stu-id="de9ce-142">Sign in using a managed identity</span></span> 

<span data-ttu-id="de9ce-143">Le identità gestite sono una funzionalità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="de9ce-143">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="de9ce-144">Le identità gestite sono entità servizio assegnate alle risorse che vengono eseguite in Azure.</span><span class="sxs-lookup"><span data-stu-id="de9ce-144">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="de9ce-145">È possibile usare l'entità servizio di un'identità gestita per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse.</span><span class="sxs-lookup"><span data-stu-id="de9ce-145">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="de9ce-146">Le identità gestite sono disponibili solo nelle risorse in esecuzione in un cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="de9ce-146">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="de9ce-147">Per altre informazioni sulle identità gestite per le risorse di Azure, vedere [Come usare le identità gestite per le risorse di Azure in una macchina virtuale di Azure per acquisire un token di accesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="de9ce-147">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="de9ce-148">Accedere con un tenant non predefinito o come Cloud Solution Provider (CSP)</span><span class="sxs-lookup"><span data-stu-id="de9ce-148">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="de9ce-149">Se l'account è associato a più di un tenant, l'accesso richiede l'uso del parametro `-TenantId` per la connessione.</span><span class="sxs-lookup"><span data-stu-id="de9ce-149">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="de9ce-150">Questo parametro funziona con qualsiasi altro metodo di accesso.</span><span class="sxs-lookup"><span data-stu-id="de9ce-150">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="de9ce-151">Quando si accede, il valore del parametro può essere l'ID oggetto di Azure del tenant (ID Tenant) o il nome di dominio completo del tenant.</span><span class="sxs-lookup"><span data-stu-id="de9ce-151">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="de9ce-152">Per gli utenti [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), il valore `-TenantId` **deve** essere un ID tenant.</span><span class="sxs-lookup"><span data-stu-id="de9ce-152">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="de9ce-153">Accedere a un altro cloud</span><span class="sxs-lookup"><span data-stu-id="de9ce-153">Sign in to another Cloud</span></span>

<span data-ttu-id="de9ce-154">I servizi cloud di Azure offrono ambienti conformi alle normative di gestione dei dati a livello di area.</span><span class="sxs-lookup"><span data-stu-id="de9ce-154">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="de9ce-155">Per gli account nel cloud di un'area, impostare l'ambiente al momento dell'accesso con l'argomento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="de9ce-155">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="de9ce-156">Ad esempio, se l'account si trova nel cloud della Cina:</span><span class="sxs-lookup"><span data-stu-id="de9ce-156">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="de9ce-157">Il comando seguente recupera un elenco degli ambienti disponibili:</span><span class="sxs-lookup"><span data-stu-id="de9ce-157">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
