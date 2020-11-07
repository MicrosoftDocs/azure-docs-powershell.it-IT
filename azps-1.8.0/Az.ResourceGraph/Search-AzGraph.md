---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: 5a9a47ff6f4a329d3e48ec54df85ade3be5ae84d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677424"
---
# <span data-ttu-id="8b4cf-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="8b4cf-101">Search-AzGraph</span></span>

## <span data-ttu-id="8b4cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b4cf-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4cf-103">Esegue una query sulle risorse gestite da Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="8b4cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b4cf-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b4cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b4cf-105">DESCRIPTION</span></span>
<span data-ttu-id="8b4cf-106">Leggi altre informazioni sulla sintassi della query: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="8b4cf-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="8b4cf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b4cf-107">EXAMPLES</span></span>

### <span data-ttu-id="8b4cf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b4cf-108">Example 1</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location, tags" -First 3


id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.Compute/virtualMachineScaleSets/nt
name       : nt
type       : microsoft.compute/virtualmachinescalesets
location   : eastus
tags       : @{resourceType=Service Fabric; clusterName=gov-art-int-nt-a}

id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.EventGrid/topics/egtopic-1
name       : egtopic-1
type       : microsoft.eventgrid/topics
location   : westus2
tags       :
```

<span data-ttu-id="8b4cf-109">Query di risorse semplici che richiede un sottoinsieme di campi delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="8b4cf-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8b4cf-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="8b4cf-111">Query complessa sulle risorse con selezione di campi, filtro e riepilogo.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

## <span data-ttu-id="8b4cf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b4cf-112">PARAMETERS</span></span>

### <span data-ttu-id="8b4cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4cf-113">-DefaultProfile</span></span>
<span data-ttu-id="8b4cf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b4cf-115">-Query</span><span class="sxs-lookup"><span data-stu-id="8b4cf-115">-Query</span></span>
<span data-ttu-id="8b4cf-116">Query grafico risorse.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-116">Resource Graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4cf-117">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="8b4cf-117">-Subscription</span></span>
<span data-ttu-id="8b4cf-118">Abbonamento a cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-118">Subscription(s) to run query against.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4cf-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="8b4cf-119">-Skip</span></span>
<span data-ttu-id="8b4cf-120">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-120">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4cf-121">-Primo</span><span class="sxs-lookup"><span data-stu-id="8b4cf-121">-First</span></span>
<span data-ttu-id="8b4cf-122">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-122">The maximum number of objects to return.</span></span> <span data-ttu-id="8b4cf-123">Valori consentiti: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-123">Allowed values: 1-5000.</span></span>
<span data-ttu-id="8b4cf-124">Il valore predefinito è 100.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-124">Default value is 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4cf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4cf-125">CommonParameters</span></span>
<span data-ttu-id="8b4cf-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4cf-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b4cf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4cf-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b4cf-128">INPUTS</span></span>

### <span data-ttu-id="8b4cf-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8b4cf-129">None</span></span>

## <span data-ttu-id="8b4cf-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b4cf-130">OUTPUTS</span></span>

### <span data-ttu-id="8b4cf-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8b4cf-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8b4cf-132">Note</span><span class="sxs-lookup"><span data-stu-id="8b4cf-132">NOTES</span></span>

## <span data-ttu-id="8b4cf-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b4cf-133">RELATED LINKS</span></span>
