---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476860"
---
# <span data-ttu-id="0ce5b-101">Modulo AZ. ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0ce5b-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="0ce5b-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ce5b-102">Description</span></span>
<span data-ttu-id="0ce5b-103">Questa caratteristica viene usata dai clienti dei provider di servizi gestiti (MSPs).</span><span class="sxs-lookup"><span data-stu-id="0ce5b-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="0ce5b-104">I clienti offrono a MSP la possibilità di gestire il proprio gruppo di abbonamenti o risorse.</span><span class="sxs-lookup"><span data-stu-id="0ce5b-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="0ce5b-105">Oltre a concedere l'accesso, il cliente può anche rimuovere l'accesso o visualizzare l'accesso esistente.</span><span class="sxs-lookup"><span data-stu-id="0ce5b-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="0ce5b-106">MSPs è in grado di visualizzare l'elenco dei clienti che hanno concesso loro l'accesso agli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="0ce5b-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="0ce5b-107">Questo processo include due oggetti: una definizione di registrazione che identifica l'MSP e le definizioni di ruolo concesse agli utenti di MSP.</span><span class="sxs-lookup"><span data-stu-id="0ce5b-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="0ce5b-108">L'MSP può facoltativamente definire questo oggetto usando un Marketplace di servizi gestiti che offre le assegnazioni di Access che associano un abbonamento alla definizione.</span><span class="sxs-lookup"><span data-stu-id="0ce5b-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="0ce5b-109">Cmdlet AZ. ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0ce5b-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="0ce5b-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0ce5b-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="0ce5b-111">Ottiene una specifica assegnazione di registrazione o un elenco delle assegnazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0ce5b-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="0ce5b-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0ce5b-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="0ce5b-113">Ottiene una definizione di registrazione specifica o un elenco delle definizioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0ce5b-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="0ce5b-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0ce5b-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="0ce5b-115">Crea o aggiorna un'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0ce5b-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="0ce5b-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0ce5b-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="0ce5b-117">Crea o aggiorna una definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0ce5b-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="0ce5b-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0ce5b-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="0ce5b-119">Rimuove un'assegnazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0ce5b-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="0ce5b-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0ce5b-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="0ce5b-121">Rimuove una definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0ce5b-121">Removes a registration definition.</span></span>
