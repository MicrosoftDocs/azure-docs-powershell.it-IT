---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: 853c06c6179f25065efba71b2d148c36e2d74ef4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474966"
---
# <span data-ttu-id="f2e9a-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="f2e9a-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="f2e9a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e9a-103">Creare una nuova query di grafico.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-103">Create a new graph query.</span></span>

## <span data-ttu-id="f2e9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2e9a-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2e9a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2e9a-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e9a-106">Creare una nuova query di grafico.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-106">Create a new graph query.</span></span>

## <span data-ttu-id="f2e9a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2e9a-107">EXAMPLES</span></span>

### <span data-ttu-id="f2e9a-108">Esempio 1: creare una query di grafico risorse tramite il parametro di query</span><span class="sxs-lookup"><span data-stu-id="f2e9a-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="f2e9a-109">Questo comando crea una query del grafico risorse in base al parametro di query.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="f2e9a-110">Esempio 2: creare una query di grafico risorse tramite il parametro file</span><span class="sxs-lookup"><span data-stu-id="f2e9a-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="f2e9a-111">Questo comando crea una query di grafico risorse in base al parametro file.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="f2e9a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2e9a-112">PARAMETERS</span></span>

### <span data-ttu-id="f2e9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e9a-113">-DefaultProfile</span></span>
<span data-ttu-id="f2e9a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2e9a-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2e9a-115">-Description</span></span>
<span data-ttu-id="f2e9a-116">Descrizione di una query di grafico.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-116">The description of a graph query.</span></span>

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

### <span data-ttu-id="f2e9a-117">-File</span><span class="sxs-lookup"><span data-stu-id="f2e9a-117">-File</span></span>
<span data-ttu-id="f2e9a-118">Il contenuto del file verrà passato al parametro di query.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-118">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="f2e9a-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f2e9a-119">-Location</span></span>
<span data-ttu-id="f2e9a-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="f2e9a-120">The location of the resource</span></span>

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

### <span data-ttu-id="f2e9a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2e9a-121">-Name</span></span>
<span data-ttu-id="f2e9a-122">Il nome della risorsa query del grafico.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-122">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="f2e9a-123">-Query</span><span class="sxs-lookup"><span data-stu-id="f2e9a-123">-Query</span></span>
<span data-ttu-id="f2e9a-124">Query KQL che sarà Graph.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-124">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="f2e9a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2e9a-125">-ResourceGroupName</span></span>
<span data-ttu-id="f2e9a-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2e9a-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2e9a-127">-SubscriptionId</span></span>
<span data-ttu-id="f2e9a-128">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-128">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="f2e9a-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2e9a-129">-Tag</span></span>
<span data-ttu-id="f2e9a-130">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="f2e9a-130">Resource tags</span></span>

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

### <span data-ttu-id="f2e9a-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f2e9a-131">-Confirm</span></span>
<span data-ttu-id="f2e9a-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2e9a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2e9a-133">-WhatIf</span></span>
<span data-ttu-id="f2e9a-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2e9a-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2e9a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e9a-136">CommonParameters</span></span>
<span data-ttu-id="f2e9a-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2e9a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e9a-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2e9a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e9a-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2e9a-139">INPUTS</span></span>

### <span data-ttu-id="f2e9a-140">Microsoft. Azure. PowerShell. Cmdlets. ResourceGraph. Models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="f2e9a-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="f2e9a-141">Microsoft. Azure. PowerShell. Cmdlets. ResourceGraph. Models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="f2e9a-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="f2e9a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2e9a-142">OUTPUTS</span></span>

### <span data-ttu-id="f2e9a-143">Microsoft. Azure. PowerShell. Cmdlets. ResourceGraph. Models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="f2e9a-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="f2e9a-144">Note</span><span class="sxs-lookup"><span data-stu-id="f2e9a-144">NOTES</span></span>

<span data-ttu-id="f2e9a-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f2e9a-145">ALIASES</span></span>

## <span data-ttu-id="f2e9a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2e9a-146">RELATED LINKS</span></span>

