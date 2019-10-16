---
title: Gestire le sottoscrizioni di Azure con Azure PowerShell
description: Gestire le sottoscrizioni di Azure con Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 778fdb463a42b609d3a94c910a2c0f9553ef4eb9
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/15/2019
ms.locfileid: "72370318"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="a2267-103">Usare più sottoscrizioni di Azure</span><span class="sxs-lookup"><span data-stu-id="a2267-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="a2267-104">La maggior parte degli utenti di Azure non avrà mai più di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a2267-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="a2267-105">Si possono tuttavia avere più sottoscrizioni in Azure se si fa parte di più organizzazioni o se l'organizzazione ha suddiviso l'accesso a determinate risorse tra vari gruppi.</span><span class="sxs-lookup"><span data-stu-id="a2267-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="a2267-106">L'interfaccia della riga di comando supporta la selezione di una sottoscrizione sia a livello globale che per ogni comando.</span><span class="sxs-lookup"><span data-stu-id="a2267-106">The CLI supports selecting a subscription both globally and per command.</span></span>

<span data-ttu-id="a2267-107">Per informazioni dettagliate su sottoscrizioni, fatturazione e gestione dei cosi, vedere la [documentazione su fatturazione e gestione dei costi](/azure/billing/).</span><span class="sxs-lookup"><span data-stu-id="a2267-107">For detailed information on subscriptions, billing, and cost management, see the [billing and cost management documentation](/azure/billing/).</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="a2267-108">Tenant, utenti e sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="a2267-108">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="a2267-109">La differenza tra tenant, utenti e sottoscrizioni in Azure potrebbe non essere del tutto chiara.</span><span class="sxs-lookup"><span data-stu-id="a2267-109">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="a2267-110">Un _tenant_ è l'entità di Azure Active Directory che include un'intera organizzazione.</span><span class="sxs-lookup"><span data-stu-id="a2267-110">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="a2267-111">Il tenant ha almeno una _sottoscrizione_ e un _utente_.</span><span class="sxs-lookup"><span data-stu-id="a2267-111">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="a2267-112">Un utente è una persona ed è associato a un solo tenant, corrispondente all'organizzazione a cui appartiene.</span><span class="sxs-lookup"><span data-stu-id="a2267-112">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="a2267-113">Gli utenti sono gli account che accedono ad Azure per creare, gestire e usare le risorse.</span><span class="sxs-lookup"><span data-stu-id="a2267-113">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="a2267-114">Un utente può avere accesso a più _sottoscrizioni_, che sono contratti con Microsoft per l'uso dei servizi cloud, incluso Azure.</span><span class="sxs-lookup"><span data-stu-id="a2267-114">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="a2267-115">Ogni risorsa è associata a una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a2267-115">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="a2267-116">Per altre informazioni sulle differenze tra tenant, utenti e sottoscrizioni, vedere il [dizionario della terminologia cloud di Azure](/azure/azure-glossary-cloud-terminology).</span><span class="sxs-lookup"><span data-stu-id="a2267-116">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="a2267-117">Per informazioni su come aggiungere una sottoscrizione al tenant di Azure Active Directory, vedere [Come aggiungere una sottoscrizione di Azure ad Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span><span class="sxs-lookup"><span data-stu-id="a2267-117">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="a2267-118">Per informazioni su come eseguire l'accesso a un tenant specifico, vedere [Accedere con Azure PowerShell](/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="a2267-118">To learn how to sign in to a specific tenant, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="a2267-119">Cambiare la sottoscrizione attiva</span><span class="sxs-lookup"><span data-stu-id="a2267-119">Change the active subscription</span></span>

<span data-ttu-id="a2267-120">In Azure PowerShell l'accesso alle risorse per una sottoscrizione richiede la modifica della sottoscrizione associata alla sessione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="a2267-120">In Azure PowerShell, accessing the resources for a subscription requires changing the subscription associated with your current Azure session.</span></span>
<span data-ttu-id="a2267-121">Questa operazione viene eseguita modificando il contesto della sessione attiva, cioè le informazioni su tenant, sottoscrizione e cmdlet dell'utente in cui deve essere eseguita.</span><span class="sxs-lookup"><span data-stu-id="a2267-121">This is done by modifying the active session context, the information about which tenant, subscription, and user cmdlets should be run against.</span></span>
<span data-ttu-id="a2267-122">Per modificare le sottoscrizioni, è prima necessario recuperare un oggetto di contesto di Azure PowerShell con [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) e quindi di modificare il contesto corrente con [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="a2267-122">In order to change subscriptions, an Azure PowerShell Context object first needs to be retrieved with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and then the current context changed with [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span></span>

<span data-ttu-id="a2267-123">L'esempio seguente mostra come ottenere una sottoscrizione nel tenant attualmente attivo e impostarla come sessione attiva:</span><span class="sxs-lookup"><span data-stu-id="a2267-123">The next example shows how to get a subscription in the currently active tenant, and set it as the active session:</span></span>

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

<span data-ttu-id="a2267-124">Per altre informazioni sui contesti di Azure PowerShell, tra cui come salvarli e passare rapidamente dall'uno all'altro per lavorare facilmente con più sottoscrizioni, vedere [Conservare le credenziali con i contesti di Azure PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="a2267-124">To learn more about Azure PowerShell contexts, including how to save them and quickly switch between them for working with multiple subscriptions easily, see [Persist credentials with Azure PowerShell contexts](context-persistence.md).</span></span>
