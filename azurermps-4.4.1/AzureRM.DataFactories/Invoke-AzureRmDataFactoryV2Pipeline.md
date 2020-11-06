---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: a7486c3fc50e5c6517022190e05d099329fc6001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516263"
---
# <span data-ttu-id="44569-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="44569-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="44569-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44569-102">SYNOPSIS</span></span>
  <span data-ttu-id="44569-103">Richiama una pipeline per avviare una corsa.</span><span class="sxs-lookup"><span data-stu-id="44569-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44569-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44569-104">SYNTAX</span></span>

### <span data-ttu-id="44569-105">ByFactoryNameByParameterFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44569-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44569-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="44569-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44569-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="44569-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44569-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="44569-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44569-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44569-109">DESCRIPTION</span></span>
<span data-ttu-id="44569-110">Il comando **Invoke-AzureRmDataFactoryV2Pipeline** avvia un'esecuzione sulla pipeline specificata e restituisce un ID per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="44569-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="44569-111">Questo GUID può essere passato a **Get-AzureRmDataFactoryV2PipelineRun** o **Get-AzureRmDataFactoryV2ActivityRun** per ottenere ulteriori informazioni su questa esecuzione.</span><span class="sxs-lookup"><span data-stu-id="44569-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="44569-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44569-112">EXAMPLES</span></span>

### <span data-ttu-id="44569-113">Esempio 1: richiamare una pipeline per avviare un'esecuzione</span><span class="sxs-lookup"><span data-stu-id="44569-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="44569-114">Questo comando avvia una pipeline di esecuzione "DPWikisample" nella Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="44569-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="44569-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44569-115">PARAMETERS</span></span>

### <span data-ttu-id="44569-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44569-116">-Confirm</span></span>
<span data-ttu-id="44569-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44569-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44569-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="44569-118">-DataFactoryName</span></span>
<span data-ttu-id="44569-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="44569-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44569-120">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="44569-120">-ParameterFile</span></span>
<span data-ttu-id="44569-121">Nome del file con parametri per l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="44569-121">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44569-122">Parametro-</span><span class="sxs-lookup"><span data-stu-id="44569-122">-Parameter</span></span>
<span data-ttu-id="44569-123">Parametri per l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="44569-123">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44569-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44569-124">-InputObject</span></span>
<span data-ttu-id="44569-125">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="44569-125">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44569-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="44569-126">-PipelineName</span></span>
<span data-ttu-id="44569-127">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="44569-127">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44569-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44569-128">-ResourceGroupName</span></span>
<span data-ttu-id="44569-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44569-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44569-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44569-130">-WhatIf</span></span>
<span data-ttu-id="44569-131">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44569-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44569-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44569-132">-DefaultProfile</span></span>
<span data-ttu-id="44569-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44569-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44569-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44569-134">CommonParameters</span></span>
<span data-ttu-id="44569-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44569-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44569-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44569-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44569-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44569-137">INPUTS</span></span>

### <span data-ttu-id="44569-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="44569-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="44569-139">System. String System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="44569-139">System.String System.Collections.Hashtable</span></span>

## <span data-ttu-id="44569-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44569-140">OUTPUTS</span></span>

### <span data-ttu-id="44569-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="44569-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="44569-142">Note</span><span class="sxs-lookup"><span data-stu-id="44569-142">NOTES</span></span>

## <span data-ttu-id="44569-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44569-143">RELATED LINKS</span></span>

[<span data-ttu-id="44569-144">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="44569-144">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="44569-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="44569-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

