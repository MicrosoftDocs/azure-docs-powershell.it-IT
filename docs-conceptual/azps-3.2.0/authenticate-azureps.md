---
title: Accedere con Azure PowerShell
description: Come eseguire l'accesso con Azure PowerShell come utente, come entità servizio o con le identità gestite per le risorse di Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/04/2019
ms.openlocfilehash: 614cce77deb4390ea158a48ae2d48b7b983224f2
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182588"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="1caa5-103">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1caa5-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="1caa5-104">Azure PowerShell supporta diversi metodi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="1caa5-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="1caa5-105">Il modo più semplice per iniziare è con [Azure Cloud Shell](/azure/cloud-shell/overview), che esegue automaticamente l'accesso.</span><span class="sxs-lookup"><span data-stu-id="1caa5-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="1caa5-106">Con un'installazione locale è possibile accedere in modo interattivo tramite il browser.</span><span class="sxs-lookup"><span data-stu-id="1caa5-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="1caa5-107">Quando si scrivono script per l'automazione, l'approccio consigliato è quello di usare un'[entità servizio](create-azure-service-principal-azureps.md) con le autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="1caa5-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="1caa5-108">Quando si limitano il più possibile le autorizzazioni di accesso per il proprio caso d'uso, si contribuisce a proteggere le risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="1caa5-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="1caa5-109">Dopo l'accesso, i comandi vengono eseguiti sulla sottoscrizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1caa5-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="1caa5-110">Per modificare la sottoscrizione attiva per una sessione, usare il cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="1caa5-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="1caa5-111">Per modificare la sottoscrizione predefinita usata per l'accesso con Azure PowerShell, usare [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="1caa5-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="1caa5-112">Le credenziali vengono condivise tra più sessioni di PowerShell, purché si rimanga connessi.</span><span class="sxs-lookup"><span data-stu-id="1caa5-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="1caa5-113">Per altre informazioni, vedere l'articolo relativo alle [Credenziali persistenti](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1caa5-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="1caa5-114">Accedere in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="1caa5-114">Sign in interactively</span></span>

<span data-ttu-id="1caa5-115">Per accedere in modo interattivo, usare il cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="1caa5-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="1caa5-116">Quando viene eseguito, questo cmdlet visualizzerà una stringa del token.</span><span class="sxs-lookup"><span data-stu-id="1caa5-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="1caa5-117">Per accedere, copiare questa stringa e incollarla in https://microsoft.com/devicelogin in un browser.</span><span class="sxs-lookup"><span data-stu-id="1caa5-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="1caa5-118">La sessione di PowerShell verrà autenticata per connettersi ad Azure.</span><span class="sxs-lookup"><span data-stu-id="1caa5-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="1caa5-119">L'autorizzazione tramite le credenziali nome utente/password è stata rimossa in Azure PowerShell a causa delle modifiche apportate nelle implementazioni delle autorizzazioni di Active Directory e per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1caa5-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="1caa5-120">Se si usa l'autorizzazione tramite credenziali per motivi di automazione, [creare invece un'entità servizio](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1caa5-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a><span data-ttu-id="1caa5-121">Accedere con un'entità servizio <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="1caa5-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="1caa5-122">Le entità servizio sono account Azure non interattivi.</span><span class="sxs-lookup"><span data-stu-id="1caa5-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="1caa5-123">Come per gli altri account utente, le relative autorizzazioni vengono gestite con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1caa5-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="1caa5-124">Concedendo a un'entità servizio solo le autorizzazioni necessarie, viene garantita la sicurezza degli script di automazione.</span><span class="sxs-lookup"><span data-stu-id="1caa5-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="1caa5-125">Per informazioni su come creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1caa5-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="1caa5-126">Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="1caa5-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="1caa5-127">Saranno necessari anche l'ID applicazione dell'entità servizio, le credenziali di accesso e l'ID tenant associato all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="1caa5-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="1caa5-128">La modalità di accesso con un'entità servizio varia a seconda che sia stata configurata per l'autenticazione basata su password o basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="1caa5-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="1caa5-129">Autenticazione basata su password</span><span class="sxs-lookup"><span data-stu-id="1caa5-129">Password-based authentication</span></span>

<span data-ttu-id="1caa5-130">Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="1caa5-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="1caa5-131">Questo cmdlet presenterà una richiesta di nome utente e password.</span><span class="sxs-lookup"><span data-stu-id="1caa5-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="1caa5-132">Usare l'ID entità servizio per il nome utente.</span><span class="sxs-lookup"><span data-stu-id="1caa5-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="1caa5-133">Per gli scenari di automazione, è necessario creare le credenziali da un nome utente e una stringa sicura:</span><span class="sxs-lookup"><span data-stu-id="1caa5-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="1caa5-134">Assicurarsi di adottare procedure valide per l'archiviazione delle password quando si automatizzano le connessioni dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="1caa5-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="1caa5-135">Autenticazione basata su certificati</span><span class="sxs-lookup"><span data-stu-id="1caa5-135">Certificate-based authentication</span></span>

