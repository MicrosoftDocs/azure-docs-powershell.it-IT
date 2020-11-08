---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199961"
---
# <span data-ttu-id="5b63a-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="5b63a-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="5b63a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b63a-102">SYNOPSIS</span></span>
<span data-ttu-id="5b63a-103">Richiama una pipeline per avviare una corsa.</span><span class="sxs-lookup"><span data-stu-id="5b63a-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="5b63a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b63a-104">SYNTAX</span></span>

### <span data-ttu-id="5b63a-105">NewByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b63a-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b63a-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="5b63a-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b63a-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="5b63a-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b63a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b63a-108">DESCRIPTION</span></span>
<span data-ttu-id="5b63a-109">Il comando **Invoke-AzSynapsePipeline** avvia un'esecuzione sulla pipeline specificata e restituisce un ID per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5b63a-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="5b63a-110">Questo GUID può essere passato a **Get-AzSynapsePipelineRun** o **Get-AzSynapseActivityRun** per ottenere ulteriori informazioni su questa esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5b63a-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="5b63a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b63a-111">EXAMPLES</span></span>

### <span data-ttu-id="5b63a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5b63a-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="5b63a-113">Questo comando avvia un'esecuzione per pipeline denominata ContosoPipeline nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="5b63a-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="5b63a-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5b63a-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="5b63a-115">Questo comando avvia un'esecuzione per pipeline denominata ContosoPipeline nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b63a-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="5b63a-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5b63a-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="5b63a-117">Questo comando avvia un'esecuzione per pipeline denominata ContosoPipeline nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b63a-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="5b63a-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b63a-118">PARAMETERS</span></span>

### <span data-ttu-id="5b63a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b63a-119">-AsJob</span></span>
<span data-ttu-id="5b63a-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5b63a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b63a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b63a-121">-DefaultProfile</span></span>
<span data-ttu-id="5b63a-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b63a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b63a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b63a-123">-InputObject</span></span>
<span data-ttu-id="5b63a-124">Informazioni sull'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b63a-124">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b63a-125">-Recupero</span><span class="sxs-lookup"><span data-stu-id="5b63a-125">-IsRecovery</span></span>
<span data-ttu-id="5b63a-126">Flag modalità di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5b63a-126">Recovery mode flag.</span></span>
<span data-ttu-id="5b63a-127">Se la modalità di ripristino è impostata su true, l'esecuzione della pipeline di riferimento specificata e la nuova esecuzione verranno raggruppate in base allo stesso groupId.</span><span class="sxs-lookup"><span data-stu-id="5b63a-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="5b63a-128">Parametro-</span><span class="sxs-lookup"><span data-stu-id="5b63a-128">-Parameter</span></span>
<span data-ttu-id="5b63a-129">Parametri per l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b63a-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="5b63a-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="5b63a-130">-ParameterFile</span></span>
<span data-ttu-id="5b63a-131">Nome del file con parametri per l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b63a-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="5b63a-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="5b63a-132">-PipelineName</span></span>
<span data-ttu-id="5b63a-133">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b63a-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName, NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b63a-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="5b63a-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="5b63a-135">ID esecuzione della pipeline per la ripetizione.</span><span class="sxs-lookup"><span data-stu-id="5b63a-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="5b63a-136">Se viene specificato ID esecuzione, verranno usati i parametri dell'esecuzione specificata per creare una nuova esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5b63a-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="5b63a-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="5b63a-137">-StartActivityName</span></span>
<span data-ttu-id="5b63a-138">In modalità di ripristino la ripetizione inizierà da questa attività.</span><span class="sxs-lookup"><span data-stu-id="5b63a-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="5b63a-139">Se non specificato, verranno eseguite tutte le attività.</span><span class="sxs-lookup"><span data-stu-id="5b63a-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="5b63a-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5b63a-140">-WorkspaceName</span></span>
<span data-ttu-id="5b63a-141">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="5b63a-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b63a-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5b63a-142">-WorkspaceObject</span></span>
<span data-ttu-id="5b63a-143">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b63a-143">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b63a-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b63a-144">-Confirm</span></span>
<span data-ttu-id="5b63a-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b63a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b63a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b63a-146">-WhatIf</span></span>
<span data-ttu-id="5b63a-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b63a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b63a-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b63a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b63a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b63a-149">CommonParameters</span></span>
<span data-ttu-id="5b63a-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b63a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b63a-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b63a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b63a-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b63a-152">INPUTS</span></span>

### <span data-ttu-id="5b63a-153">Microsoft. Azure. Commands. sinapsi. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="5b63a-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="5b63a-154">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5b63a-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5b63a-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b63a-155">OUTPUTS</span></span>

### <span data-ttu-id="5b63a-156">Microsoft. Azure. Commands. sinapsi. Models. PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="5b63a-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="5b63a-157">Note</span><span class="sxs-lookup"><span data-stu-id="5b63a-157">NOTES</span></span>

## <span data-ttu-id="5b63a-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b63a-158">RELATED LINKS</span></span>