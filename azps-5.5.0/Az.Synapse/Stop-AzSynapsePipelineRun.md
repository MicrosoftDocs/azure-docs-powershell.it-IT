---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190575"
---
# <span data-ttu-id="7c295-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="7c295-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="7c295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c295-102">SYNOPSIS</span></span>
<span data-ttu-id="7c295-103">Interrompe l'esecuzione di una pipeline in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7c295-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="7c295-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c295-104">SYNTAX</span></span>

### <span data-ttu-id="7c295-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c295-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c295-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="7c295-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c295-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="7c295-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c295-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7c295-108">DESCRIPTION</span></span>
<span data-ttu-id="7c295-109">Il cmdlet **Stop-AzSynapsePipelineRun** interrompe l'esecuzione di una pipeline in un'area di lavoro specificata con l'ID di esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="7c295-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="7c295-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c295-110">EXAMPLES</span></span>

### <span data-ttu-id="7c295-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c295-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="7c295-112">Questo comando interrompe l'esecuzione della pipeline con id b9730a13-aa12-4926-a8b3-8e3a974ab0bd nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7c295-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="7c295-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7c295-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="7c295-114">Questo comando interrompe l'esecuzione della pipeline con id b9730a13-aa12-4926-a8b3-8e3a974ab0bd nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="7c295-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="7c295-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7c295-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="7c295-116">Questo comando interrompe l'esecuzione della pipeline con id b9730a13-aa12-4926-a8b3-8e3a974ab0bd nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="7c295-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7c295-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c295-117">PARAMETERS</span></span>

### <span data-ttu-id="7c295-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c295-118">-AsJob</span></span>
<span data-ttu-id="7c295-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7c295-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c295-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c295-120">-DefaultProfile</span></span>
<span data-ttu-id="7c295-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c295-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c295-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c295-122">-InputObject</span></span>
<span data-ttu-id="7c295-123">Informazioni sulla pipeline di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7c295-123">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c295-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c295-124">-PassThru</span></span>
<span data-ttu-id="7c295-125">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7c295-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7c295-126">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7c295-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7c295-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="7c295-127">-PipelineRunId</span></span>
<span data-ttu-id="7c295-128">Identificatore di esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="7c295-128">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c295-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7c295-129">-WorkspaceName</span></span>
<span data-ttu-id="7c295-130">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="7c295-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c295-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7c295-131">-WorkspaceObject</span></span>
<span data-ttu-id="7c295-132">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="7c295-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c295-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c295-133">-Confirm</span></span>
<span data-ttu-id="7c295-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c295-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c295-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c295-135">-WhatIf</span></span>
<span data-ttu-id="7c295-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c295-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c295-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c295-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c295-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c295-138">CommonParameters</span></span>
<span data-ttu-id="7c295-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c295-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c295-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7c295-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c295-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="7c295-141">INPUTS</span></span>

### <span data-ttu-id="7c295-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7c295-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7c295-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="7c295-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="7c295-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c295-144">OUTPUTS</span></span>

### <span data-ttu-id="7c295-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c295-145">System.Boolean</span></span>

## <span data-ttu-id="7c295-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="7c295-146">NOTES</span></span>

## <span data-ttu-id="7c295-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c295-147">RELATED LINKS</span></span>
