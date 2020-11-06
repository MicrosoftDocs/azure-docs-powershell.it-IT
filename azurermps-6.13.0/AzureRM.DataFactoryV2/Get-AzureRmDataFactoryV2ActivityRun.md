---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
ms.openlocfilehash: 4bfebac1d37dbdc0cac2bc8262993a6c81b0c9ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515427"
---
# <span data-ttu-id="ff32a-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="ff32a-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="ff32a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff32a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff32a-103">Ottiene informazioni sulle esecuzioni delle attività per un'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="ff32a-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff32a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff32a-104">SYNTAX</span></span>

### <span data-ttu-id="ff32a-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff32a-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff32a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ff32a-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff32a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff32a-107">DESCRIPTION</span></span>
<span data-ttu-id="ff32a-108">Il cmdlet **Get-AzureRmDataFactoryV2ActivityRun** ottiene le informazioni sulle esecuzioni in Azure Data Factory per l'esecuzione della pipeline specificata avvenuta nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="ff32a-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="ff32a-109">È inoltre possibile specificare i filtri per il nome dell'attività, il nome del servizio collegato che ha eseguito l'esecuzione e lo stato dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ff32a-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="ff32a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff32a-110">EXAMPLES</span></span>

### <span data-ttu-id="ff32a-111">Esempio 1: ottenere tutte le attività eseguite per un'esecuzione della pipeline</span><span class="sxs-lookup"><span data-stu-id="ff32a-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="ff32a-112">Questo comando consente di ottenere informazioni dettagliate su tutte le attività eseguite nell'esecuzione della pipeline con ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" che si è verificato tra "2017-09-01" e "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="ff32a-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="ff32a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff32a-113">PARAMETERS</span></span>

### <span data-ttu-id="ff32a-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="ff32a-114">-ActivityName</span></span>
<span data-ttu-id="ff32a-115">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="ff32a-115">The name of the activity.</span></span>

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

### <span data-ttu-id="ff32a-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff32a-116">-DataFactory</span></span>
<span data-ttu-id="ff32a-117">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ff32a-117">The data factory object.</span></span>

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

### <span data-ttu-id="ff32a-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ff32a-118">-DataFactoryName</span></span>
<span data-ttu-id="ff32a-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="ff32a-119">The data factory name.</span></span>

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

### <span data-ttu-id="ff32a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff32a-120">-DefaultProfile</span></span>
<span data-ttu-id="ff32a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff32a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff32a-122">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="ff32a-122">-LinkedServiceName</span></span>
<span data-ttu-id="ff32a-123">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="ff32a-123">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff32a-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="ff32a-124">-PipelineRunId</span></span>
<span data-ttu-id="ff32a-125">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="ff32a-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="ff32a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff32a-126">-ResourceGroupName</span></span>
<span data-ttu-id="ff32a-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ff32a-127">The resource group name.</span></span>

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

### <span data-ttu-id="ff32a-128">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="ff32a-128">-RunStartedAfter</span></span>
<span data-ttu-id="ff32a-129">Il periodo di tempo in cui viene avviata l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="ff32a-129">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="ff32a-130">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="ff32a-130">-RunStartedBefore</span></span>
<span data-ttu-id="ff32a-131">L'ora in cui è stata avviata l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="ff32a-131">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="ff32a-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="ff32a-132">-Status</span></span>
<span data-ttu-id="ff32a-133">Lo stato dell'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="ff32a-133">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="ff32a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff32a-134">CommonParameters</span></span>
<span data-ttu-id="ff32a-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff32a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff32a-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff32a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff32a-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff32a-137">INPUTS</span></span>

### <span data-ttu-id="ff32a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ff32a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="ff32a-139">Parametri: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff32a-139">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="ff32a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ff32a-140">System.String</span></span>

## <span data-ttu-id="ff32a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff32a-141">OUTPUTS</span></span>

### <span data-ttu-id="ff32a-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="ff32a-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="ff32a-143">Note</span><span class="sxs-lookup"><span data-stu-id="ff32a-143">NOTES</span></span>

## <span data-ttu-id="ff32a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff32a-144">RELATED LINKS</span></span>

[<span data-ttu-id="ff32a-145">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ff32a-145">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="ff32a-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="ff32a-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

