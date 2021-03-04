---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 33c6f65e258ee16b0ffb6a4616ffd1c7c5f16c77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962909"
---
# <span data-ttu-id="9c0d9-101">Modulo Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="9c0d9-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="9c0d9-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c0d9-102">Description</span></span>
<span data-ttu-id="9c0d9-103">Questa funzionalità viene usata dai clienti di provider di servizi gestiti (MSP).</span><span class="sxs-lookup"><span data-stu-id="9c0d9-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="9c0d9-104">I clienti offrono a MSP la possibilità di gestire la sottoscrizione o il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9c0d9-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="9c0d9-105">Oltre a concedere l'accesso, il cliente può anche rimuovere l'accesso o visualizzare l'accesso esistente.</span><span class="sxs-lookup"><span data-stu-id="9c0d9-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="9c0d9-106">I criteri di gestione dei dati sono in grado di visualizzare l'elenco dei clienti che hanno concesso loro l'accesso alle sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="9c0d9-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="9c0d9-107">Questo processo implica due oggetti: una definizione di registrazione che identifica l'MSP e le definizioni di ruolo concesse agli utenti MSP.</span><span class="sxs-lookup"><span data-stu-id="9c0d9-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="9c0d9-108">L'MSP può facoltativamente definire questo oggetto usando un marketplace di Servizi gestiti che offre assegnazioni di Access che associano una sottoscrizione alla definizione.</span><span class="sxs-lookup"><span data-stu-id="9c0d9-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="9c0d9-109">Cmdlet di Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="9c0d9-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="9c0d9-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="9c0d9-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="9c0d9-111">Ottiene una specifica attività di registrazione o un elenco delle assegnazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c0d9-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="9c0d9-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="9c0d9-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="9c0d9-113">Ottiene una definizione di registrazione specifica o un elenco delle definizioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c0d9-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="9c0d9-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="9c0d9-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="9c0d9-115">Crea o aggiorna un'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c0d9-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="9c0d9-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="9c0d9-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="9c0d9-117">Crea o aggiorna una definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c0d9-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="9c0d9-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="9c0d9-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="9c0d9-119">Rimuove un'attività di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c0d9-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="9c0d9-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="9c0d9-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="9c0d9-121">Rimuove una definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c0d9-121">Removes a registration definition.</span></span>
