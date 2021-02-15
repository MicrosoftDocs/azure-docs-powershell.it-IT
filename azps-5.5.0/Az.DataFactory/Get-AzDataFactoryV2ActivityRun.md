---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: cdee786d338dce2663bf99916c6b6c2b250e22b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200598"
---
# <span data-ttu-id="909ca-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="909ca-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="909ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="909ca-102">SYNOPSIS</span></span>
<span data-ttu-id="909ca-103">Ottiene informazioni sulle attività eseguite per un'esecuzione di pipeline.</span><span class="sxs-lookup"><span data-stu-id="909ca-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="909ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="909ca-104">SYNTAX</span></span>

### <span data-ttu-id="909ca-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="909ca-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="909ca-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="909ca-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="909ca-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="909ca-107">DESCRIPTION</span></span>
<span data-ttu-id="909ca-108">Il cmdlet **Get-AzDataActivityV2ActivityRun** ottiene informazioni sull'esecuzione in Data factory di Azure per l'esecuzione della pipeline specificata nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="909ca-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="909ca-109">Inoltre, è possibile specificare i filtri per il nome dell'attività, il nome del servizio collegato che ha eseguito l'esecuzione e lo stato dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="909ca-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="909ca-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="909ca-110">EXAMPLES</span></span>

### <span data-ttu-id="909ca-111">Esempio 1: Ottenere tutte le attività eseguite per un'esecuzione di una pipeline</span><span class="sxs-lookup"><span data-stu-id="909ca-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="909ca-112">Questo comando ottiene dettagli su tutte le attività eseguite nella pipeline con ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" che si è verificato tra "2017-09-01" e "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="909ca-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="909ca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="909ca-113">PARAMETERS</span></span>

### <span data-ttu-id="909ca-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="909ca-114">-ActivityName</span></span>
<span data-ttu-id="909ca-115">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="909ca-115">The name of the activity.</span></span>

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

### <span data-ttu-id="909ca-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="909ca-116">-DataFactory</span></span>
<span data-ttu-id="909ca-117">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="909ca-117">The data factory object.</span></span>

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

### <span data-ttu-id="909ca-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="909ca-118">-DataFactoryName</span></span>
<span data-ttu-id="909ca-119">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="909ca-119">The data factory name.</span></span>

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

### <span data-ttu-id="909ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="909ca-120">-DefaultProfile</span></span>
<span data-ttu-id="909ca-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="909ca-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="909ca-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="909ca-122">-PipelineRunId</span></span>
<span data-ttu-id="909ca-123">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="909ca-123">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="909ca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="909ca-124">-ResourceGroupName</span></span>
<span data-ttu-id="909ca-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="909ca-125">The resource group name.</span></span>

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

### <span data-ttu-id="909ca-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="909ca-126">-RunStartedAfter</span></span>
<span data-ttu-id="909ca-127">Il tempo in corrispondenza o dopo il quale è iniziata l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="909ca-127">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="909ca-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="909ca-128">-RunStartedBefore</span></span>
<span data-ttu-id="909ca-129">Il tempo in corrispondenza o prima del quale è iniziata l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="909ca-129">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="909ca-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="909ca-130">-Status</span></span>
<span data-ttu-id="909ca-131">Stato dell'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="909ca-131">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="909ca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="909ca-132">CommonParameters</span></span>
<span data-ttu-id="909ca-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="909ca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="909ca-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="909ca-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="909ca-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="909ca-135">INPUTS</span></span>

### <span data-ttu-id="909ca-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="909ca-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="909ca-137">System.String</span><span class="sxs-lookup"><span data-stu-id="909ca-137">System.String</span></span>

## <span data-ttu-id="909ca-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="909ca-138">OUTPUTS</span></span>

### <span data-ttu-id="909ca-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="909ca-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="909ca-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="909ca-140">NOTES</span></span>

## <span data-ttu-id="909ca-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="909ca-141">RELATED LINKS</span></span>

[<span data-ttu-id="909ca-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="909ca-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="909ca-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="909ca-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

