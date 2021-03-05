---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 68c524f2c8712b0da0600abda2fa8035dd5a979c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975134"
---
# <span data-ttu-id="60aa4-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="60aa4-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="60aa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="60aa4-103">Ottiene informazioni sulle esecuzioni della pipeline.</span><span class="sxs-lookup"><span data-stu-id="60aa4-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="60aa4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60aa4-104">SYNTAX</span></span>

### <span data-ttu-id="60aa4-105">ByFactoryNameByRunId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60aa4-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60aa4-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="60aa4-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60aa4-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="60aa4-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60aa4-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="60aa4-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60aa4-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60aa4-109">DESCRIPTION</span></span>
<span data-ttu-id="60aa4-110">Il **comando Get-AzDataFactoryV2PipelineRun** restituisce informazioni sulle esecuzioni per la pipeline specificata.</span><span class="sxs-lookup"><span data-stu-id="60aa4-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="60aa4-111">Se si specifica PipelineRunId, vengono visualizzati i dettagli per l'esecuzione con tale ID.</span><span class="sxs-lookup"><span data-stu-id="60aa4-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="60aa4-112">Se pipelineRunId non è specificato, visualizza informazioni su tutte le esecuzioni per le pipeline che si sono verificate tra i valori di LastUpdatedAfter e LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="60aa4-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="60aa4-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60aa4-113">EXAMPLES</span></span>

### <span data-ttu-id="60aa4-114">Esempio 1: Ottenere informazioni per l'esecuzione di una pipeline</span><span class="sxs-lookup"><span data-stu-id="60aa4-114">Example 1: Get information for a pipeline run</span></span>
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

<span data-ttu-id="60aa4-115">Questo comando recupera i dettagli sull'esecuzione della pipeline con ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="60aa4-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="60aa4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60aa4-116">PARAMETERS</span></span>

### <span data-ttu-id="60aa4-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="60aa4-117">-DataFactory</span></span>
<span data-ttu-id="60aa4-118">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="60aa4-118">The data factory object.</span></span>

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

### <span data-ttu-id="60aa4-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="60aa4-119">-DataFactoryName</span></span>
<span data-ttu-id="60aa4-120">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="60aa4-120">The data factory name.</span></span>

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

### <span data-ttu-id="60aa4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60aa4-121">-DefaultProfile</span></span>
<span data-ttu-id="60aa4-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60aa4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60aa4-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="60aa4-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="60aa4-124">L'ora in cui o dopo l'esecuzione della pipeline è stata aggiornata nel formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="60aa4-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="60aa4-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="60aa4-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="60aa4-126">L'ora in cui o prima dell'esecuzione della pipeline è stata aggiornata in formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="60aa4-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="60aa4-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="60aa4-127">-PipelineName</span></span>
<span data-ttu-id="60aa4-128">Nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="60aa4-128">The pipeline name.</span></span>

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

### <span data-ttu-id="60aa4-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="60aa4-129">-PipelineRunId</span></span>
<span data-ttu-id="60aa4-130">ID di esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="60aa4-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="60aa4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60aa4-131">-ResourceGroupName</span></span>
<span data-ttu-id="60aa4-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60aa4-132">The resource group name.</span></span>

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

### <span data-ttu-id="60aa4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60aa4-133">CommonParameters</span></span>
<span data-ttu-id="60aa4-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60aa4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60aa4-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60aa4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60aa4-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="60aa4-136">INPUTS</span></span>

### <span data-ttu-id="60aa4-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="60aa4-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="60aa4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="60aa4-138">System.String</span></span>

## <span data-ttu-id="60aa4-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60aa4-139">OUTPUTS</span></span>

### <span data-ttu-id="60aa4-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="60aa4-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="60aa4-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="60aa4-141">NOTES</span></span>

## <span data-ttu-id="60aa4-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60aa4-142">RELATED LINKS</span></span>

[<span data-ttu-id="60aa4-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="60aa4-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="60aa4-144">Get-AzDataActivityV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="60aa4-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

