---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e96d4fa13dc1b479c37b56cb3887b6d519df24f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000109"
---
# <span data-ttu-id="97fad-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="97fad-101">Search-AzGraph</span></span>

## <span data-ttu-id="97fad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97fad-102">SYNOPSIS</span></span>
<span data-ttu-id="97fad-103">Esegue una query sulle risorse gestite da Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="97fad-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="97fad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97fad-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97fad-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="97fad-105">DESCRIPTION</span></span>
<span data-ttu-id="97fad-106">Per altre informazioni sulla sintassi della query, vedere: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="97fad-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="97fad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97fad-107">EXAMPLES</span></span>

### <span data-ttu-id="97fad-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97fad-108">Example 1</span></span>
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

<span data-ttu-id="97fad-109">Query di risorse semplice che richiede un sottoinsieme di campi delle risorse.</span><span class="sxs-lookup"><span data-stu-id="97fad-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="97fad-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="97fad-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="97fad-111">Query complessa sulle risorse con selezione dei campi, filtro e riepilogo.</span><span class="sxs-lookup"><span data-stu-id="97fad-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="97fad-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="97fad-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="97fad-113">Query con tutte le macchine virtuali che non usano dischi gestiti e che include i nomi visualizzati dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="97fad-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="97fad-114">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="97fad-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="97fad-115">Query che visualizza il conteggio delle risorse per nome visualizzato del tenant e della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="97fad-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="97fad-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97fad-116">PARAMETERS</span></span>

### <span data-ttu-id="97fad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97fad-117">-DefaultProfile</span></span>
<span data-ttu-id="97fad-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97fad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97fad-119">-Query</span><span class="sxs-lookup"><span data-stu-id="97fad-119">-Query</span></span>
<span data-ttu-id="97fad-120">Query Diagramma risorse.</span><span class="sxs-lookup"><span data-stu-id="97fad-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="97fad-121">-Abbonamento</span><span class="sxs-lookup"><span data-stu-id="97fad-121">-Subscription</span></span>
<span data-ttu-id="97fad-122">Sottoscrizioni su cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="97fad-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="97fad-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="97fad-123">-Skip</span></span>
<span data-ttu-id="97fad-124">Ignora i primi N oggetti e quindi ottiene gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="97fad-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="97fad-125">-First</span><span class="sxs-lookup"><span data-stu-id="97fad-125">-First</span></span>
<span data-ttu-id="97fad-126">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="97fad-126">The maximum number of objects to return.</span></span> <span data-ttu-id="97fad-127">Valori consentiti: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="97fad-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="97fad-128">Il valore predefinito è 100.</span><span class="sxs-lookup"><span data-stu-id="97fad-128">Default value is 100.</span></span>

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

### <span data-ttu-id="97fad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97fad-129">CommonParameters</span></span>
<span data-ttu-id="97fad-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97fad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97fad-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97fad-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97fad-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="97fad-132">INPUTS</span></span>

### <span data-ttu-id="97fad-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="97fad-133">None</span></span>

## <span data-ttu-id="97fad-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97fad-134">OUTPUTS</span></span>

### <span data-ttu-id="97fad-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="97fad-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="97fad-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="97fad-136">NOTES</span></span>

## <span data-ttu-id="97fad-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97fad-137">RELATED LINKS</span></span>
