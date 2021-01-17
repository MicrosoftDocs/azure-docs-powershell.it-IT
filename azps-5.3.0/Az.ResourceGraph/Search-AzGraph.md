---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e1d9aa5c9bf2538f20d37a23b35dec4d7a850cbc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475707"
---
# <span data-ttu-id="9a451-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="9a451-101">Search-AzGraph</span></span>

## <span data-ttu-id="9a451-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a451-102">SYNOPSIS</span></span>
<span data-ttu-id="9a451-103">Esegue una query sulle risorse gestite da Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="9a451-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="9a451-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a451-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a451-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a451-105">DESCRIPTION</span></span>
<span data-ttu-id="9a451-106">Leggi altre informazioni sulla sintassi della query: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="9a451-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="9a451-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a451-107">EXAMPLES</span></span>

### <span data-ttu-id="9a451-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a451-108">Example 1</span></span>
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

<span data-ttu-id="9a451-109">Query di risorse semplici che richiede un sottoinsieme di campi delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9a451-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="9a451-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9a451-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="9a451-111">Query complessa sulle risorse con selezione di campi, filtro e riepilogo.</span><span class="sxs-lookup"><span data-stu-id="9a451-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="9a451-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9a451-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="9a451-113">Query contenente tutte le macchine virtuali che non usano dischi gestiti e include nomi visualizzati in abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9a451-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="9a451-114">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="9a451-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="9a451-115">Query che Visualizza il numero di risorse per i nomi visualizzati tenant e Subscription.</span><span class="sxs-lookup"><span data-stu-id="9a451-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="9a451-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a451-116">PARAMETERS</span></span>

### <span data-ttu-id="9a451-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a451-117">-DefaultProfile</span></span>
<span data-ttu-id="9a451-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a451-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a451-119">-Query</span><span class="sxs-lookup"><span data-stu-id="9a451-119">-Query</span></span>
<span data-ttu-id="9a451-120">Query grafico risorse.</span><span class="sxs-lookup"><span data-stu-id="9a451-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="9a451-121">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="9a451-121">-Subscription</span></span>
<span data-ttu-id="9a451-122">Abbonamento a cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="9a451-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="9a451-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="9a451-123">-Skip</span></span>
<span data-ttu-id="9a451-124">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="9a451-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="9a451-125">-Primo</span><span class="sxs-lookup"><span data-stu-id="9a451-125">-First</span></span>
<span data-ttu-id="9a451-126">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="9a451-126">The maximum number of objects to return.</span></span> <span data-ttu-id="9a451-127">Valori consentiti: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="9a451-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="9a451-128">Il valore predefinito è 100.</span><span class="sxs-lookup"><span data-stu-id="9a451-128">Default value is 100.</span></span>

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

### <span data-ttu-id="9a451-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a451-129">CommonParameters</span></span>
<span data-ttu-id="9a451-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a451-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a451-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a451-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a451-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a451-132">INPUTS</span></span>

### <span data-ttu-id="9a451-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9a451-133">None</span></span>

## <span data-ttu-id="9a451-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a451-134">OUTPUTS</span></span>

### <span data-ttu-id="9a451-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9a451-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9a451-136">Note</span><span class="sxs-lookup"><span data-stu-id="9a451-136">NOTES</span></span>

## <span data-ttu-id="9a451-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a451-137">RELATED LINKS</span></span>
