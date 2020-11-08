---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189906"
---
# <span data-ttu-id="f6683-101">Modulo AZ. ResourceMover</span><span class="sxs-lookup"><span data-stu-id="f6683-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="f6683-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6683-102">Description</span></span>
<span data-ttu-id="f6683-103">PowerShell di Microsoft Azure: cmdlet ResourceMover</span><span class="sxs-lookup"><span data-stu-id="f6683-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="f6683-104">Cmdlet AZ. ResourceMover</span><span class="sxs-lookup"><span data-stu-id="f6683-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="f6683-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="f6683-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="f6683-106">Crea o aggiorna una risorsa di movimento nella raccolta Move.</span><span class="sxs-lookup"><span data-stu-id="f6683-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="f6683-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f6683-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="f6683-108">Ottiene la raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="f6683-108">Gets the move collection.</span></span>

### [<span data-ttu-id="f6683-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="f6683-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="f6683-110">Ottiene la risorsa di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="f6683-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="f6683-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="f6683-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="f6683-112">Ottiene un elenco di dipendenze non risolte.</span><span class="sxs-lookup"><span data-stu-id="f6683-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="f6683-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="f6683-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="f6683-114">Conferma il set di risorse incluso nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="f6683-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="f6683-115">L'operazione di commit viene attivata in moveResources in moveState ' CommitPending ' o ' CommitFailed ', in un completamento positivo il moveResource moveState esegue una transizione a Committed.</span><span class="sxs-lookup"><span data-stu-id="f6683-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="f6683-116">Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="f6683-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="f6683-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="f6683-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="f6683-118">Elimina il set di risorse incluso nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="f6683-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="f6683-119">L'operazione di eliminazione viene attivata in moveResources in moveState "CommitPending" o "DiscardFailed", in un completamento positivo il moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="f6683-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="f6683-120">Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="f6683-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="f6683-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="f6683-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="f6683-122">Sposta il set di risorse incluso nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="f6683-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="f6683-123">L'operazione di movimento viene attivata dopo che il moveResources si trova in moveState ' MovePending ' o ' MoveFailed ', in seguito a un completamento positivo il moveResource moveState esegue una transizione a CommitPending.</span><span class="sxs-lookup"><span data-stu-id="f6683-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="f6683-124">Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="f6683-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="f6683-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="f6683-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="f6683-126">Avvia la preparazione per il set di risorse incluso nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="f6683-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="f6683-127">L'operazione di preparazione si trova in moveResources che si trovano nel moveState ' PreparePending ' o ' PrepareFailed ', in un completamento positivo il moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="f6683-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="f6683-128">Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="f6683-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="f6683-129">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f6683-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="f6683-130">Crea o aggiorna una raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="f6683-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="f6683-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f6683-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="f6683-132">Elimina una raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="f6683-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="f6683-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="f6683-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="f6683-134">Elimina una risorsa di trasferimento dalla raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="f6683-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="f6683-135">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="f6683-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="f6683-136">Calcola, risolve e convalida le dipendenze di moveResources nella raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="f6683-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>
