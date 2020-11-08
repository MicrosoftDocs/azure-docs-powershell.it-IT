---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189199"
---
# <span data-ttu-id="0230b-101">Modulo AZ. support</span><span class="sxs-lookup"><span data-stu-id="0230b-101">Az.Support Module</span></span>
## <span data-ttu-id="0230b-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0230b-102">Description</span></span>
<span data-ttu-id="0230b-103">Gli argomenti di questa sezione documentano i cmdlet di PowerShell di Azure per creare e gestire i ticket di supporto di Azure nel Framework ARM (Azure Resource Manager).</span><span class="sxs-lookup"><span data-stu-id="0230b-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="0230b-104">I cmdlet sono presenti nello spazio dei nomi Microsoft. Azure. Commands. support</span><span class="sxs-lookup"><span data-stu-id="0230b-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="0230b-105">Cmdlet AZ. support</span><span class="sxs-lookup"><span data-stu-id="0230b-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="0230b-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="0230b-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="0230b-107">Ottiene l'elenco corrente di servizi Azure per il quale è disponibile il supporto.</span><span class="sxs-lookup"><span data-stu-id="0230b-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="0230b-108">Ogni servizio Azure include un set di categorie denominato classificazione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="0230b-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="0230b-109">Ottenere l'elenco corrente della classificazione dei problemi per un servizio tramite Get-AzSupportProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="0230b-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="0230b-110">È possibile usare il GUID di classificazione del servizio e dei problemi per creare un nuovo ticket di supporto usando New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="0230b-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="0230b-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="0230b-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="0230b-112">Ottiene l'elenco corrente della classificazione dei problemi per un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="0230b-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="0230b-113">È possibile usare il GUID di classificazione del servizio e dei problemi per creare un nuovo ticket di supporto usando New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="0230b-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="0230b-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="0230b-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="0230b-115">Cmdlet helper per creare un oggetto profilo del contatto di supporto.</span><span class="sxs-lookup"><span data-stu-id="0230b-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="0230b-116">Puoi usare questo oggetto per New-AzSupportTicket cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0230b-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="0230b-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="0230b-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="0230b-118">Crea un nuovo ticket di supporto di Azure.</span><span class="sxs-lookup"><span data-stu-id="0230b-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="0230b-119">Questa operazione è modellata sul comportamento della [pagina di richiesta di supporto](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)di Azure New.</span><span class="sxs-lookup"><span data-stu-id="0230b-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="0230b-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="0230b-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="0230b-121">Ottiene l'elenco dei ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="0230b-121">Gets the list of support tickets.</span></span> <span data-ttu-id="0230b-122">È possibile ottenere i dettagli del ticket di supporto completo in base al nome del biglietto o filtrare i ticket di supporto per *stato* o *i valori CreatedDate*.</span><span class="sxs-lookup"><span data-stu-id="0230b-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="0230b-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="0230b-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="0230b-124">Aggiornare la gravità del ticket di supporto, lo stato o i dettagli del contatto del cliente.</span><span class="sxs-lookup"><span data-stu-id="0230b-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="0230b-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="0230b-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="0230b-126">Ottiene le comunicazioni per un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="0230b-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="0230b-127">Puoi anche filtrare le comunicazioni di ticket di supporto per *i valori CreatedDate*   o *CommunicationType*.</span><span class="sxs-lookup"><span data-stu-id="0230b-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="0230b-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="0230b-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="0230b-129">Aggiunge una nuova comunicazione del cliente a un ticket di supporto di Azure.</span><span class="sxs-lookup"><span data-stu-id="0230b-129">Adds a new customer communication to an Azure support ticket.</span></span> 



