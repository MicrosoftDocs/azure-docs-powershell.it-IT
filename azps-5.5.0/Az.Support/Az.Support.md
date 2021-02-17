---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182846"
---
# Modulo Az.Support
## Descrizione
Gli argomenti di questa sezione illustrano i cmdlet di Azure PowerShell per la creazione e la gestione dei ticket di supporto di Azure nel framework di Gestione risorse di Azure (ARM). I cmdlet sono presenti nello spazio dei nomi Microsoft.Azure.Commands.Support

## Cmdlet di Az.Support
### [Get-AzSupportService](Get-AzSupportService.md)
Ottiene l'elenco corrente di servizi di Azure per cui è disponibile il supporto. Ogni servizio Azure ha un proprio set di categorie denominato classificazione dei problemi. Ottenere l'elenco corrente di classificazione dei problemi per un servizio con Get-AzSupportProblemClassification. È possibile usare il GUID per la classificazione del servizio e del problema per creare un nuovo ticket di supporto usando New-AzSupportTicket.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Recupera l'elenco corrente di classificazione dei problemi per un servizio di Azure. È possibile usare il GUID per la classificazione del servizio e del problema per creare un nuovo ticket di supporto usando New-AzSupportTicket. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Cmdlet Helper per creare un oggetto profilo del contatto di supporto. È possibile usare questo oggetto per New-AzSupportTicket cmdlet.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Crea un nuovo ticket di supporto di Azure. Questa operazione è modellata sul comportamento della pagina di richiesta di supporto di Azure [New.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Ottiene l'elenco dei ticket di supporto. È possibile ottenere i dettagli completi del ticket di supporto in base al nome del ticket o filtrare i ticket di supporto *in base a Status* o *CreatedDate.*

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Aggiorna la gravità, lo stato o i dettagli di contatto di un ticket di supporto.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Riceve comunicazioni per un ticket di supporto. È anche possibile filtrare le comunicazioni del ticket di supporto *in base a CreatedDate* *o CommunicationType.* 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Aggiunge una nuova comunicazione del cliente a un ticket di supporto di Azure. 



