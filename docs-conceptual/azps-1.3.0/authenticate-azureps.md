---
title: Accedere con Azure PowerShell
description: Come eseguire l'accesso con Azure PowerShell come utente, come entità servizio o con le identità gestite per le risorse di Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 80c59a10666c6e3a01e6c33716fce40094fb14be
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2019
ms.locfileid: "56144871"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="38077-103">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="38077-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="38077-104">Azure PowerShell supporta diversi metodi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="38077-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="38077-105">Il modo più semplice per iniziare è con [Azure Cloud Shell](/azure/cloud-shell/overview), che esegue automaticamente l'accesso.</span><span class="sxs-lookup"><span data-stu-id="38077-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="38077-106">Con un'installazione locale è possibile accedere in modo interattivo tramite il browser.</span><span class="sxs-lookup"><span data-stu-id="38077-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="38077-107">Quando si scrivono script per l'automazione, l'approccio consigliato è quello di usare un'[entità servizio](create-azure-service-principal-azureps.md) con le autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="38077-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="38077-108">Quando si limitano il più possibile le autorizzazioni di accesso per il proprio caso d'uso, si contribuisce a proteggere le risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="38077-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="38077-109">Dopo l'accesso, i comandi vengono eseguiti sulla sottoscrizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="38077-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="38077-110">Per modificare la sottoscrizione attiva per una sessione, usare il cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="38077-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="38077-111">Per modificare la sottoscrizione predefinita usata per l'accesso con Azure PowerShell, usare [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="38077-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="38077-112">Le credenziali vengono condivise tra più sessioni di PowerShell, purché si rimanga connessi.</span><span class="sxs-lookup"><span data-stu-id="38077-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="38077-113">Per altre informazioni, vedere l'articolo relativo alle [Credenziali persistenti](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="38077-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="38077-114">Accedere in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="38077-114">Sign in interactively</span></span>

<span data-ttu-id="38077-115">Per accedere in modo interattivo, usare il cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="38077-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="38077-116">Quando viene eseguito, questo cmdlet visualizzerà una stringa del token.</span><span class="sxs-lookup"><span data-stu-id="38077-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="38077-117">Per accedere, copiare questa stringa e incollarla in https://microsoft.com/devicelogin in un browser.</span><span class="sxs-lookup"><span data-stu-id="38077-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="38077-118">La sessione di PowerShell verrà autenticata per connettersi ad Azure.</span><span class="sxs-lookup"><span data-stu-id="38077-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

## <a name="sign-in-with-credentials"></a><span data-ttu-id="38077-119">Accedere con le credenziali</span><span class="sxs-lookup"><span data-stu-id="38077-119">Sign in with credentials</span></span>

<span data-ttu-id="38077-120">È anche possibile accedere con un oggetto `PSCredential` autorizzato a connettersi ad Azure.</span><span class="sxs-lookup"><span data-stu-id="38077-120">You can also sign in with a `PSCredential` object authorized to connect to Azure.</span></span>
<span data-ttu-id="38077-121">Il modo più semplice per ottenere un oggetto credenziali è con il cmdlet [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential).</span><span class="sxs-lookup"><span data-stu-id="38077-121">The easiest way to get a credential object is with the [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) cmdlet.</span></span> <span data-ttu-id="38077-122">Quando viene eseguito, questo cmdlet richiederà una coppia di credenziali nome utente/password.</span><span class="sxs-lookup"><span data-stu-id="38077-122">When run, this cmdlet will prompt you for a username/password credential pair.</span></span>

> [!Note]
> <span data-ttu-id="38077-123">Questo approccio non funziona con gli account Microsoft o gli account in cui è abilitata l'autenticazione a due fattori.</span><span class="sxs-lookup"><span data-stu-id="38077-123">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="38077-124">Accedere con un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="38077-124">Sign in with a service principal</span></span>

<span data-ttu-id="38077-125">Le entità servizio sono account Azure non interattivi.</span><span class="sxs-lookup"><span data-stu-id="38077-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="38077-126">Come per gli altri account utente, le relative autorizzazioni vengono gestite con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="38077-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="38077-127">Concedendo a un'entità servizio solo le autorizzazioni necessarie, viene garantita la sicurezza degli script di automazione.</span><span class="sxs-lookup"><span data-stu-id="38077-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="38077-128">Per informazioni su come creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="38077-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="38077-129">Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="38077-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="38077-130">Saranno necessari anche l'ID applicazione dell'entità servizio, le credenziali di accesso e l'ID tenant associato all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="38077-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="38077-131">Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="38077-131">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="38077-132">Questo cmdlet visualizzerà la richiesta di inserimento dell'ID utente e della password dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="38077-132">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="38077-133">Accedere con un'identità gestita</span><span class="sxs-lookup"><span data-stu-id="38077-133">Sign in using a managed identity</span></span> 

<span data-ttu-id="38077-134">Le identità gestite sono una funzionalità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="38077-134">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="38077-135">Le identità gestite sono entità servizio assegnate alle risorse che vengono eseguite in Azure.</span><span class="sxs-lookup"><span data-stu-id="38077-135">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="38077-136">È possibile usare l'entità servizio di un'identità gestita per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse.</span><span class="sxs-lookup"><span data-stu-id="38077-136">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="38077-137">Le identità gestite sono disponibili solo nelle risorse in esecuzione in un cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="38077-137">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="38077-138">Per altre informazioni sulle identità gestite per le risorse di Azure, vedere [Come usare le identità gestite per le risorse di Azure in una macchina virtuale di Azure per acquisire un token di accesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="38077-138">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="38077-139">Accedere con un tenant non predefinito o come Cloud Solution Provider (CSP)</span><span class="sxs-lookup"><span data-stu-id="38077-139">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="38077-140">Se l'account è associato a più di un tenant, l'accesso richiede l'uso del parametro `-TenantId` per la connessione.</span><span class="sxs-lookup"><span data-stu-id="38077-140">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="38077-141">Questo parametro funziona con qualsiasi altro metodo di accesso.</span><span class="sxs-lookup"><span data-stu-id="38077-141">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="38077-142">Quando si accede, il valore del parametro può essere l'ID oggetto di Azure del tenant (ID Tenant) o il nome di dominio completo del tenant.</span><span class="sxs-lookup"><span data-stu-id="38077-142">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="38077-143">Per gli utenti [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), il valore `-TenantId` **deve** essere un ID tenant.</span><span class="sxs-lookup"><span data-stu-id="38077-143">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="38077-144">Accedere a un altro cloud</span><span class="sxs-lookup"><span data-stu-id="38077-144">Sign in to another Cloud</span></span>

<span data-ttu-id="38077-145">I servizi cloud di Azure offrono ambienti conformi alle normative di gestione dei dati a livello di area.</span><span class="sxs-lookup"><span data-stu-id="38077-145">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="38077-146">Per gli account nel cloud di un'area, impostare l'ambiente al momento dell'accesso con l'argomento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="38077-146">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="38077-147">Ad esempio, se l'account si trova nel cloud della Cina:</span><span class="sxs-lookup"><span data-stu-id="38077-147">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="38077-148">Il comando seguente recupera un elenco degli ambienti disponibili:</span><span class="sxs-lookup"><span data-stu-id="38077-148">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```