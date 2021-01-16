---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 889cffd16c836c5f895a9eb587c14cfbe66a45b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363142"
---
# <span data-ttu-id="d8dbd-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="d8dbd-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="d8dbd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="d8dbd-103">Ottiene informazioni sulle esecuzioni della pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="d8dbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8dbd-104">SYNTAX</span></span>

### <span data-ttu-id="d8dbd-105">ByFactoryNameByRunId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8dbd-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8dbd-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="d8dbd-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8dbd-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="d8dbd-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8dbd-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="d8dbd-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8dbd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8dbd-109">DESCRIPTION</span></span>
<span data-ttu-id="d8dbd-110">Il comando **Get-AzDataFactoryV2PipelineRun** restituisce informazioni sulle esecuzioni per la pipeline specificata.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="d8dbd-111">Se PipelineRunId è specificato, Mostra i dettagli per l'esecuzione con quell'ID.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="d8dbd-112">Se PipelineRunId non è specificato, Visualizza le informazioni su tutte le esecuzioni per le pipeline che si verificano tra i valori di LastUpdatedAfter e LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="d8dbd-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8dbd-113">EXAMPLES</span></span>

### <span data-ttu-id="d8dbd-114">Esempio 1: ottenere informazioni per un'esecuzione della pipeline</span><span class="sxs-lookup"><span data-stu-id="d8dbd-114">Example 1: Get information for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

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

<span data-ttu-id="d8dbd-115">Questo comando consente di ottenere informazioni dettagliate sull'esecuzione della pipeline con ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="d8dbd-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="d8dbd-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8dbd-116">PARAMETERS</span></span>

### <span data-ttu-id="d8dbd-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d8dbd-117">-DataFactory</span></span>
<span data-ttu-id="d8dbd-118">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-118">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dbd-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d8dbd-119">-DataFactoryName</span></span>
<span data-ttu-id="d8dbd-120">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dbd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8dbd-121">-DefaultProfile</span></span>
<span data-ttu-id="d8dbd-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8dbd-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="d8dbd-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="d8dbd-124">L'ora in o dopo la quale l'esecuzione della pipeline è stata aggiornata in formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dbd-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="d8dbd-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="d8dbd-126">L'ora in o prima della quale è stata aggiornata l'esecuzione della pipeline in formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dbd-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d8dbd-127">-PipelineName</span></span>
<span data-ttu-id="d8dbd-128">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-128">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dbd-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="d8dbd-129">-PipelineRunId</span></span>
<span data-ttu-id="d8dbd-130">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-130">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dbd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8dbd-131">-ResourceGroupName</span></span>
<span data-ttu-id="d8dbd-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dbd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8dbd-133">CommonParameters</span></span>
<span data-ttu-id="d8dbd-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8dbd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8dbd-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8dbd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8dbd-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8dbd-136">INPUTS</span></span>

### <span data-ttu-id="d8dbd-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d8dbd-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="d8dbd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d8dbd-138">System.String</span></span>

## <span data-ttu-id="d8dbd-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8dbd-139">OUTPUTS</span></span>

### <span data-ttu-id="d8dbd-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="d8dbd-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="d8dbd-141">Note</span><span class="sxs-lookup"><span data-stu-id="d8dbd-141">NOTES</span></span>

## <span data-ttu-id="d8dbd-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8dbd-142">RELATED LINKS</span></span>

[<span data-ttu-id="d8dbd-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d8dbd-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="d8dbd-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="d8dbd-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

