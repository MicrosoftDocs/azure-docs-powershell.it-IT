---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208547"
---
# <span data-ttu-id="171f8-101">Modulo Az.ResourceMover</span><span class="sxs-lookup"><span data-stu-id="171f8-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="171f8-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="171f8-102">Description</span></span>
<span data-ttu-id="171f8-103">Microsoft Azure PowerShell: cmdlet ResourceMover</span><span class="sxs-lookup"><span data-stu-id="171f8-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="171f8-104">Cmdlet Az.ResourceMover</span><span class="sxs-lookup"><span data-stu-id="171f8-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="171f8-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="171f8-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="171f8-106">Crea o aggiorna una risorsa di spostamento nella raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="171f8-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="171f8-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="171f8-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="171f8-108">Ottiene la raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="171f8-108">Gets the move collection.</span></span>

### [<span data-ttu-id="171f8-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="171f8-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="171f8-110">Ottiene la risorsa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="171f8-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="171f8-111">Get-AzResourceMoverUnresolvedWithy</span><span class="sxs-lookup"><span data-stu-id="171f8-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="171f8-112">Ottiene un elenco di dipendenze non risolte.</span><span class="sxs-lookup"><span data-stu-id="171f8-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="171f8-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="171f8-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="171f8-114">Esegue il commit del set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="171f8-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="171f8-115">L'operazione di commit viene attivata su moveResources in moveState 'CommitPending' o 'CommitFailed', al completamento di moveResource moveState esegue una transizione a Committed.</span><span class="sxs-lookup"><span data-stu-id="171f8-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="171f8-116">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="171f8-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="171f8-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="171f8-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="171f8-118">Elimina il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="171f8-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="171f8-119">L'operazione di eliminazione viene attivata su moveResources in moveState 'CommitPending' o 'DiscardFailed', al completamento di moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="171f8-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="171f8-120">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="171f8-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="171f8-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="171f8-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="171f8-122">Sposta il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="171f8-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="171f8-123">L'operazione di spostamento viene attivata dopo che moveResources si trova nello stato moveState 'MovePending' o 'MoveFailed', al completamento di moveResource moveState esegue una transizione a CommitPending.</span><span class="sxs-lookup"><span data-stu-id="171f8-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="171f8-124">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="171f8-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="171f8-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="171f8-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="171f8-126">Avvia la preparazione per il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="171f8-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="171f8-127">L'operazione di preparazione si trova su moveResources che si trova in moveState 'PreparePending' o 'PrepareFailed', al completamento di moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="171f8-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="171f8-128">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="171f8-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="171f8-129">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="171f8-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="171f8-130">Crea o aggiorna una raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="171f8-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="171f8-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="171f8-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="171f8-132">Elimina una raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="171f8-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="171f8-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="171f8-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="171f8-134">Elimina una risorsa di spostamento dalla raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="171f8-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="171f8-135">Resolve-AzResourceMoverMoveCollectionWithy</span><span class="sxs-lookup"><span data-stu-id="171f8-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="171f8-136">Calcola, risolve e convalida le dipendenze di moveResources nella raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="171f8-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

