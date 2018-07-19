---
title: Accedere ad Azure PowerShell
description: Accedere ad Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: caacf32af78b98e8d9d455a8c4dd0bbb698d355f
ms.sourcegitcommit: cb1fd248920d7efca67bd6c738a3b47206df7890
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2018
ms.locfileid: "39024580"
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="01f56-103">Accedere ad Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="01f56-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="01f56-104">Azure PowerShell supporta più metodi di accesso.</span><span class="sxs-lookup"><span data-stu-id="01f56-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="01f56-105">Il modo più semplice per iniziare consiste nell'accedere in modo interattivo dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="01f56-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="01f56-106">Accesso interattivo</span><span class="sxs-lookup"><span data-stu-id="01f56-106">Interactive log in</span></span>

1. <span data-ttu-id="01f56-107">Digitare `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="01f56-107">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="01f56-108">Apparirà una finestra di dialogo che richiede le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="01f56-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="01f56-109">Digitare l'indirizzo di posta elettronica e la password associati all'account.</span><span class="sxs-lookup"><span data-stu-id="01f56-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="01f56-110">Le informazioni delle credenziali vengono autenticate e salvate in Azure, quindi la finestra viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="01f56-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="01f56-111">Accesso con un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="01f56-111">Log in with a service principal</span></span>

<span data-ttu-id="01f56-112">Le entità servizio consentono di creare account non interattivi da usare per la modifica delle risorse.</span><span class="sxs-lookup"><span data-stu-id="01f56-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="01f56-113">Le entità servizio sono analoghe agli account utente a cui è possibile applicare delle regole mediante Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="01f56-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="01f56-114">Concedendo le autorizzazioni minime necessarie a un'entità servizio, è possibile garantire una sicurezza ancora maggiore agli script di automazione.</span><span class="sxs-lookup"><span data-stu-id="01f56-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="01f56-115">Se non si dispone già di un'entità servizio, [crearne una](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="01f56-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="01f56-116">Accedere con l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="01f56-116">Log in with the service principal.</span></span>

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="01f56-117">Per ottenere il TenantId, accedere in modo interattivo e quindi recuperare il TenantId dalla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="01f56-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

    ```powershell
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="01f56-118">Accedere tramite un'Identità del servizio gestito della macchina virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="01f56-118">Log in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="01f56-119">Identità del servizio gestito è una funzionalità in anteprima di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="01f56-119">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="01f56-120">È possibile usare un'entità servizio di Identità del servizio gestito per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse.</span><span class="sxs-lookup"><span data-stu-id="01f56-120">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span>

<span data-ttu-id="01f56-121">Per altre informazioni su Identità del servizio gestito, vedere [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi) (Come usare un'Identità del servizio gestito della macchina virtuale di Azure per l'accesso e l'acquisizione di token).</span><span class="sxs-lookup"><span data-stu-id="01f56-121">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="01f56-122">Accedere a un altro cloud</span><span class="sxs-lookup"><span data-stu-id="01f56-122">Log in to another Cloud</span></span>

<span data-ttu-id="01f56-123">I servizi cloud di Azure offrono più ambienti conformi alle norme in materia di gestione dei dati vigenti in diversi paesi.</span><span class="sxs-lookup"><span data-stu-id="01f56-123">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="01f56-124">Se l'account di Azure si trova in un cloud governativo è necessario specificare l'ambiente quando si accede.</span><span class="sxs-lookup"><span data-stu-id="01f56-124">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="01f56-125">Ad esempio, se l'account si trova nel cloud della Cina, accedere usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="01f56-125">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="01f56-126">Usare il comando seguente per visualizzare un elenco degli ambienti disponibili:</span><span class="sxs-lookup"><span data-stu-id="01f56-126">Use the following command to get a list of available environments:</span></span>

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```output
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="01f56-127">Altre informazioni sulla gestione degli accessi in base al ruolo in Azure</span><span class="sxs-lookup"><span data-stu-id="01f56-127">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="01f56-128">Per altre informazioni su autenticazione e gestione delle sottoscrizioni in Azure, vedere [Gestire account, sottoscrizioni e ruoli amministrativi](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="01f56-128">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="01f56-129">Cmdlet di Azure PowerShell per la gestione dei ruoli</span><span class="sxs-lookup"><span data-stu-id="01f56-129">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="01f56-130">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="01f56-130">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="01f56-131">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="01f56-131">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="01f56-132">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="01f56-132">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="01f56-133">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="01f56-133">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="01f56-134">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="01f56-134">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="01f56-135">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="01f56-135">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="01f56-136">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="01f56-136">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
