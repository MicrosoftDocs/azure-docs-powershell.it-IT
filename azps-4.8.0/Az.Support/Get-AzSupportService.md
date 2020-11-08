---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
ms.openlocfilehash: 019f37fa6b735b506c71a914a6ea59700565fd49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191129"
---
# <span data-ttu-id="4b56e-101">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="4b56e-101">Get-AzSupportService</span></span>

## <span data-ttu-id="4b56e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b56e-102">SYNOPSIS</span></span>
<span data-ttu-id="4b56e-103">Ottenere i servizi per i quali è disponibile il supporto.</span><span class="sxs-lookup"><span data-stu-id="4b56e-103">Get services for which support is available.</span></span> 

## <span data-ttu-id="4b56e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b56e-104">SYNTAX</span></span>

### <span data-ttu-id="4b56e-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4b56e-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportService [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b56e-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b56e-106">GetByNameParameterSet</span></span>
```
Get-AzSupportService -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b56e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b56e-107">DESCRIPTION</span></span>
<span data-ttu-id="4b56e-108">Ottiene l'elenco corrente di servizi Azure per il quale è disponibile il supporto.</span><span class="sxs-lookup"><span data-stu-id="4b56e-108">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="4b56e-109">Ogni servizio può contenere una o più informazioni sul tipo di risorsa Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="4b56e-109">Each service may contain one or more Azure resource manager (ARM) resource type information.</span></span> <span data-ttu-id="4b56e-110">I tipi di risorsa (ad esempio: "Microsoft. Compute/VirtualMachines") possono essere utili per mappare le risorse di prodotto e ARM giuste quando si crea un ticket di supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="4b56e-110">Resource types (example: 'microsoft.compute/virtualmachines') can be useful to map the right product and ARM resource when creating a technical support ticket.</span></span> <span data-ttu-id="4b56e-111">Ogni servizio Azure include un set di categorie denominato classificazione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="4b56e-111">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="4b56e-112">Ottenere l'elenco corrente della classificazione dei problemi per un servizio tramite Get-AzSupportProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="4b56e-112">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="4b56e-113">È possibile usare il GUID di classificazione del servizio e dei problemi per creare un nuovo ticket di supporto usando New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="4b56e-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="4b56e-114">Usa sempre i GUID di classificazione del servizio e dei problemi ottenuti a livello di programmazione.</span><span class="sxs-lookup"><span data-stu-id="4b56e-114">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="4b56e-115">Questa procedura garantisce che siano presenti i GUID più recenti per la classificazione del servizio e dei problemi per la creazione di ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="4b56e-115">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="4b56e-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b56e-116">EXAMPLES</span></span>

### <span data-ttu-id="4b56e-117">Esempio 1: ottenere tutti i servizi disponibili per il supporto</span><span class="sxs-lookup"><span data-stu-id="4b56e-117">Example 1: Get all services available for support</span></span>
```powershell
PS C:\> Get-AzSupportService

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
809e8afe-489e-08b0-95f2-08f835a383e8 Advanced Threat Protection - Azure
6859f4e8-4a1d-13e4-f276-6d055007e83d Advanced Threat Protection - Microsoft Defender
94332e54-73b0-b8e3-306e-db3ad13d950b Advanced Threat Protection - O365
26d8424b-0a41-4443-cbc6-0309ea8708d0 Advisor
8f1ddc5f-0c5e-50c7-9810-e01a8d1da925 AKS Engine on Azure Stack
c1840ac9-309f-f235-c0ae-4782f283b698 Alerts and Action Groups
e8fe7c6f-d883-c57f-6576-cf801ca30653 Analysis Services
07651e65-958a-0877-36f3-61bbba85d783 API for FHIR
b4d0e877-0166-0474-9a76-b5be30ba40e4 API Management Service
e14f616b-42c5-4515-3d7c-67935eece51a App Configuration
445c0905-55e2-4f42-d853-ec9e17a5180e App Service Certificates
b7d2f8b7-7d20-cf2f-ddd5-5543ada54bd2 App Service Domains
101732bb-31af-ee61-7c16-d4ad77c86a50 Application Gateway
```

### <span data-ttu-id="4b56e-118">Esempio 2: ottenere informazioni dettagliate su un singolo servizio in base all'ID disponibile per il supporto</span><span class="sxs-lookup"><span data-stu-id="4b56e-118">Example 2: Get details of a single service by id available for support</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "484e2236-bc6d-b1bb-76d2-7d09278cf9ea"

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
```

## <span data-ttu-id="4b56e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b56e-119">PARAMETERS</span></span>

### <span data-ttu-id="4b56e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b56e-120">-DefaultProfile</span></span>
<span data-ttu-id="4b56e-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b56e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b56e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="4b56e-122">-Id</span></span>
<span data-ttu-id="4b56e-123">ID servizio.</span><span class="sxs-lookup"><span data-stu-id="4b56e-123">Service id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b56e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b56e-124">CommonParameters</span></span>
<span data-ttu-id="4b56e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b56e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b56e-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b56e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b56e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b56e-127">INPUTS</span></span>

### <span data-ttu-id="4b56e-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4b56e-128">None</span></span>

## <span data-ttu-id="4b56e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b56e-129">OUTPUTS</span></span>

### <span data-ttu-id="4b56e-130">Microsoft. Azure. Commands. support. Models. PSSupportService</span><span class="sxs-lookup"><span data-stu-id="4b56e-130">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="4b56e-131">Note</span><span class="sxs-lookup"><span data-stu-id="4b56e-131">NOTES</span></span>

## <span data-ttu-id="4b56e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b56e-132">RELATED LINKS</span></span>