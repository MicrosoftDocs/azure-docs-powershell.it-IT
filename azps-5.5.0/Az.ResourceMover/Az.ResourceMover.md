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
# Modulo Az.ResourceMover
## Descrizione
Microsoft Azure PowerShell: cmdlet ResourceMover

## Cmdlet Az.ResourceMover
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Crea o aggiorna una risorsa di spostamento nella raccolta di spostamento.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Ottiene la raccolta di spostamento.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Ottiene la risorsa di spostamento.

### [Get-AzResourceMoverUnresolvedWithy](Get-AzResourceMoverUnresolvedDependency.md)
Ottiene un elenco di dipendenze non risolte.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Esegue il commit del set di risorse incluse nel corpo della richiesta.
L'operazione di commit viene attivata su moveResources in moveState 'CommitPending' o 'CommitFailed', al completamento di moveResource moveState esegue una transizione a Committed.
Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Elimina il set di risorse incluse nel corpo della richiesta.
L'operazione di eliminazione viene attivata su moveResources in moveState 'CommitPending' o 'DiscardFailed', al completamento di moveResource moveState esegue una transizione a MovePending.
Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Sposta il set di risorse incluse nel corpo della richiesta.
L'operazione di spostamento viene attivata dopo che moveResources si trova nello stato moveState 'MovePending' o 'MoveFailed', al completamento di moveResource moveState esegue una transizione a CommitPending.
Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Avvia la preparazione per il set di risorse incluse nel corpo della richiesta.
L'operazione di preparazione si trova su moveResources che si trova in moveState 'PreparePending' o 'PrepareFailed', al completamento di moveResource moveState esegue una transizione a MovePending.
Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Crea o aggiorna una raccolta di spostamento.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Elimina una raccolta di spostamento.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Elimina una risorsa di spostamento dalla raccolta di spostamento.

### [Resolve-AzResourceMoverMoveCollectionWithy](Resolve-AzResourceMoverMoveCollectionDependency.md)
Calcola, risolve e convalida le dipendenze di moveResources nella raccolta di spostamento.

