---
title: Accedere con Azure PowerShell
description: Come eseguire l'accesso con Azure PowerShell come utente, come entità servizio o con le identità gestite per le risorse di Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 9a93145f2abeea466a739775ca8ae7e337e78166
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275657"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="5a49b-103">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5a49b-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="5a49b-104">Azure PowerShell supporta più metodi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="5a49b-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="5a49b-105">Il modo più semplice per iniziare consiste nell'accedere in modo interattivo dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5a49b-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="5a49b-106">Accedere in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="5a49b-106">Sign in interactively</span></span>

<span data-ttu-id="5a49b-107">Per accedere in modo interattivo, usare il cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="5a49b-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount
```

<span data-ttu-id="5a49b-108">Durante l'esecuzione, questo cmdlet aprirà una finestra di dialogo che chiederà l'indirizzo e-mail e la password associati all'account Azure.</span><span class="sxs-lookup"><span data-stu-id="5a49b-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="5a49b-109">Quando si esegue l'autenticazione, queste informazioni vengono salvate per la sessione corrente di PowerShell, la finestra di dialogo viene chiusa e si ha accesso a tutti i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5a49b-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a49b-110">Questo accesso è valido _solo_ per la sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5a49b-110">This sign in is for the current PowerShell session _only_.</span></span> <span data-ttu-id="5a49b-111">Per mantenere l'autenticazione da una sessione all'altra, vedere l'articolo sulle [Credenziali persistenti](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="5a49b-111">To persist authentication across multiple sessions, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="5a49b-112">Accedere con un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="5a49b-112">Sign in with a service principal</span></span>

<span data-ttu-id="5a49b-113">Le entità servizio consentono di creare account non interattivi da usare per la modifica delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5a49b-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="5a49b-114">Le entità servizio sono analoghe agli account utente a cui è possibile applicare delle regole mediante Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5a49b-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="5a49b-115">Concedendo le autorizzazioni minime necessarie a un'entità servizio, è possibile garantire una sicurezza ancora maggiore agli script di automazione.</span><span class="sxs-lookup"><span data-stu-id="5a49b-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="5a49b-116">Se è necessario creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="5a49b-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="5a49b-117">Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="5a49b-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="5a49b-118">Saranno anche necessari l'ID applicazione dell'entità servizio, le credenziali di accesso e l'ID tenant associati all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5a49b-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="5a49b-119">Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="5a49b-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="5a49b-120">Questo cmdlet visualizza una finestra di dialogo in cui inserire l'ID utente e la password dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5a49b-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="5a49b-121">Accedere con le identità gestite per le risorse di Azure</span><span class="sxs-lookup"><span data-stu-id="5a49b-121">Sign in using managed identities for Azure resources</span></span>

<span data-ttu-id="5a49b-122">Le identità gestite per le risorse di Azure sono una funzionalità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5a49b-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="5a49b-123">È possibile usare l'entità servizio di un'identità gestita per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse.</span><span class="sxs-lookup"><span data-stu-id="5a49b-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="5a49b-124">Le identità gestite sono disponibili solo nelle macchine virtuali in esecuzione in un cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a49b-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="5a49b-125">Per informazioni sulle identità gestite per le risorse di Azure, vedere [Come usare le identità gestite per le risorse di Azure in una macchina virtuale di Azure per acquisire un token di accesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="5a49b-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="5a49b-126">Accedere a un altro cloud</span><span class="sxs-lookup"><span data-stu-id="5a49b-126">Sign in to another Cloud</span></span>

<span data-ttu-id="5a49b-127">I servizi cloud di Azure offrono più ambienti conformi alle norme in materia di gestione dei dati vigenti in diverse aree.</span><span class="sxs-lookup"><span data-stu-id="5a49b-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="5a49b-128">Se l'account di Azure si trova in un cloud associato a una di queste aree, è necessario specificare l'ambiente al momento dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="5a49b-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="5a49b-129">Ad esempio, se l'account si trova nel cloud della Cina, accedere usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="5a49b-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="5a49b-130">Usare il comando seguente per visualizzare un elenco degli ambienti disponibili:</span><span class="sxs-lookup"><span data-stu-id="5a49b-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="5a49b-131">Altre informazioni sulla gestione degli accessi in base al ruolo in Azure</span><span class="sxs-lookup"><span data-stu-id="5a49b-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="5a49b-132">Per altre informazioni su autenticazione e gestione delle sottoscrizioni in Azure, vedere [Gestire account, sottoscrizioni e ruoli amministrativi](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="5a49b-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="5a49b-133">Cmdlet di Azure PowerShell per la gestione dei ruoli:</span><span class="sxs-lookup"><span data-stu-id="5a49b-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="5a49b-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5a49b-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="5a49b-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5a49b-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="5a49b-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5a49b-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="5a49b-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5a49b-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="5a49b-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5a49b-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="5a49b-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5a49b-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="5a49b-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5a49b-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