<span data-ttu-id="1caa5-136">Per l'autenticazione basata su certificato, è necessario che Azure PowerShell sia in grado di recuperare informazioni da un archivio certificati locale in base a un'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="1caa5-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="1caa5-137">Quando si usa un'entità servizio invece di un'applicazione registrata, aggiungere l'argomento `-ServicePrincipal` e specificare l'ID dell'entità servizio come valore del parametro `-ApplicationId`.</span><span class="sxs-lookup"><span data-stu-id="1caa5-137">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="1caa5-138">In PowerShell 5.1 è possibile gestire e controllare l'archivio certificati con il modulo [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="1caa5-138">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="1caa5-139">Per PowerShell Core 6.x e versioni successive la procedura è più complicata.</span><span class="sxs-lookup"><span data-stu-id="1caa5-139">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="1caa5-140">Gli script seguenti mostrano come importare un certificato esistente nell'archivio certificati accessibile a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1caa5-140">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="1caa5-141">Importare un certificato in PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="1caa5-141">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="1caa5-142">Importare un certificato in PowerShell Core 6.x e versioni successive</span><span class="sxs-lookup"><span data-stu-id="1caa5-142">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="1caa5-143">Accedere con un'identità gestita</span><span class="sxs-lookup"><span data-stu-id="1caa5-143">Sign in using a managed identity</span></span>

<span data-ttu-id="1caa5-144">Le identità gestite sono una funzionalità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1caa5-144">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="1caa5-145">Le identità gestite sono entità servizio assegnate alle risorse che vengono eseguite in Azure.</span><span class="sxs-lookup"><span data-stu-id="1caa5-145">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="1caa5-146">È possibile usare l'entità servizio di un'identità gestita per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse.</span><span class="sxs-lookup"><span data-stu-id="1caa5-146">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="1caa5-147">Le identità gestite sono disponibili solo nelle risorse in esecuzione in un cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="1caa5-147">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="1caa5-148">Questo comando si connette usando l'identità gestita dell'ambiente host.</span><span class="sxs-lookup"><span data-stu-id="1caa5-148">This command connects using the managed identity of the host environment.</span></span> <span data-ttu-id="1caa5-149">Se, ad esempio, viene eseguito in una macchina virtuale con un'identità del servizio gestita assegnata, il codice può accedere usando tale identità assegnata.</span><span class="sxs-lookup"><span data-stu-id="1caa5-149">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity 
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="1caa5-150">Accedere con un tenant non predefinito o come Cloud Solution Provider (CSP)</span><span class="sxs-lookup"><span data-stu-id="1caa5-150">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="1caa5-151">Se l'account è associato a più di un tenant, l'accesso richiede l'uso del parametro `-Tenant` per la connessione.</span><span class="sxs-lookup"><span data-stu-id="1caa5-151">If your account is associated with more than one tenant, sign-in requires the use of the `-Tenant` parameter when connecting.</span></span> <span data-ttu-id="1caa5-152">Questo parametro funziona con qualsiasi metodo di accesso.</span><span class="sxs-lookup"><span data-stu-id="1caa5-152">This parameter will work with any sign-in method.</span></span> <span data-ttu-id="1caa5-153">Quando si accede, il valore del parametro può essere l'ID oggetto di Azure del tenant (ID Tenant) o il nome di dominio completo del tenant.</span><span class="sxs-lookup"><span data-stu-id="1caa5-153">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="1caa5-154">Per gli utenti [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), il valore `-Tenant` **deve** essere un ID tenant.</span><span class="sxs-lookup"><span data-stu-id="1caa5-154">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="1caa5-155">Accedere a un altro cloud</span><span class="sxs-lookup"><span data-stu-id="1caa5-155">Sign in to another Cloud</span></span>

<span data-ttu-id="1caa5-156">I servizi cloud di Azure offrono ambienti conformi alle normative di gestione dei dati a livello di area.</span><span class="sxs-lookup"><span data-stu-id="1caa5-156">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="1caa5-157">Per gli account nel cloud di un'area, impostare l'ambiente al momento dell'accesso con l'argomento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="1caa5-157">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="1caa5-158">Questo parametro funziona con qualsiasi metodo di accesso.</span><span class="sxs-lookup"><span data-stu-id="1caa5-158">This parameter will work with any sign-in method.</span></span> <span data-ttu-id="1caa5-159">Ad esempio, se l'account si trova nel cloud della Cina:</span><span class="sxs-lookup"><span data-stu-id="1caa5-159">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="1caa5-160">Il comando seguente recupera un elenco degli ambienti disponibili:</span><span class="sxs-lookup"><span data-stu-id="1caa5-160">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
