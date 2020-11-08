---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189191"
---
# <span data-ttu-id="f645e-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="f645e-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="f645e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f645e-102">SYNOPSIS</span></span>
<span data-ttu-id="f645e-103">Ottiene informazioni sulle esecuzioni delle attività per un'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="f645e-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="f645e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f645e-104">SYNTAX</span></span>

### <span data-ttu-id="f645e-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f645e-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f645e-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="f645e-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f645e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f645e-107">DESCRIPTION</span></span>
<span data-ttu-id="f645e-108">Il cmdlet **Get-AzSynapseActivityRun** ottiene le informazioni sulle esecuzioni nell'area di lavoro per l'esecuzione della pipeline specificata avvenuta nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="f645e-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="f645e-109">È inoltre possibile specificare i filtri per il nome dell'attività e lo stato dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f645e-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="f645e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f645e-110">EXAMPLES</span></span>

### <span data-ttu-id="f645e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f645e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="f645e-112">Questo comando consente di ottenere informazioni dettagliate su tutte le attività eseguite nella pipeline denominata ContosoPipeline Run with ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" che si è verificato tra "2018-09-01T21:00" e "2018-09-30T21:00".</span><span class="sxs-lookup"><span data-stu-id="f645e-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="f645e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f645e-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="f645e-114">Questo comando consente di ottenere informazioni dettagliate su tutte le attività eseguite nella pipeline denominata ContosoPipeline eseguita con ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" che si è verificato tra "2018-09-01T21:00" e "2018-09-30T21:00" tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="f645e-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="f645e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f645e-115">PARAMETERS</span></span>

### <span data-ttu-id="f645e-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="f645e-116">-ActivityName</span></span>
<span data-ttu-id="f645e-117">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="f645e-117">The name of the activity.</span></span>

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

### <span data-ttu-id="f645e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f645e-118">-DefaultProfile</span></span>
<span data-ttu-id="f645e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f645e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f645e-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="f645e-120">-PipelineName</span></span>
<span data-ttu-id="f645e-121">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="f645e-121">The pipeline name.</span></span>

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

### <span data-ttu-id="f645e-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="f645e-122">-PipelineRunId</span></span>
<span data-ttu-id="f645e-123">Identificatore di esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="f645e-123">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="f645e-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="f645e-124">-RunStartedAfter</span></span>
<span data-ttu-id="f645e-125">Intervallo di tempo in cui l'evento di esecuzione è stato aggiornato in formato "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="f645e-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f645e-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="f645e-126">-RunStartedBefore</span></span>
<span data-ttu-id="f645e-127">Il periodo di tempo in cui l'evento Run è stato aggiornato in formato "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="f645e-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f645e-128">-Stato</span><span class="sxs-lookup"><span data-stu-id="f645e-128">-Status</span></span>
<span data-ttu-id="f645e-129">Lo stato dell'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="f645e-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="f645e-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f645e-130">-WorkspaceName</span></span>
<span data-ttu-id="f645e-131">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f645e-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f645e-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f645e-132">-WorkspaceObject</span></span>
<span data-ttu-id="f645e-133">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f645e-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f645e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f645e-134">CommonParameters</span></span>
<span data-ttu-id="f645e-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f645e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f645e-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f645e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f645e-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f645e-137">INPUTS</span></span>

### <span data-ttu-id="f645e-138">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f645e-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f645e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f645e-139">OUTPUTS</span></span>

### <span data-ttu-id="f645e-140">Microsoft. Azure. Commands. sinapsi. Models. PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="f645e-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="f645e-141">Note</span><span class="sxs-lookup"><span data-stu-id="f645e-141">NOTES</span></span>

## <span data-ttu-id="f645e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f645e-142">RELATED LINKS</span></span>
