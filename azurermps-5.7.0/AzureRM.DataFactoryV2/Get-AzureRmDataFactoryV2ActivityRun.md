---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
ms.openlocfilehash: 300aad37f2dede64a4adebc4f1a9d9eb9cc43743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509904"
---
# <span data-ttu-id="22477-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="22477-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="22477-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22477-102">SYNOPSIS</span></span>
<span data-ttu-id="22477-103">Ottiene informazioni sulle esecuzioni delle attività per un'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="22477-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22477-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22477-104">SYNTAX</span></span>

### <span data-ttu-id="22477-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22477-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22477-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="22477-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22477-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22477-107">DESCRIPTION</span></span>
<span data-ttu-id="22477-108">Il cmdlet **Get-AzureRmDataFactoryV2ActivityRun** ottiene le informazioni sulle esecuzioni in Azure Data Factory per l'esecuzione della pipeline specificata avvenuta nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="22477-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="22477-109">È inoltre possibile specificare i filtri per il nome dell'attività, il nome del servizio collegato che ha eseguito l'esecuzione e lo stato dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="22477-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="22477-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22477-110">EXAMPLES</span></span>

### <span data-ttu-id="22477-111">Esempio 1: ottenere tutte le attività eseguite per un'esecuzione della pipeline</span><span class="sxs-lookup"><span data-stu-id="22477-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="22477-112">Questo comando consente di ottenere informazioni dettagliate su tutte le attività eseguite nell'esecuzione della pipeline con ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" che si è verificato tra "2017-09-01" e "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="22477-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="22477-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22477-113">PARAMETERS</span></span>

### <span data-ttu-id="22477-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="22477-114">-ActivityName</span></span>
<span data-ttu-id="22477-115">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="22477-115">The name of the activity.</span></span>

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

### <span data-ttu-id="22477-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="22477-116">-DataFactory</span></span>
<span data-ttu-id="22477-117">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="22477-117">The data factory object.</span></span>

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

### <span data-ttu-id="22477-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="22477-118">-DataFactoryName</span></span>
<span data-ttu-id="22477-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="22477-119">The data factory name.</span></span>

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

### <span data-ttu-id="22477-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22477-120">-DefaultProfile</span></span>
<span data-ttu-id="22477-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22477-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22477-122">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="22477-122">-LinkedServiceName</span></span>
<span data-ttu-id="22477-123">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="22477-123">The linked service name.</span></span>

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

### <span data-ttu-id="22477-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="22477-124">-PipelineRunId</span></span>
<span data-ttu-id="22477-125">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="22477-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="22477-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22477-126">-ResourceGroupName</span></span>
<span data-ttu-id="22477-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22477-127">The resource group name.</span></span>

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

### <span data-ttu-id="22477-128">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="22477-128">-RunStartedAfter</span></span>
<span data-ttu-id="22477-129">Il periodo di tempo in cui viene avviata l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="22477-129">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="22477-130">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="22477-130">-RunStartedBefore</span></span>
<span data-ttu-id="22477-131">L'ora in cui è stata avviata l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="22477-131">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="22477-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="22477-132">-Status</span></span>
<span data-ttu-id="22477-133">Lo stato dell'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="22477-133">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="22477-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22477-134">CommonParameters</span></span>
<span data-ttu-id="22477-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22477-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22477-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22477-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22477-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22477-137">INPUTS</span></span>

### <span data-ttu-id="22477-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="22477-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="22477-139">System. String</span><span class="sxs-lookup"><span data-stu-id="22477-139">System.String</span></span>

## <span data-ttu-id="22477-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22477-140">OUTPUTS</span></span>

### <span data-ttu-id="22477-141">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22477-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="22477-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="22477-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="22477-143">Note</span><span class="sxs-lookup"><span data-stu-id="22477-143">NOTES</span></span>

## <span data-ttu-id="22477-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22477-144">RELATED LINKS</span></span>

[<span data-ttu-id="22477-145">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="22477-145">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="22477-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="22477-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

