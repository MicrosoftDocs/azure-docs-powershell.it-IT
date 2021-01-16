---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358777"
---
# Modulo AZ. ResourceMover
## Descrizione
PowerShell di Microsoft Azure: cmdlet ResourceMover

## Cmdlet AZ. ResourceMover
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Crea o aggiorna una risorsa di movimento nella raccolta Move.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Ottiene la raccolta di mosse.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Ottiene la risorsa di trasferimento.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Ottiene un elenco di dipendenze non risolte.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Conferma il set di risorse incluso nel corpo della richiesta.
L'operazione di commit viene attivata in moveResources in moveState ' CommitPending ' o ' CommitFailed ', in un completamento positivo il moveResource moveState esegue una transizione a Committed.
Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Elimina il set di risorse incluso nel corpo della richiesta.
L'operazione di eliminazione viene attivata in moveResources in moveState "CommitPending" o "DiscardFailed", in un completamento positivo il moveResource moveState esegue una transizione a MovePending.
Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Sposta il set di risorse incluso nel corpo della richiesta.
L'operazione di movimento viene attivata dopo che il moveResources si trova in moveState ' MovePending ' o ' MoveFailed ', in seguito a un completamento positivo il moveResource moveState esegue una transizione a CommitPending.
Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Avvia la preparazione per il set di risorse incluso nel corpo della richiesta.
L'operazione di preparazione si trova in moveResources che si trovano nel moveState ' PreparePending ' o ' PrepareFailed ', in un completamento positivo il moveResource moveState esegue una transizione a MovePending.
Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Crea o aggiorna una raccolta di mosse.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Elimina una raccolta di mosse.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Elimina una risorsa di trasferimento dalla raccolta di mosse.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Calcola, risolve e convalida le dipendenze di moveResources nella raccolta di mosse.

