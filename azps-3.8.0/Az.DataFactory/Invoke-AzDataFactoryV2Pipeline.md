---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 87d4cfadd183a6aa2652b86336b4dc8d089936fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865305"
---
# <span data-ttu-id="1ef57-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1ef57-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="1ef57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ef57-102">SYNOPSIS</span></span>
  <span data-ttu-id="1ef57-103">Richiama una pipeline per avviare una corsa.</span><span class="sxs-lookup"><span data-stu-id="1ef57-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="1ef57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ef57-104">SYNTAX</span></span>

### <span data-ttu-id="1ef57-105">ByFactoryNameByParameterFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ef57-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef57-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="1ef57-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef57-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="1ef57-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef57-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="1ef57-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ef57-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ef57-109">DESCRIPTION</span></span>
<span data-ttu-id="1ef57-110">Il comando **Invoke-AzDataFactoryV2Pipeline** avvia un'esecuzione sulla pipeline specificata e restituisce un ID per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1ef57-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="1ef57-111">Questo GUID può essere passato a **Get-AzDataFactoryV2PipelineRun** o **Get-AzDataFactoryV2ActivityRun** per ottenere ulteriori informazioni su questa esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1ef57-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="1ef57-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ef57-112">EXAMPLES</span></span>

### <span data-ttu-id="1ef57-113">Esempio 1: richiamare una pipeline per avviare un'esecuzione</span><span class="sxs-lookup"><span data-stu-id="1ef57-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="1ef57-114">Questo comando avvia una pipeline di esecuzione "DPWikisample" nella Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="1ef57-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="1ef57-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ef57-115">PARAMETERS</span></span>

### <span data-ttu-id="1ef57-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1ef57-116">-DataFactoryName</span></span>
<span data-ttu-id="1ef57-117">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="1ef57-117">The data factory name.</span></span>

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

### <span data-ttu-id="1ef57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef57-118">-DefaultProfile</span></span>
<span data-ttu-id="1ef57-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef57-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ef57-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ef57-120">-InputObject</span></span>
<span data-ttu-id="1ef57-121">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1ef57-121">The data factory object.</span></span>

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

### <span data-ttu-id="1ef57-122">Parametro-</span><span class="sxs-lookup"><span data-stu-id="1ef57-122">-Parameter</span></span>
<span data-ttu-id="1ef57-123">Parametri per l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="1ef57-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="1ef57-124">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="1ef57-124">-ParameterFile</span></span>
<span data-ttu-id="1ef57-125">Nome del file con parametri per l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="1ef57-125">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="1ef57-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="1ef57-126">-PipelineName</span></span>
<span data-ttu-id="1ef57-127">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="1ef57-127">The pipeline name.</span></span>

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

### <span data-ttu-id="1ef57-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ef57-128">-ResourceGroupName</span></span>
<span data-ttu-id="1ef57-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1ef57-129">The resource group name.</span></span>

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

### <span data-ttu-id="1ef57-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1ef57-130">-Confirm</span></span>
<span data-ttu-id="1ef57-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ef57-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ef57-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ef57-132">-WhatIf</span></span>
<span data-ttu-id="1ef57-133">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ef57-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1ef57-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef57-134">CommonParameters</span></span>
<span data-ttu-id="1ef57-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ef57-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef57-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ef57-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef57-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ef57-137">INPUTS</span></span>

### <span data-ttu-id="1ef57-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1ef57-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="1ef57-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1ef57-139">System.String</span></span>

### <span data-ttu-id="1ef57-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1ef57-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1ef57-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ef57-141">OUTPUTS</span></span>

### <span data-ttu-id="1ef57-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1ef57-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="1ef57-143">Note</span><span class="sxs-lookup"><span data-stu-id="1ef57-143">NOTES</span></span>

## <span data-ttu-id="1ef57-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ef57-144">RELATED LINKS</span></span>

[<span data-ttu-id="1ef57-145">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="1ef57-145">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="1ef57-146">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="1ef57-146">Get-AzDataFactoryV2ActivityRun</span></span>]()

