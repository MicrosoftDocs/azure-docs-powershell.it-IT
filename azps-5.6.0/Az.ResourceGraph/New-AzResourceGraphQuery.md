---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: c20e7c63fac01459d3df9d417b0fcec6aed83d36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000141"
---
# <span data-ttu-id="b6008-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="b6008-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="b6008-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6008-102">SYNOPSIS</span></span>
<span data-ttu-id="b6008-103">Creare una nuova query grafico.</span><span class="sxs-lookup"><span data-stu-id="b6008-103">Create a new graph query.</span></span>

## <span data-ttu-id="b6008-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6008-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6008-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6008-105">DESCRIPTION</span></span>
<span data-ttu-id="b6008-106">Creare una nuova query grafico.</span><span class="sxs-lookup"><span data-stu-id="b6008-106">Create a new graph query.</span></span>

## <span data-ttu-id="b6008-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6008-107">EXAMPLES</span></span>

### <span data-ttu-id="b6008-108">Esempio 1: Creare una query del grafico delle risorse tramite il parametro di query</span><span class="sxs-lookup"><span data-stu-id="b6008-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="b6008-109">Questo comando crea una query del diagramma risorse tramite il parametro della query.</span><span class="sxs-lookup"><span data-stu-id="b6008-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="b6008-110">Esempio 2: Creare una query del grafico delle risorse tramite il parametro del file</span><span class="sxs-lookup"><span data-stu-id="b6008-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="b6008-111">Questo comando crea una query del diagramma risorse tramite il parametro del file.</span><span class="sxs-lookup"><span data-stu-id="b6008-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="b6008-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6008-112">PARAMETERS</span></span>

### <span data-ttu-id="b6008-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6008-113">-DefaultProfile</span></span>
<span data-ttu-id="b6008-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6008-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6008-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6008-115">-Description</span></span>
<span data-ttu-id="b6008-116">Descrizione di una query grafico.</span><span class="sxs-lookup"><span data-stu-id="b6008-116">The description of a graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6008-117">-File</span><span class="sxs-lookup"><span data-stu-id="b6008-117">-File</span></span>
<span data-ttu-id="b6008-118">Il contenuto del file verrà passato al parametro della query.</span><span class="sxs-lookup"><span data-stu-id="b6008-118">The content of the file will be passed to the query parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6008-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b6008-119">-Location</span></span>
<span data-ttu-id="b6008-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="b6008-120">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6008-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b6008-121">-Name</span></span>
<span data-ttu-id="b6008-122">Nome della risorsa Query grafico.</span><span class="sxs-lookup"><span data-stu-id="b6008-122">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6008-123">-Query</span><span class="sxs-lookup"><span data-stu-id="b6008-123">-Query</span></span>
<span data-ttu-id="b6008-124">Query KQL che verrà tracciata.</span><span class="sxs-lookup"><span data-stu-id="b6008-124">KQL query that will be graph.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6008-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6008-125">-ResourceGroupName</span></span>
<span data-ttu-id="b6008-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6008-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6008-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6008-127">-SubscriptionId</span></span>
<span data-ttu-id="b6008-128">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6008-128">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6008-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6008-129">-Tag</span></span>
<span data-ttu-id="b6008-130">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="b6008-130">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6008-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6008-131">-Confirm</span></span>
<span data-ttu-id="b6008-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6008-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6008-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6008-133">-WhatIf</span></span>
<span data-ttu-id="b6008-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6008-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6008-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6008-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6008-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6008-136">CommonParameters</span></span>
<span data-ttu-id="b6008-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6008-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6008-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6008-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6008-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6008-139">INPUTS</span></span>

### <span data-ttu-id="b6008-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="b6008-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="b6008-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="b6008-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="b6008-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6008-142">OUTPUTS</span></span>

### <span data-ttu-id="b6008-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="b6008-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="b6008-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6008-144">NOTES</span></span>

<span data-ttu-id="b6008-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b6008-145">ALIASES</span></span>

## <span data-ttu-id="b6008-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6008-146">RELATED LINKS</span></span>

