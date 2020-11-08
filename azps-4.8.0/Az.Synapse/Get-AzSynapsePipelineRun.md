---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189181"
---
# <span data-ttu-id="3d631-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="3d631-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="3d631-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d631-102">SYNOPSIS</span></span>
<span data-ttu-id="3d631-103">Ottiene informazioni sulle esecuzioni della pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d631-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="3d631-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d631-104">SYNTAX</span></span>

### <span data-ttu-id="3d631-105">GetByNameAndId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d631-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d631-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="3d631-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d631-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="3d631-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d631-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="3d631-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d631-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d631-109">DESCRIPTION</span></span>
<span data-ttu-id="3d631-110">Il comando **Get-AzSynapsePipelineRun** restituisce informazioni sulle esecuzioni per la pipeline specificata.</span><span class="sxs-lookup"><span data-stu-id="3d631-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="3d631-111">Se PipelineRunId è specificato, Mostra i dettagli per l'esecuzione con quell'ID.</span><span class="sxs-lookup"><span data-stu-id="3d631-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="3d631-112">Se PipelineRunId non è specificato, Visualizza le informazioni su tutte le esecuzioni per le pipeline che si verificano tra i valori di RunStartedAfter e RunStartedBefore.</span><span class="sxs-lookup"><span data-stu-id="3d631-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="3d631-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d631-113">EXAMPLES</span></span>

### <span data-ttu-id="3d631-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d631-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="3d631-115">Questo comando consente di ottenere informazioni dettagliate sull'esecuzione della pipeline con ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="3d631-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="3d631-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d631-116">PARAMETERS</span></span>

### <span data-ttu-id="3d631-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d631-117">-DefaultProfile</span></span>
<span data-ttu-id="3d631-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d631-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d631-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="3d631-119">-PipelineName</span></span>
<span data-ttu-id="3d631-120">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d631-120">The pipeline name.</span></span>

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

### <span data-ttu-id="3d631-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="3d631-121">-PipelineRunId</span></span>
<span data-ttu-id="3d631-122">Identificatore di esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d631-122">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="3d631-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="3d631-123">-RunStartedAfter</span></span>
<span data-ttu-id="3d631-124">Intervallo di tempo in cui l'evento di esecuzione è stato aggiornato in formato "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="3d631-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="3d631-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="3d631-125">-RunStartedBefore</span></span>
<span data-ttu-id="3d631-126">Il periodo di tempo in cui l'evento Run è stato aggiornato in formato "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="3d631-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="3d631-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3d631-127">-WorkspaceName</span></span>
<span data-ttu-id="3d631-128">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3d631-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3d631-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3d631-129">-WorkspaceObject</span></span>
<span data-ttu-id="3d631-130">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d631-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3d631-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d631-131">CommonParameters</span></span>
<span data-ttu-id="3d631-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d631-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d631-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d631-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d631-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d631-134">INPUTS</span></span>

### <span data-ttu-id="3d631-135">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3d631-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3d631-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d631-136">OUTPUTS</span></span>

### <span data-ttu-id="3d631-137">Microsoft. Azure. Commands. sinapsi. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="3d631-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="3d631-138">Note</span><span class="sxs-lookup"><span data-stu-id="3d631-138">NOTES</span></span>

## <span data-ttu-id="3d631-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d631-139">RELATED LINKS</span></span>
