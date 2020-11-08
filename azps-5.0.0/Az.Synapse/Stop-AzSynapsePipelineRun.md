---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200062"
---
# <span data-ttu-id="e02f3-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="e02f3-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="e02f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e02f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e02f3-103">Interrompe l'esecuzione di una pipeline in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e02f3-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="e02f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e02f3-104">SYNTAX</span></span>

### <span data-ttu-id="e02f3-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e02f3-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e02f3-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="e02f3-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e02f3-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e02f3-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e02f3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e02f3-108">DESCRIPTION</span></span>
<span data-ttu-id="e02f3-109">Il cmdlet **Stop-AzSynapsePipelineRun** interrompe l'esecuzione di una pipeline in un'area di lavoro specificata con l'ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="e02f3-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="e02f3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e02f3-110">EXAMPLES</span></span>

### <span data-ttu-id="e02f3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e02f3-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="e02f3-112">Questo comando interrompe l'esecuzione della pipeline con ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e02f3-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e02f3-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e02f3-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="e02f3-114">Questo comando interrompe l'esecuzione della pipeline con ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="e02f3-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="e02f3-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e02f3-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="e02f3-116">Questo comando interrompe l'esecuzione della pipeline con ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="e02f3-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e02f3-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e02f3-117">PARAMETERS</span></span>

### <span data-ttu-id="e02f3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e02f3-118">-AsJob</span></span>
<span data-ttu-id="e02f3-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e02f3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e02f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02f3-120">-DefaultProfile</span></span>
<span data-ttu-id="e02f3-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e02f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e02f3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e02f3-122">-InputObject</span></span>
<span data-ttu-id="e02f3-123">Informazioni sull'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="e02f3-123">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="e02f3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e02f3-124">-PassThru</span></span>
<span data-ttu-id="e02f3-125">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e02f3-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e02f3-126">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="e02f3-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e02f3-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="e02f3-127">-PipelineRunId</span></span>
<span data-ttu-id="e02f3-128">Identificatore di esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="e02f3-128">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="e02f3-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e02f3-129">-WorkspaceName</span></span>
<span data-ttu-id="e02f3-130">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e02f3-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e02f3-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e02f3-131">-WorkspaceObject</span></span>
<span data-ttu-id="e02f3-132">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="e02f3-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e02f3-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e02f3-133">-Confirm</span></span>
<span data-ttu-id="e02f3-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e02f3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e02f3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e02f3-135">-WhatIf</span></span>
<span data-ttu-id="e02f3-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e02f3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e02f3-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e02f3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e02f3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02f3-138">CommonParameters</span></span>
<span data-ttu-id="e02f3-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02f3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02f3-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e02f3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02f3-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e02f3-141">INPUTS</span></span>

### <span data-ttu-id="e02f3-142">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e02f3-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e02f3-143">Microsoft. Azure. Commands. sinapsi. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="e02f3-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="e02f3-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e02f3-144">OUTPUTS</span></span>

### <span data-ttu-id="e02f3-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e02f3-145">System.Boolean</span></span>

## <span data-ttu-id="e02f3-146">Note</span><span class="sxs-lookup"><span data-stu-id="e02f3-146">NOTES</span></span>

## <span data-ttu-id="e02f3-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e02f3-147">RELATED LINKS</span></span>
