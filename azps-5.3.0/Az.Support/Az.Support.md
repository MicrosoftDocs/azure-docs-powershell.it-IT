---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474587"
---
# Modulo AZ. support
## Descrizione
Gli argomenti di questa sezione documentano i cmdlet di PowerShell di Azure per creare e gestire i ticket di supporto di Azure nel Framework ARM (Azure Resource Manager). I cmdlet sono presenti nello spazio dei nomi Microsoft. Azure. Commands. support

## Cmdlet AZ. support
### [Get-AzSupportService](Get-AzSupportService.md)
Ottiene l'elenco corrente di servizi Azure per il quale è disponibile il supporto. Ogni servizio Azure include un set di categorie denominato classificazione dei problemi. Ottenere l'elenco corrente della classificazione dei problemi per un servizio tramite Get-AzSupportProblemClassification. È possibile usare il GUID di classificazione del servizio e dei problemi per creare un nuovo ticket di supporto usando New-AzSupportTicket.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Ottiene l'elenco corrente della classificazione dei problemi per un servizio Azure. È possibile usare il GUID di classificazione del servizio e dei problemi per creare un nuovo ticket di supporto usando New-AzSupportTicket. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Cmdlet helper per creare un oggetto profilo del contatto di supporto. Puoi usare questo oggetto per New-AzSupportTicket cmdlet.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Crea un nuovo ticket di supporto di Azure. Questa operazione è modellata sul comportamento della [pagina di richiesta di supporto](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)di Azure New.

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Ottiene l'elenco dei ticket di supporto. È possibile ottenere i dettagli del ticket di supporto completo in base al nome del biglietto o filtrare i ticket di supporto per *stato* o *i valori CreatedDate*.

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Aggiornare la gravità del ticket di supporto, lo stato o i dettagli del contatto del cliente.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Ottiene le comunicazioni per un ticket di supporto. Puoi anche filtrare le comunicazioni di ticket di supporto per *i valori CreatedDate* o *CommunicationType*. 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Aggiunge una nuova comunicazione del cliente a un ticket di supporto di Azure. 



