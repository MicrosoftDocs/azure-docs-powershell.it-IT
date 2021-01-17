---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: cdee786d338dce2663bf99916c6b6c2b250e22b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477172"
---
# <span data-ttu-id="263ca-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="263ca-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="263ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="263ca-102">SYNOPSIS</span></span>
<span data-ttu-id="263ca-103">Ottiene informazioni sulle esecuzioni delle attività per un'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="263ca-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="263ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="263ca-104">SYNTAX</span></span>

### <span data-ttu-id="263ca-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="263ca-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="263ca-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="263ca-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="263ca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="263ca-107">DESCRIPTION</span></span>
<span data-ttu-id="263ca-108">Il cmdlet **Get-AzDataFactoryV2ActivityRun** ottiene le informazioni sulle esecuzioni in Azure Data Factory per l'esecuzione della pipeline specificata avvenuta nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="263ca-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="263ca-109">È inoltre possibile specificare i filtri per il nome dell'attività, il nome del servizio collegato che ha eseguito l'esecuzione e lo stato dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="263ca-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="263ca-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="263ca-110">EXAMPLES</span></span>

### <span data-ttu-id="263ca-111">Esempio 1: ottenere tutte le attività eseguite per un'esecuzione della pipeline</span><span class="sxs-lookup"><span data-stu-id="263ca-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="263ca-112">Questo comando consente di ottenere informazioni dettagliate su tutte le attività eseguite nell'esecuzione della pipeline con ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" che si è verificato tra "2017-09-01" e "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="263ca-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="263ca-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="263ca-113">PARAMETERS</span></span>

### <span data-ttu-id="263ca-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="263ca-114">-ActivityName</span></span>
<span data-ttu-id="263ca-115">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="263ca-115">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263ca-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="263ca-116">-DataFactory</span></span>
<span data-ttu-id="263ca-117">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="263ca-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="263ca-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="263ca-118">-DataFactoryName</span></span>
<span data-ttu-id="263ca-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="263ca-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="263ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="263ca-120">-DefaultProfile</span></span>
<span data-ttu-id="263ca-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="263ca-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="263ca-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="263ca-122">-PipelineRunId</span></span>
<span data-ttu-id="263ca-123">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="263ca-123">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263ca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="263ca-124">-ResourceGroupName</span></span>
<span data-ttu-id="263ca-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="263ca-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="263ca-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="263ca-126">-RunStartedAfter</span></span>
<span data-ttu-id="263ca-127">Il periodo di tempo in cui viene avviata l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="263ca-127">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263ca-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="263ca-128">-RunStartedBefore</span></span>
<span data-ttu-id="263ca-129">L'ora in cui è stata avviata l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="263ca-129">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263ca-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="263ca-130">-Status</span></span>
<span data-ttu-id="263ca-131">Lo stato dell'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="263ca-131">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263ca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="263ca-132">CommonParameters</span></span>
<span data-ttu-id="263ca-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="263ca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="263ca-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="263ca-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="263ca-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="263ca-135">INPUTS</span></span>

### <span data-ttu-id="263ca-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="263ca-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="263ca-137">System. String</span><span class="sxs-lookup"><span data-stu-id="263ca-137">System.String</span></span>

## <span data-ttu-id="263ca-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="263ca-138">OUTPUTS</span></span>

### <span data-ttu-id="263ca-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="263ca-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="263ca-140">Note</span><span class="sxs-lookup"><span data-stu-id="263ca-140">NOTES</span></span>

## <span data-ttu-id="263ca-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="263ca-141">RELATED LINKS</span></span>

[<span data-ttu-id="263ca-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="263ca-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="263ca-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="263ca-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

