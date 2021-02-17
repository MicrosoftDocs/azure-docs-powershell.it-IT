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
# <span data-ttu-id="bb3a1-101">Modulo Az.Support</span><span class="sxs-lookup"><span data-stu-id="bb3a1-101">Az.Support Module</span></span>
## <span data-ttu-id="bb3a1-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb3a1-102">Description</span></span>
<span data-ttu-id="bb3a1-103">Gli argomenti di questa sezione illustrano i cmdlet di Azure PowerShell per la creazione e la gestione dei ticket di supporto di Azure nel framework di Gestione risorse di Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="bb3a1-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="bb3a1-104">I cmdlet sono presenti nello spazio dei nomi Microsoft.Azure.Commands.Support</span><span class="sxs-lookup"><span data-stu-id="bb3a1-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="bb3a1-105">Cmdlet di Az.Support</span><span class="sxs-lookup"><span data-stu-id="bb3a1-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="bb3a1-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="bb3a1-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="bb3a1-107">Ottiene l'elenco corrente di servizi di Azure per cui è disponibile il supporto.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="bb3a1-108">Ogni servizio Azure ha un proprio set di categorie denominato classificazione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="bb3a1-109">Ottenere l'elenco corrente di classificazione dei problemi per un servizio con Get-AzSupportProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="bb3a1-110">È possibile usare il GUID per la classificazione del servizio e del problema per creare un nuovo ticket di supporto usando New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="bb3a1-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="bb3a1-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="bb3a1-112">Recupera l'elenco corrente di classificazione dei problemi per un servizio di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="bb3a1-113">È possibile usare il GUID per la classificazione del servizio e del problema per creare un nuovo ticket di supporto usando New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="bb3a1-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="bb3a1-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="bb3a1-115">Cmdlet Helper per creare un oggetto profilo del contatto di supporto.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="bb3a1-116">È possibile usare questo oggetto per New-AzSupportTicket cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="bb3a1-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="bb3a1-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="bb3a1-118">Crea un nuovo ticket di supporto di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="bb3a1-119">Questa operazione è modellata sul comportamento della pagina di richiesta di supporto di Azure [New.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)</span><span class="sxs-lookup"><span data-stu-id="bb3a1-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="bb3a1-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="bb3a1-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="bb3a1-121">Ottiene l'elenco dei ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-121">Gets the list of support tickets.</span></span> <span data-ttu-id="bb3a1-122">È possibile ottenere i dettagli completi del ticket di supporto in base al nome del ticket o filtrare i ticket di supporto *in base a Status* o *CreatedDate.*</span><span class="sxs-lookup"><span data-stu-id="bb3a1-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="bb3a1-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="bb3a1-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="bb3a1-124">Aggiorna la gravità, lo stato o i dettagli di contatto di un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="bb3a1-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="bb3a1-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="bb3a1-126">Riceve comunicazioni per un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="bb3a1-127">È anche possibile filtrare le comunicazioni del ticket di supporto *in base a CreatedDate* *o CommunicationType.*</span><span class="sxs-lookup"><span data-stu-id="bb3a1-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="bb3a1-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="bb3a1-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="bb3a1-129">Aggiunge una nuova comunicazione del cliente a un ticket di supporto di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3a1-129">Adds a new customer communication to an Azure support ticket.</span></span> 



