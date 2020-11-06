---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 05adb3533604188aa5331d0d4b3f41a2aeba292d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521062"
---
# <span data-ttu-id="50cc1-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="50cc1-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="50cc1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="50cc1-103">Ottiene informazioni sulle esecuzioni della pipeline.</span><span class="sxs-lookup"><span data-stu-id="50cc1-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50cc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50cc1-104">SYNTAX</span></span>

### <span data-ttu-id="50cc1-105">ByFactoryNameByRunId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50cc1-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50cc1-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="50cc1-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50cc1-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="50cc1-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50cc1-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="50cc1-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50cc1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50cc1-109">DESCRIPTION</span></span>
<span data-ttu-id="50cc1-110">Il comando **Get-AzureRmDataFactoryV2PipelineRun** restituisce informazioni sulle esecuzioni per la pipeline specificata.</span><span class="sxs-lookup"><span data-stu-id="50cc1-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="50cc1-111">Se PipelineRunId è specificato, Mostra i dettagli per l'esecuzione con quell'ID.</span><span class="sxs-lookup"><span data-stu-id="50cc1-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="50cc1-112">Se PipelineRunId non è specificato, Visualizza le informazioni su tutte le esecuzioni per la pipeline specificata che è avvenuta tra i valori di LastUpdatedAfter e LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="50cc1-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="50cc1-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50cc1-113">EXAMPLES</span></span>

### <span data-ttu-id="50cc1-114">Esempio 1: ottenere informazioni per un'esecuzione di pipline</span><span class="sxs-lookup"><span data-stu-id="50cc1-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="50cc1-115">Questo comando consente di ottenere informazioni dettagliate sull'esecuzione della pipeline con ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="50cc1-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="50cc1-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50cc1-116">PARAMETERS</span></span>

### <span data-ttu-id="50cc1-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="50cc1-117">-DataFactory</span></span>
<span data-ttu-id="50cc1-118">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="50cc1-118">The data factory object.</span></span>

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

### <span data-ttu-id="50cc1-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="50cc1-119">-DataFactoryName</span></span>
<span data-ttu-id="50cc1-120">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="50cc1-120">The data factory name.</span></span>

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

### <span data-ttu-id="50cc1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50cc1-121">-DefaultProfile</span></span>
<span data-ttu-id="50cc1-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50cc1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50cc1-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="50cc1-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="50cc1-124">L'ora in o dopo la quale l'esecuzione della pipeline è stata aggiornata in formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="50cc1-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="50cc1-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="50cc1-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="50cc1-126">L'ora in o prima della quale è stata aggiornata l'esecuzione della pipeline in formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="50cc1-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="50cc1-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="50cc1-127">-PipelineName</span></span>
<span data-ttu-id="50cc1-128">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="50cc1-128">The pipeline name.</span></span>

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

### <span data-ttu-id="50cc1-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="50cc1-129">-PipelineRunId</span></span>
<span data-ttu-id="50cc1-130">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="50cc1-130">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50cc1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50cc1-131">-ResourceGroupName</span></span>
<span data-ttu-id="50cc1-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50cc1-132">The resource group name.</span></span>

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

### <span data-ttu-id="50cc1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50cc1-133">CommonParameters</span></span>
<span data-ttu-id="50cc1-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50cc1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50cc1-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50cc1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50cc1-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50cc1-136">INPUTS</span></span>

### <span data-ttu-id="50cc1-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="50cc1-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="50cc1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="50cc1-138">System.String</span></span>

## <span data-ttu-id="50cc1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50cc1-139">OUTPUTS</span></span>

### <span data-ttu-id="50cc1-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="50cc1-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="50cc1-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="50cc1-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="50cc1-142">Note</span><span class="sxs-lookup"><span data-stu-id="50cc1-142">NOTES</span></span>

## <span data-ttu-id="50cc1-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50cc1-143">RELATED LINKS</span></span>

[<span data-ttu-id="50cc1-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="50cc1-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="50cc1-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="50cc1-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

