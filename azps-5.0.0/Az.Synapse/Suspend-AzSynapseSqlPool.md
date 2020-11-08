---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: fef045417a9c6cb22cd3ec3651a5b27b127b3b9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193121"
---
# <span data-ttu-id="d3b5c-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d3b5c-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="d3b5c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b5c-103">Sospende un pool SQL di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d3b5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3b5c-104">SYNTAX</span></span>

### <span data-ttu-id="d3b5c-105">SuspendByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3b5c-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3b5c-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3b5c-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3b5c-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3b5c-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3b5c-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3b5c-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3b5c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3b5c-109">DESCRIPTION</span></span>
<span data-ttu-id="d3b5c-110">Il cmdlet **Suspend-AzSynapseSqlPool** sospende un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d3b5c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3b5c-111">EXAMPLES</span></span>

### <span data-ttu-id="d3b5c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3b5c-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="d3b5c-113">Questo comando sospende un pool SQL di analisi delle sinapsi di Azure attivo.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d3b5c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3b5c-114">PARAMETERS</span></span>

### <span data-ttu-id="d3b5c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3b5c-115">-AsJob</span></span>
<span data-ttu-id="d3b5c-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d3b5c-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b5c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b5c-117">-DefaultProfile</span></span>
<span data-ttu-id="d3b5c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3b5c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3b5c-119">-InputObject</span></span>
<span data-ttu-id="d3b5c-120">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b5c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3b5c-121">-Name</span></span>
<span data-ttu-id="d3b5c-122">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b5c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3b5c-123">-PassThru</span></span>
<span data-ttu-id="d3b5c-124">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d3b5c-125">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-125">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b5c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3b5c-126">-ResourceGroupName</span></span>
<span data-ttu-id="d3b5c-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b5c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3b5c-128">-ResourceId</span></span>
<span data-ttu-id="d3b5c-129">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b5c-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d3b5c-130">-WorkspaceName</span></span>
<span data-ttu-id="d3b5c-131">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b5c-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d3b5c-132">-WorkspaceObject</span></span>
<span data-ttu-id="d3b5c-133">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b5c-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3b5c-134">-Confirm</span></span>
<span data-ttu-id="d3b5c-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3b5c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3b5c-136">-WhatIf</span></span>
<span data-ttu-id="d3b5c-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3b5c-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3b5c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b5c-139">CommonParameters</span></span>
<span data-ttu-id="d3b5c-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3b5c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b5c-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3b5c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b5c-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3b5c-142">INPUTS</span></span>

### <span data-ttu-id="d3b5c-143">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d3b5c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d3b5c-144">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d3b5c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d3b5c-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3b5c-145">OUTPUTS</span></span>

### <span data-ttu-id="d3b5c-146">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d3b5c-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d3b5c-147">Note</span><span class="sxs-lookup"><span data-stu-id="d3b5c-147">NOTES</span></span>

## <span data-ttu-id="d3b5c-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3b5c-148">RELATED LINKS</span></span>
