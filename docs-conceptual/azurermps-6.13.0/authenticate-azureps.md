---
title: Accedere con Azure PowerShell
description: Come eseguire l'accesso con Azure PowerShell come utente, come entità servizio o con le identità gestite per le risorse di Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 6a42217c47c1e5101a708da87c15fc14004f2069
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587874"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="e434b-103">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e434b-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="e434b-104">Azure PowerShell supporta diversi metodi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="e434b-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="e434b-105">Il modo più semplice per iniziare consiste nell'accedere in modo interattivo dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e434b-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="e434b-106">Accedere in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="e434b-106">Sign in interactively</span></span>

<span data-ttu-id="e434b-107">Per accedere in modo interattivo, usare il cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="e434b-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount
```

<span data-ttu-id="e434b-108">Durante l'esecuzione, questo cmdlet aprirà una finestra di dialogo che chiederà l'indirizzo e-mail e la password associati all'account Azure.</span><span class="sxs-lookup"><span data-stu-id="e434b-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="e434b-109">Questa autenticazione dura per la sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e434b-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e434b-110">A partire dalla versione Azure PowerShell 6.3.0, le credenziali vengono condivise tra più sessioni di PowerShell, purché si rimanga connessi a Windows.</span><span class="sxs-lookup"><span data-stu-id="e434b-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="e434b-111">Per altre informazioni, vedere l'articolo relativo alle [Credenziali persistenti](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="e434b-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="e434b-112">Accedere con un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="e434b-112">Sign in with a service principal</span></span>

<span data-ttu-id="e434b-113">Le entità servizio sono account Azure non interattivi.</span><span class="sxs-lookup"><span data-stu-id="e434b-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="e434b-114">Come per gli altri account utente, le relative autorizzazioni vengono gestite con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e434b-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="e434b-115">Concedendo a un'entità servizio solo le autorizzazioni necessarie, viene garantita la sicurezza degli script di automazione.</span><span class="sxs-lookup"><span data-stu-id="e434b-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="e434b-116">Per informazioni su come creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="e434b-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="e434b-117">Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="e434b-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="e434b-118">Saranno necessari anche l'ID applicazione dell'entità servizio, le credenziali di accesso e l'ID tenant associato all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="e434b-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="e434b-119">Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="e434b-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="e434b-120">Questo cmdlet visualizza una finestra di dialogo in cui inserire l'ID utente e la password dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="e434b-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="e434b-121">Accedere con un'identità del servizio gestita di Azure</span><span class="sxs-lookup"><span data-stu-id="e434b-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="e434b-122">Le identità gestite per le risorse di Azure sono una funzionalità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e434b-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="e434b-123">È possibile usare l'entità servizio di un'identità gestita per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse.</span><span class="sxs-lookup"><span data-stu-id="e434b-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="e434b-124">Le identità gestite sono disponibili solo nelle macchine virtuali in esecuzione in un cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="e434b-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="e434b-125">Per informazioni sulle identità gestite per le risorse di Azure, vedere [Come usare le identità gestite per le risorse di Azure in una macchina virtuale di Azure per acquisire un token di accesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="e434b-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="e434b-126">Effettuare l'accesso come Cloud Solution Provider (CSP)</span><span class="sxs-lookup"><span data-stu-id="e434b-126">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="e434b-127">L'accesso come [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) richiede l'uso di `-TenantId`.</span><span class="sxs-lookup"><span data-stu-id="e434b-127">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="e434b-128">Questo parametro può essere generalmente specificato come ID tenant o nome dominio.</span><span class="sxs-lookup"><span data-stu-id="e434b-128">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="e434b-129">Per l'accesso come CSP è tuttavia necessario specificare un **ID tenant**.</span><span class="sxs-lookup"><span data-stu-id="e434b-129">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="e434b-130">Accedere a un altro cloud</span><span class="sxs-lookup"><span data-stu-id="e434b-130">Sign in to another Cloud</span></span>

<span data-ttu-id="e434b-131">I servizi cloud di Azure offrono ambienti conformi alle normative di gestione dei dati a livello di area.</span><span class="sxs-lookup"><span data-stu-id="e434b-131">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="e434b-132">Per gli account nel cloud di un'area, impostare l'ambiente al momento dell'accesso con l'argomento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="e434b-132">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="e434b-133">Ad esempio, se l'account si trova nel cloud della Cina:</span><span class="sxs-lookup"><span data-stu-id="e434b-133">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="e434b-134">Il comando seguente recupera un elenco degli ambienti disponibili:</span><span class="sxs-lookup"><span data-stu-id="e434b-134">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="e434b-135">Altre informazioni sulla gestione degli accessi in base al ruolo in Azure</span><span class="sxs-lookup"><span data-stu-id="e434b-135">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="e434b-136">Per altre informazioni su autenticazione e gestione delle sottoscrizioni in Azure, vedere [Gestire account, sottoscrizioni e ruoli amministrativi](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="e434b-136">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="e434b-137">Cmdlet di Azure PowerShell per la gestione dei ruoli:</span><span class="sxs-lookup"><span data-stu-id="e434b-137">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="e434b-138">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e434b-138">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="e434b-139">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e434b-139">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="e434b-140">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e434b-140">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="e434b-141">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e434b-141">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="e434b-142">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e434b-142">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="e434b-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e434b-143">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="e434b-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e434b-144">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
