---
title: Accedere con Azure PowerShell
description: Come effettuare l'accesso con Azure PowerShell come utente, entità servizio o con l'identità del servizio gestita.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 20194ac2282d602ba61bf130791edac9f4ffae6c
ms.sourcegitcommit: 990f82648b0aa2e970f96c02466a7134077c8c56
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2018
ms.locfileid: "38100223"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="1538c-103">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1538c-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="1538c-104">Azure PowerShell supporta più metodi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="1538c-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="1538c-105">Il modo più semplice per iniziare consiste nell'accedere in modo interattivo dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="1538c-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="1538c-106">Accedere in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="1538c-106">Sign in interactively</span></span>

<span data-ttu-id="1538c-107">Per accedere in modo interattivo, usare il cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="1538c-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="1538c-108">Durante l'esecuzione, questo cmdlet aprirà una finestra di dialogo che chiederà l'indirizzo e-mail e la password associati all'account Azure.</span><span class="sxs-lookup"><span data-stu-id="1538c-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="1538c-109">Quando si esegue l'autenticazione, queste informazioni vengono salvate per la sessione corrente di PowerShell, la finestra di dialogo viene chiusa e si ha accesso a tutti i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1538c-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1538c-110">A partire dalla versione Azure PowerShell 6.3.0, le credenziali vengono condivise tra più sessioni di PowerShell, purché si rimanga connessi a Windows.</span><span class="sxs-lookup"><span data-stu-id="1538c-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="1538c-111">Per altre informazioni, vedere l'articolo relativo alle [Credenziali persistenti](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1538c-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="1538c-112">Accedere con un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="1538c-112">Sign in with a service principal</span></span>

<span data-ttu-id="1538c-113">Le entità servizio consentono di creare account non interattivi da usare per la modifica delle risorse.</span><span class="sxs-lookup"><span data-stu-id="1538c-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="1538c-114">Le entità servizio sono analoghe agli account utente a cui è possibile applicare delle regole mediante Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1538c-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="1538c-115">Concedendo le autorizzazioni minime necessarie a un'entità servizio, è possibile garantire una sicurezza ancora maggiore agli script di automazione.</span><span class="sxs-lookup"><span data-stu-id="1538c-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="1538c-116">Se è necessario creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1538c-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="1538c-117">Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="1538c-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="1538c-118">Saranno anche necessari l'ID applicazione dell'entità servizio, le credenziali di accesso e l'ID tenant associati all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="1538c-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="1538c-119">Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="1538c-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="1538c-120">Questo cmdlet visualizza una finestra di dialogo in cui inserire l'ID utente e la password dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="1538c-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="1538c-121">Accedere tramite un'identità del servizio gestita della macchina virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="1538c-121">Sign in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="1538c-122">Identità del servizio gestito è una funzionalità in anteprima di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1538c-122">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="1538c-123">È possibile usare un'entità servizio di Identità del servizio gestito per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse.</span><span class="sxs-lookup"><span data-stu-id="1538c-123">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="1538c-124">L'identità del servizio gestita è disponibile solo in macchine virtuali in esecuzione in un cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="1538c-124">MSI is only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="1538c-125">Per altre informazioni su Identità del servizio gestito, vedere [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi) (Come usare un'Identità del servizio gestito della macchina virtuale di Azure per l'accesso e l'acquisizione di token).</span><span class="sxs-lookup"><span data-stu-id="1538c-125">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="1538c-126">Accedere a un altro cloud</span><span class="sxs-lookup"><span data-stu-id="1538c-126">Sign in to another Cloud</span></span>

<span data-ttu-id="1538c-127">I servizi cloud di Azure offrono più ambienti conformi alle norme in materia di gestione dei dati vigenti in diverse aree.</span><span class="sxs-lookup"><span data-stu-id="1538c-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="1538c-128">Se l'account di Azure si trova in un cloud associato a una di queste aree, è necessario specificare l'ambiente al momento dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="1538c-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="1538c-129">Ad esempio, se l'account si trova nel cloud della Cina, accedere usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="1538c-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="1538c-130">Usare il comando seguente per visualizzare un elenco degli ambienti disponibili:</span><span class="sxs-lookup"><span data-stu-id="1538c-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="1538c-131">Altre informazioni sulla gestione degli accessi in base al ruolo in Azure</span><span class="sxs-lookup"><span data-stu-id="1538c-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="1538c-132">Per altre informazioni su autenticazione e gestione delle sottoscrizioni in Azure, vedere [Gestire account, sottoscrizioni e ruoli amministrativi](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="1538c-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="1538c-133">Cmdlet di Azure PowerShell per la gestione dei ruoli:</span><span class="sxs-lookup"><span data-stu-id="1538c-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="1538c-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1538c-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="1538c-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1538c-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="1538c-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1538c-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="1538c-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1538c-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="1538c-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1538c-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="1538c-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1538c-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="1538c-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1538c-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
