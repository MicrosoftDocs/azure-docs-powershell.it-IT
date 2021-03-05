---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: 0f43535baa284dbe9f7c69aee5a688443172089a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000046"
---
# <span data-ttu-id="28097-101">Modulo Az.ResourceMover</span><span class="sxs-lookup"><span data-stu-id="28097-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="28097-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28097-102">Description</span></span>
<span data-ttu-id="28097-103">Microsoft Azure PowerShell: cmdlet ResourceMover</span><span class="sxs-lookup"><span data-stu-id="28097-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="28097-104">Cmdlet Az.ResourceMover</span><span class="sxs-lookup"><span data-stu-id="28097-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="28097-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="28097-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="28097-106">Crea o aggiorna una risorsa spostata nella raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="28097-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="28097-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="28097-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="28097-108">Ottiene la raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="28097-108">Gets the move collection.</span></span>

### [<span data-ttu-id="28097-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="28097-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="28097-110">Ottiene la risorsa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="28097-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="28097-111">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="28097-111">Get-AzResourceMoverRequiredForResources</span></span>](Get-AzResourceMoverRequiredForResources.md)
<span data-ttu-id="28097-112">Elenco delle risorse di spostamento per cui è necessaria una risorsa arm.</span><span class="sxs-lookup"><span data-stu-id="28097-112">List of the move resources for which an arm resource is required for.</span></span>

### [<span data-ttu-id="28097-113">Get-AzResourceMoverUnresolvedWithy</span><span class="sxs-lookup"><span data-stu-id="28097-113">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="28097-114">Ottiene un elenco di dipendenze non risolte.</span><span class="sxs-lookup"><span data-stu-id="28097-114">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="28097-115">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="28097-115">Invoke-AzResourceMoverBulkRemove</span></span>](Invoke-AzResourceMoverBulkRemove.md)
<span data-ttu-id="28097-116">Rimuove il set di risorse di spostamento incluse nel corpo della richiesta dalla raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="28097-116">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="28097-117">La saturazione viene eseguita dal servizio.</span><span class="sxs-lookup"><span data-stu-id="28097-117">The orchestration is done by service.</span></span>
<span data-ttu-id="28097-118">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="28097-118">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="28097-119">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="28097-119">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="28097-120">Esegue il commit del set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="28097-120">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="28097-121">L'operazione di commit viene attivata su moveResources in moveState 'CommitPending' o 'CommitFailed', al completamento di moveResource moveState esegue una transizione a Committed.</span><span class="sxs-lookup"><span data-stu-id="28097-121">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="28097-122">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="28097-122">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="28097-123">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="28097-123">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="28097-124">Elimina il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="28097-124">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="28097-125">L'operazione di eliminazione viene attivata su moveResources in moveState 'CommitPending' o 'DiscardFailed', al completamento di moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="28097-125">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="28097-126">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="28097-126">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="28097-127">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="28097-127">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="28097-128">Sposta il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="28097-128">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="28097-129">L'operazione di spostamento viene attivata dopo che moveResources si trova nello stato moveState 'MovePending' o 'MoveFailed', al completamento di moveResource moveState esegue una transizione a CommitPending.</span><span class="sxs-lookup"><span data-stu-id="28097-129">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="28097-130">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="28097-130">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="28097-131">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="28097-131">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="28097-132">Avvia la preparazione per il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="28097-132">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="28097-133">L'operazione di preparazione si trova su moveResources che si trova in moveState 'PreparePending' o 'PrepareFailed', al completamento di moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="28097-133">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="28097-134">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="28097-134">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="28097-135">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="28097-135">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="28097-136">Crea o aggiorna una raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="28097-136">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="28097-137">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="28097-137">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="28097-138">Elimina una raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="28097-138">Deletes a move collection.</span></span>

### [<span data-ttu-id="28097-139">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="28097-139">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="28097-140">Elimina una risorsa di spostamento dalla raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="28097-140">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="28097-141">Resolve-AzResourceMoverMoveCollection Più risorse</span><span class="sxs-lookup"><span data-stu-id="28097-141">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="28097-142">Calcola, risolve e convalida le dipendenze di moveResources nella raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="28097-142">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

