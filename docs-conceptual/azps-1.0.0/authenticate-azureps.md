---
title: Accedere con Azure PowerShell
description: Come eseguire l'accesso con Azure PowerShell come utente, come entità servizio o con le identità gestite per le risorse di Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 8b085720aeabe26c1293ece193e050b31f99a693
ms.sourcegitcommit: ae81b08a45d8729fc8d40156422e3eb2e94de8c7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/27/2018
ms.locfileid: "53786680"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="d8df4-103">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d8df4-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="d8df4-104">Azure PowerShell supporta diversi metodi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d8df4-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="d8df4-105">Il modo più semplice per iniziare consiste nell'accedere in modo interattivo dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d8df4-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="d8df4-106">Accedere in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="d8df4-106">Sign in interactively</span></span>

<span data-ttu-id="d8df4-107">Per accedere in modo interattivo, usare il cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="d8df4-107">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="d8df4-108">Quando viene eseguito, questo cmdlet visualizzerà una stringa del token.</span><span class="sxs-lookup"><span data-stu-id="d8df4-108">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="d8df4-109">Per accedere, copiare questa stringa e incollarla in https://microsoft.com/devicelogin in un browser.</span><span class="sxs-lookup"><span data-stu-id="d8df4-109">To log in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="d8df4-110">La sessione di PowerShell verrà quindi autenticata per connettersi ad Azure.</span><span class="sxs-lookup"><span data-stu-id="d8df4-110">Your PowerShell session will then be authenticated to connect to Azure.</span></span> <span data-ttu-id="d8df4-111">Questa autenticazione dura per la sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d8df4-111">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="d8df4-112">Le credenziali vengono condivise tra più sessioni di PowerShell, purché si rimanga connessi.</span><span class="sxs-lookup"><span data-stu-id="d8df4-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="d8df4-113">Per altre informazioni, vedere l'articolo relativo alle [Credenziali persistenti](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="d8df4-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="d8df4-114">Accedere con un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="d8df4-114">Sign in with a service principal</span></span>

<span data-ttu-id="d8df4-115">Le entità servizio sono account Azure non interattivi.</span><span class="sxs-lookup"><span data-stu-id="d8df4-115">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="d8df4-116">Come per gli altri account utente, le relative autorizzazioni vengono gestite con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8df4-116">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="d8df4-117">Concedendo a un'entità servizio solo le autorizzazioni necessarie, viene garantita la sicurezza degli script di automazione.</span><span class="sxs-lookup"><span data-stu-id="d8df4-117">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="d8df4-118">Per informazioni su come creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="d8df4-118">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="d8df4-119">Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="d8df4-119">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="d8df4-120">Saranno necessari anche l'ID applicazione dell'entità servizio, le credenziali di accesso e l'ID tenant associato all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d8df4-120">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="d8df4-121">Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="d8df4-121">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="d8df4-122">Questo cmdlet visualizzerà la richiesta di inserimento dell'ID utente e della password dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d8df4-122">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="d8df4-123">Accedere con un'identità del servizio gestita di Azure</span><span class="sxs-lookup"><span data-stu-id="d8df4-123">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="d8df4-124">Le identità gestite per le risorse di Azure sono una funzionalità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8df4-124">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="d8df4-125">È possibile usare l'entità servizio di un'identità gestita per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse.</span><span class="sxs-lookup"><span data-stu-id="d8df4-125">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="d8df4-126">Le identità gestite sono disponibili solo nelle macchine virtuali in esecuzione in un cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8df4-126">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="d8df4-127">Per informazioni sulle identità gestite per le risorse di Azure, vedere [Come usare le identità gestite per le risorse di Azure in una macchina virtuale di Azure per acquisire un token di accesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="d8df4-127">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="d8df4-128">Effettuare l'accesso come Cloud Solution Provider (CSP)</span><span class="sxs-lookup"><span data-stu-id="d8df4-128">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="d8df4-129">L'accesso come [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) richiede l'uso di `-TenantId`.</span><span class="sxs-lookup"><span data-stu-id="d8df4-129">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="d8df4-130">Questo parametro può essere generalmente specificato come ID tenant o nome dominio.</span><span class="sxs-lookup"><span data-stu-id="d8df4-130">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="d8df4-131">Per l'accesso come CSP è tuttavia necessario specificare un **ID tenant**.</span><span class="sxs-lookup"><span data-stu-id="d8df4-131">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="d8df4-132">Accedere a un altro cloud</span><span class="sxs-lookup"><span data-stu-id="d8df4-132">Sign in to another Cloud</span></span>

<span data-ttu-id="d8df4-133">I servizi cloud di Azure offrono ambienti conformi alle normative di gestione dei dati a livello di area.</span><span class="sxs-lookup"><span data-stu-id="d8df4-133">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="d8df4-134">Per gli account nel cloud di un'area, impostare l'ambiente al momento dell'accesso con l'argomento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="d8df4-134">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="d8df4-135">Ad esempio, se l'account si trova nel cloud della Cina:</span><span class="sxs-lookup"><span data-stu-id="d8df4-135">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="d8df4-136">Il comando seguente recupera un elenco degli ambienti disponibili:</span><span class="sxs-lookup"><span data-stu-id="d8df4-136">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="d8df4-137">Altre informazioni sulla gestione degli accessi in base al ruolo in Azure</span><span class="sxs-lookup"><span data-stu-id="d8df4-137">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="d8df4-138">Per altre informazioni su autenticazione e gestione delle sottoscrizioni in Azure, vedere [Gestire account, sottoscrizioni e ruoli amministrativi](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="d8df4-138">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="d8df4-139">Cmdlet di Azure PowerShell per la gestione dei ruoli:</span><span class="sxs-lookup"><span data-stu-id="d8df4-139">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="d8df4-140">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d8df4-140">Get-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Get-azRoleAssignment)
* [<span data-ttu-id="d8df4-141">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d8df4-141">Get-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Get-azRoleDefinition)
* [<span data-ttu-id="d8df4-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d8df4-142">New-AzRoleAssignment</span></span>](/powershell/module/az.Resources/New-azRoleAssignment)
* [<span data-ttu-id="d8df4-143">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d8df4-143">New-AzRoleDefinition</span></span>](/powershell/module/az.Resources/New-azRoleDefinition)
* [<span data-ttu-id="d8df4-144">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d8df4-144">Remove-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [<span data-ttu-id="d8df4-145">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d8df4-145">Remove-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [<span data-ttu-id="d8df4-146">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d8df4-146">Set-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Set-azRoleDefinition)
