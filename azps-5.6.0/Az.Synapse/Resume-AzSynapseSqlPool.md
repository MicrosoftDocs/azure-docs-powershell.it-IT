---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: cfcfb283887e221db02c894f7a7712203e516996
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967150"
---
# <span data-ttu-id="d8e3d-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d8e3d-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="d8e3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e3d-103">Riprendi un pool di SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d8e3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8e3d-104">SYNTAX</span></span>

### <span data-ttu-id="d8e3d-105">ResumeByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8e3d-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8e3d-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8e3d-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8e3d-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8e3d-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8e3d-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8e3d-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8e3d-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d8e3d-109">DESCRIPTION</span></span>
<span data-ttu-id="d8e3d-110">Il cmdlet **Resume-AzSynapseSqlPool** riprende un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d8e3d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8e3d-111">EXAMPLES</span></span>

### <span data-ttu-id="d8e3d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d8e3d-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="d8e3d-113">Questo comando riprende un pool di SQL Azure Synapse Analytics sospeso.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d8e3d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8e3d-114">PARAMETERS</span></span>

### <span data-ttu-id="d8e3d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8e3d-115">-AsJob</span></span>
<span data-ttu-id="d8e3d-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d8e3d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8e3d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e3d-117">-DefaultProfile</span></span>
<span data-ttu-id="d8e3d-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8e3d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e3d-119">-InputObject</span></span>
<span data-ttu-id="d8e3d-120">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e3d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d8e3d-121">-Name</span></span>
<span data-ttu-id="d8e3d-122">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e3d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8e3d-123">-PassThru</span></span>
<span data-ttu-id="d8e3d-124">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d8e3d-125">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d8e3d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e3d-126">-ResourceGroupName</span></span>
<span data-ttu-id="d8e3d-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e3d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8e3d-128">-ResourceId</span></span>
<span data-ttu-id="d8e3d-129">Identificatore di risorsa dell'SQL pool.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e3d-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8e3d-130">-WorkspaceName</span></span>
<span data-ttu-id="d8e3d-131">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e3d-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d8e3d-132">-WorkspaceObject</span></span>
<span data-ttu-id="d8e3d-133">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e3d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8e3d-134">-Confirm</span></span>
<span data-ttu-id="d8e3d-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e3d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e3d-136">-WhatIf</span></span>
<span data-ttu-id="d8e3d-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e3d-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e3d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e3d-139">CommonParameters</span></span>
<span data-ttu-id="d8e3d-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e3d-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d8e3d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e3d-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="d8e3d-142">INPUTS</span></span>

### <span data-ttu-id="d8e3d-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d8e3d-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d8e3d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d8e3d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d8e3d-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8e3d-145">OUTPUTS</span></span>

### <span data-ttu-id="d8e3d-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d8e3d-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d8e3d-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="d8e3d-147">NOTES</span></span>

## <span data-ttu-id="d8e3d-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8e3d-148">RELATED LINKS</span></span>
