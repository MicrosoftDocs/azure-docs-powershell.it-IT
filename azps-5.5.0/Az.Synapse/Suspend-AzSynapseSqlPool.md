---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: f0d06956c15b83511989b0ec5917918773f92293
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208947"
---
# <span data-ttu-id="385a0-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="385a0-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="385a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="385a0-102">SYNOPSIS</span></span>
<span data-ttu-id="385a0-103">Sospende un pool SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="385a0-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="385a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="385a0-104">SYNTAX</span></span>

### <span data-ttu-id="385a0-105">SuspendByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="385a0-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="385a0-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="385a0-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="385a0-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="385a0-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="385a0-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="385a0-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="385a0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="385a0-109">DESCRIPTION</span></span>
<span data-ttu-id="385a0-110">Il cmdlet **Suspend-AzSynapseSqlPool** sospende un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="385a0-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="385a0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="385a0-111">EXAMPLES</span></span>

### <span data-ttu-id="385a0-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="385a0-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="385a0-113">Questo comando sospende un pool di SQL Azure Synapse Analytics attivo.</span><span class="sxs-lookup"><span data-stu-id="385a0-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="385a0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="385a0-114">PARAMETERS</span></span>

### <span data-ttu-id="385a0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="385a0-115">-AsJob</span></span>
<span data-ttu-id="385a0-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="385a0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="385a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385a0-117">-DefaultProfile</span></span>
<span data-ttu-id="385a0-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="385a0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="385a0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="385a0-119">-InputObject</span></span>
<span data-ttu-id="385a0-120">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="385a0-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="385a0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="385a0-121">-Name</span></span>
<span data-ttu-id="385a0-122">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="385a0-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385a0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="385a0-123">-PassThru</span></span>
<span data-ttu-id="385a0-124">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="385a0-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="385a0-125">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="385a0-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="385a0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="385a0-126">-ResourceGroupName</span></span>
<span data-ttu-id="385a0-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="385a0-127">Resource group name.</span></span>

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

### <span data-ttu-id="385a0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="385a0-128">-ResourceId</span></span>
<span data-ttu-id="385a0-129">Identificatore di risorsa dell'SQL pool.</span><span class="sxs-lookup"><span data-stu-id="385a0-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="385a0-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="385a0-130">-WorkspaceName</span></span>
<span data-ttu-id="385a0-131">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="385a0-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="385a0-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="385a0-132">-WorkspaceObject</span></span>
<span data-ttu-id="385a0-133">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="385a0-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="385a0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="385a0-134">-Confirm</span></span>
<span data-ttu-id="385a0-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="385a0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="385a0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="385a0-136">-WhatIf</span></span>
<span data-ttu-id="385a0-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="385a0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="385a0-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="385a0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="385a0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385a0-139">CommonParameters</span></span>
<span data-ttu-id="385a0-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385a0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385a0-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="385a0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385a0-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="385a0-142">INPUTS</span></span>

### <span data-ttu-id="385a0-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="385a0-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="385a0-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="385a0-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="385a0-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="385a0-145">OUTPUTS</span></span>

### <span data-ttu-id="385a0-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="385a0-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="385a0-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="385a0-147">NOTES</span></span>

## <span data-ttu-id="385a0-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="385a0-148">RELATED LINKS</span></span>
