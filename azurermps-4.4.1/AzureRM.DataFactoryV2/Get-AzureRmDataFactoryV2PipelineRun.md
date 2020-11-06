---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 6042b62bb7c641cef335834645f29d73b3d4c53a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521708"
---
# <span data-ttu-id="355f8-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="355f8-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="355f8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="355f8-102">SYNOPSIS</span></span>
<span data-ttu-id="355f8-103">Ottiene informazioni sulle esecuzioni della pipeline.</span><span class="sxs-lookup"><span data-stu-id="355f8-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="355f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="355f8-104">SYNTAX</span></span>

### <span data-ttu-id="355f8-105">ByFactoryNameByRunId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="355f8-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String>
```

### <span data-ttu-id="355f8-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="355f8-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
```

### <span data-ttu-id="355f8-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="355f8-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
```

### <span data-ttu-id="355f8-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="355f8-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
```

## <span data-ttu-id="355f8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="355f8-109">DESCRIPTION</span></span>
<span data-ttu-id="355f8-110">Il comando **Get-AzureRmDataFactoryV2PipelineRun** restituisce informazioni sulle esecuzioni per la pipeline specificata.</span><span class="sxs-lookup"><span data-stu-id="355f8-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="355f8-111">Se PipelineRunId è specificato, Mostra i dettagli per l'esecuzione con quell'ID.</span><span class="sxs-lookup"><span data-stu-id="355f8-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="355f8-112">Se PipelineRunId non è specificato, Visualizza le informazioni su tutte le esecuzioni per la pipeline specificata che è avvenuta tra i valori di LastUpdatedAfter e LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="355f8-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="355f8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="355f8-113">EXAMPLES</span></span>

### <span data-ttu-id="355f8-114">Esempio 1: ottenere informazioni per un'esecuzione di pipline</span><span class="sxs-lookup"><span data-stu-id="355f8-114">Example 1: Get information for a pipline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    RunId             : 61eb095a-fe23-4591-8a97-fade6c65ca72
    PipelineName      : DPWikisample
    LastUpdated       : 9/14/2017 12:21:02 AM
    Parameters        : {[url, http://adfsamplewebapi.azurewebsites.net/api/execute/sample]}
    RunStart          : 9/14/2017 12:20:54 AM
    RunEnd            : 9/14/2017 12:21:02 AM
    DurationInMs      : 8246
    Status            : Succeeded
    Message           :

```

<span data-ttu-id="355f8-115">Questo comando consente di ottenere informazioni dettagliate sull'esecuzione della pipeline con ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="355f8-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>


## <span data-ttu-id="355f8-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="355f8-116">PARAMETERS</span></span>

### <span data-ttu-id="355f8-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="355f8-117">-DataFactory</span></span>
<span data-ttu-id="355f8-118">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="355f8-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="355f8-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="355f8-119">-DataFactoryName</span></span>
<span data-ttu-id="355f8-120">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="355f8-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="355f8-121">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="355f8-121">-LastUpdatedAfter</span></span>
<span data-ttu-id="355f8-122">L'ora in o dopo la quale l'esecuzione della pipeline è stata aggiornata in formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="355f8-122">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="355f8-123">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="355f8-123">-LastUpdatedBefore</span></span>
<span data-ttu-id="355f8-124">L'ora in o prima della quale è stata aggiornata l'esecuzione della pipeline in formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="355f8-124">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="355f8-125">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="355f8-125">-PipelineName</span></span>
<span data-ttu-id="355f8-126">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="355f8-126">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="355f8-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="355f8-127">-PipelineRunId</span></span>
<span data-ttu-id="355f8-128">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="355f8-128">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByRunId, ByFactoryNameByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="355f8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="355f8-129">-ResourceGroupName</span></span>
<span data-ttu-id="355f8-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="355f8-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="355f8-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="355f8-131">INPUTS</span></span>

### <span data-ttu-id="355f8-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="355f8-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="355f8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="355f8-133">System.String</span></span>


## <span data-ttu-id="355f8-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="355f8-134">OUTPUTS</span></span>

### <span data-ttu-id="355f8-135">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="355f8-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="355f8-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="355f8-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>


## <span data-ttu-id="355f8-137">Note</span><span class="sxs-lookup"><span data-stu-id="355f8-137">NOTES</span></span>

## <span data-ttu-id="355f8-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="355f8-138">RELATED LINKS</span></span>
[<span data-ttu-id="355f8-139">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="355f8-139">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="355f8-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="355f8-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

