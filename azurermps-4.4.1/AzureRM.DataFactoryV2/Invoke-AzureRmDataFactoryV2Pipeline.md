---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 45095fefa0d4866a40b59c61ca02a98c118cf37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687536"
---
# <span data-ttu-id="27aee-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="27aee-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="27aee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27aee-102">SYNOPSIS</span></span>
  <span data-ttu-id="27aee-103">Richiama una pipeline per avviare una corsa.</span><span class="sxs-lookup"><span data-stu-id="27aee-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27aee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27aee-104">SYNTAX</span></span>

### <span data-ttu-id="27aee-105">ByFactoryNameByParameterFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27aee-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="27aee-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="27aee-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="27aee-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="27aee-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="27aee-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="27aee-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="27aee-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27aee-109">DESCRIPTION</span></span>
<span data-ttu-id="27aee-110">Il comando **Invoke-AzureRmDataFactoryV2Pipeline** avvia un'esecuzione sulla pipeline specificata e restituisce un ID per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="27aee-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="27aee-111">Questo GUID può essere passato a **Get-AzureRmDataFactoryV2PipelineRun** o **Get-AzureRmDataFactoryV2ActivityRun** per ottenere ulteriori informazioni su questa esecuzione.</span><span class="sxs-lookup"><span data-stu-id="27aee-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="27aee-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27aee-112">EXAMPLES</span></span>

### <span data-ttu-id="27aee-113">Esempio 1: richiamare una pipeline per avviare un'esecuzione</span><span class="sxs-lookup"><span data-stu-id="27aee-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="27aee-114">Questo comando avvia una pipeline di esecuzione "DPWikisample" nella Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="27aee-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="27aee-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27aee-115">PARAMETERS</span></span>

### <span data-ttu-id="27aee-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27aee-116">-Confirm</span></span>
<span data-ttu-id="27aee-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27aee-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27aee-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="27aee-118">-DataFactoryName</span></span>
<span data-ttu-id="27aee-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="27aee-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27aee-120">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="27aee-120">-ParameterFile</span></span>
<span data-ttu-id="27aee-121">Nome del file con parametri per l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="27aee-121">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27aee-122">Parametro-</span><span class="sxs-lookup"><span data-stu-id="27aee-122">-Parameter</span></span>
<span data-ttu-id="27aee-123">Parametri per l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="27aee-123">Parameters for pipeline run.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27aee-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27aee-124">-InputObject</span></span>
<span data-ttu-id="27aee-125">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="27aee-125">The data factory object.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27aee-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="27aee-126">-PipelineName</span></span>
<span data-ttu-id="27aee-127">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="27aee-127">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27aee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27aee-128">-ResourceGroupName</span></span>
<span data-ttu-id="27aee-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27aee-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27aee-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27aee-130">-WhatIf</span></span>
<span data-ttu-id="27aee-131">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27aee-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="27aee-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27aee-132">INPUTS</span></span>

### <span data-ttu-id="27aee-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="27aee-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="27aee-134">System. String System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="27aee-134">System.String System.Collections.Hashtable</span></span>


## <span data-ttu-id="27aee-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27aee-135">OUTPUTS</span></span>

### <span data-ttu-id="27aee-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="27aee-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="27aee-137">Note</span><span class="sxs-lookup"><span data-stu-id="27aee-137">NOTES</span></span>

## <span data-ttu-id="27aee-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27aee-138">RELATED LINKS</span></span>
[<span data-ttu-id="27aee-139">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="27aee-139">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="27aee-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="27aee-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

