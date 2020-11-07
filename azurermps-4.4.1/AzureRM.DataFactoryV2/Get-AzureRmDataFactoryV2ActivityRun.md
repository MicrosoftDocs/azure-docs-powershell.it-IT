---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 2000e489dcb5a0bab384ac0aad8a1ffbe53aba15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688334"
---
# <span data-ttu-id="55642-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="55642-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="55642-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55642-102">SYNOPSIS</span></span>
<span data-ttu-id="55642-103">Ottiene informazioni sulle esecuzioni delle attività per un'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="55642-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55642-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55642-104">SYNTAX</span></span>

### <span data-ttu-id="55642-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55642-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>]
 [[-LinkedServiceName] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="55642-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="55642-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>]
 [[-LinkedServiceName] <String>] [-DataFactory] <PSDataFactory>
```


## <span data-ttu-id="55642-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55642-107">DESCRIPTION</span></span>

<span data-ttu-id="55642-108">Il cmdlet **Get-AzureRmDataFactoryV2ActivityRun** ottiene le informazioni sulle esecuzioni in Azure Data Factory per l'esecuzione della pipeline specificata avvenuta nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="55642-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="55642-109">È inoltre possibile specificare i filtri per il nome dell'attività, il nome del servizio collegato che ha eseguito l'esecuzione e lo stato dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="55642-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="55642-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55642-110">EXAMPLES</span></span>

### <span data-ttu-id="55642-111">Esempio 1: ottenere tutte le attività eseguite per un'esecuzione della pipeline</span><span class="sxs-lookup"><span data-stu-id="55642-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    LinkedServiceName :
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}

```

<span data-ttu-id="55642-112">Questo comando consente di ottenere informazioni dettagliate su tutte le attività eseguite nell'esecuzione della pipeline con ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" che si è verificato tra "2017-09-01" e "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="55642-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="55642-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55642-113">PARAMETERS</span></span>

### <span data-ttu-id="55642-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="55642-114">-ActivityName</span></span>
<span data-ttu-id="55642-115">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="55642-115">The name of the activity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55642-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="55642-116">-DataFactory</span></span>
<span data-ttu-id="55642-117">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="55642-117">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55642-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="55642-118">-DataFactoryName</span></span>
<span data-ttu-id="55642-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="55642-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55642-120">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="55642-120">-LinkedServiceName</span></span>
<span data-ttu-id="55642-121">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="55642-121">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55642-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="55642-122">-PipelineRunId</span></span>
<span data-ttu-id="55642-123">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="55642-123">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55642-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55642-124">-ResourceGroupName</span></span>
<span data-ttu-id="55642-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="55642-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55642-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="55642-126">-RunStartedAfter</span></span>
<span data-ttu-id="55642-127">Il periodo di tempo in cui viene avviata l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="55642-127">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55642-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="55642-128">-RunStartedBefore</span></span>
<span data-ttu-id="55642-129">L'ora in cui è stata avviata l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="55642-129">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55642-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="55642-130">-Status</span></span>
<span data-ttu-id="55642-131">Lo stato dell'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="55642-131">The status of the pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="55642-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55642-132">INPUTS</span></span>

### <span data-ttu-id="55642-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="55642-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="55642-134">System. String</span><span class="sxs-lookup"><span data-stu-id="55642-134">System.String</span></span>


## <span data-ttu-id="55642-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55642-135">OUTPUTS</span></span>

### <span data-ttu-id="55642-136">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="55642-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="55642-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="55642-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>


## <span data-ttu-id="55642-138">Note</span><span class="sxs-lookup"><span data-stu-id="55642-138">NOTES</span></span>

## <span data-ttu-id="55642-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55642-139">RELATED LINKS</span></span>
[<span data-ttu-id="55642-140">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="55642-140">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="55642-141">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="55642-141">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

