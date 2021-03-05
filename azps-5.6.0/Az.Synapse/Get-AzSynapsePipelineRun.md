---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 98c0f5ed1dee4c5cd25c69a1a88e596a2f99a7c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990721"
---
# <span data-ttu-id="a0c73-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="a0c73-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="a0c73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0c73-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c73-103">Ottiene informazioni sulle esecuzioni della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a0c73-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="a0c73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0c73-104">SYNTAX</span></span>

### <span data-ttu-id="a0c73-105">GetByNameAndId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0c73-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0c73-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="a0c73-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0c73-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="a0c73-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0c73-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="a0c73-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0c73-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a0c73-109">DESCRIPTION</span></span>
<span data-ttu-id="a0c73-110">Il **comando Get-AzSynapsePipelineRun** restituisce informazioni sulle esecuzioni per la pipeline specificata.</span><span class="sxs-lookup"><span data-stu-id="a0c73-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="a0c73-111">Se si specifica PipelineRunId, vengono visualizzati i dettagli per l'esecuzione con tale ID.</span><span class="sxs-lookup"><span data-stu-id="a0c73-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="a0c73-112">Se pipelineRunId non è specificato, visualizza informazioni su tutte le esecuzioni per le pipeline che si sono verificate tra i valori di RunStartedAfter e RunStartedBefore.</span><span class="sxs-lookup"><span data-stu-id="a0c73-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="a0c73-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0c73-113">EXAMPLES</span></span>

### <span data-ttu-id="a0c73-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0c73-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="a0c73-115">Questo comando recupera i dettagli sull'esecuzione della pipeline con ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="a0c73-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="a0c73-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0c73-116">PARAMETERS</span></span>

### <span data-ttu-id="a0c73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c73-117">-DefaultProfile</span></span>
<span data-ttu-id="a0c73-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0c73-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0c73-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="a0c73-119">-PipelineName</span></span>
<span data-ttu-id="a0c73-120">Nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a0c73-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c73-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a0c73-121">-PipelineRunId</span></span>
<span data-ttu-id="a0c73-122">Identificatore di esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a0c73-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c73-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="a0c73-123">-RunStartedAfter</span></span>
<span data-ttu-id="a0c73-124">L'ora in cui l'evento di esecuzione è stato aggiornato nel formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="a0c73-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c73-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="a0c73-125">-RunStartedBefore</span></span>
<span data-ttu-id="a0c73-126">L'ora in cui l'evento di esecuzione è stato aggiornato nel formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="a0c73-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c73-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a0c73-127">-WorkspaceName</span></span>
<span data-ttu-id="a0c73-128">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="a0c73-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c73-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a0c73-129">-WorkspaceObject</span></span>
<span data-ttu-id="a0c73-130">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a0c73-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0c73-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c73-131">CommonParameters</span></span>
<span data-ttu-id="a0c73-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0c73-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c73-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a0c73-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c73-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="a0c73-134">INPUTS</span></span>

### <span data-ttu-id="a0c73-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a0c73-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a0c73-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0c73-136">OUTPUTS</span></span>

### <span data-ttu-id="a0c73-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="a0c73-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="a0c73-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="a0c73-138">NOTES</span></span>

## <span data-ttu-id="a0c73-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0c73-139">RELATED LINKS</span></span>
