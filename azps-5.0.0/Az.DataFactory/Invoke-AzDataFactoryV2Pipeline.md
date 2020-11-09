---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298465"
---
# <span data-ttu-id="5a90a-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5a90a-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="5a90a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a90a-102">SYNOPSIS</span></span>
  <span data-ttu-id="5a90a-103">Richiama una pipeline per avviare una corsa.</span><span class="sxs-lookup"><span data-stu-id="5a90a-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="5a90a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a90a-104">SYNTAX</span></span>

### <span data-ttu-id="5a90a-105">ByFactoryNameByParameterFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a90a-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a90a-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="5a90a-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a90a-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="5a90a-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a90a-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="5a90a-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a90a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a90a-109">DESCRIPTION</span></span>
<span data-ttu-id="5a90a-110">Il comando **Invoke-AzDataFactoryV2Pipeline** avvia un'esecuzione sulla pipeline specificata e restituisce un ID per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5a90a-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="5a90a-111">Questo GUID può essere passato a **Get-AzDataFactoryV2PipelineRun** o **Get-AzDataFactoryV2ActivityRun** per ottenere ulteriori informazioni su questa esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5a90a-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="5a90a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a90a-112">EXAMPLES</span></span>

### <span data-ttu-id="5a90a-113">Esempio 1: richiamare una pipeline per avviare un'esecuzione</span><span class="sxs-lookup"><span data-stu-id="5a90a-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="5a90a-114">Questo comando avvia una pipeline di esecuzione "DPWikisample" nella Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="5a90a-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="5a90a-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5a90a-115">Example 2</span></span>

<span data-ttu-id="5a90a-116">Richiama una pipeline per avviare una corsa.</span><span class="sxs-lookup"><span data-stu-id="5a90a-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="5a90a-117">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="5a90a-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="5a90a-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a90a-118">PARAMETERS</span></span>

### <span data-ttu-id="5a90a-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5a90a-119">-DataFactoryName</span></span>
<span data-ttu-id="5a90a-120">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="5a90a-120">The data factory name.</span></span>

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

### <span data-ttu-id="5a90a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a90a-121">-DefaultProfile</span></span>
<span data-ttu-id="5a90a-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a90a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a90a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a90a-123">-InputObject</span></span>
<span data-ttu-id="5a90a-124">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5a90a-124">The data factory object.</span></span>

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

### <span data-ttu-id="5a90a-125">-Recupero</span><span class="sxs-lookup"><span data-stu-id="5a90a-125">-IsRecovery</span></span>
<span data-ttu-id="5a90a-126">Flag modalità di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5a90a-126">Recovery mode flag.</span></span> <span data-ttu-id="5a90a-127">Se la modalità di ripristino è impostata su true, l'esecuzione della pipeline di riferimento specificata e la nuova esecuzione verranno raggruppate in base allo stesso groupId.</span><span class="sxs-lookup"><span data-stu-id="5a90a-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a90a-128">Parametro-</span><span class="sxs-lookup"><span data-stu-id="5a90a-128">-Parameter</span></span>
<span data-ttu-id="5a90a-129">Parametri per l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a90a-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="5a90a-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="5a90a-130">-ParameterFile</span></span>
<span data-ttu-id="5a90a-131">Nome del file con parametri per l'esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a90a-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="5a90a-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="5a90a-132">-PipelineName</span></span>
<span data-ttu-id="5a90a-133">Il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a90a-133">The pipeline name.</span></span>

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

### <span data-ttu-id="5a90a-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="5a90a-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="5a90a-135">ID esecuzione della pipeline per la ripetizione.</span><span class="sxs-lookup"><span data-stu-id="5a90a-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="5a90a-136">Se viene specificato ID esecuzione, verranno usati i parametri dell'esecuzione specificata per creare una nuova esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5a90a-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a90a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a90a-137">-ResourceGroupName</span></span>
<span data-ttu-id="5a90a-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5a90a-138">The resource group name.</span></span>

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

### <span data-ttu-id="5a90a-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="5a90a-139">-StartActivityName</span></span>
<span data-ttu-id="5a90a-140">In modalità di ripristino la ripetizione inizierà da questa attività.</span><span class="sxs-lookup"><span data-stu-id="5a90a-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="5a90a-141">Se non specificato, verranno eseguite tutte le attività.</span><span class="sxs-lookup"><span data-stu-id="5a90a-141">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a90a-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="5a90a-142">-StartFromFailure</span></span>
<span data-ttu-id="5a90a-143">Avviare la ripetizione da flag attività non riuscite.</span><span class="sxs-lookup"><span data-stu-id="5a90a-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="5a90a-144">In modalità di ripristino, se specificato, la ripetizione inizierà da attività non riuscite.</span><span class="sxs-lookup"><span data-stu-id="5a90a-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a90a-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5a90a-145">-Confirm</span></span>
<span data-ttu-id="5a90a-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a90a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a90a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a90a-147">-WhatIf</span></span>
<span data-ttu-id="5a90a-148">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a90a-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5a90a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a90a-149">CommonParameters</span></span>
<span data-ttu-id="5a90a-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a90a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a90a-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a90a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a90a-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a90a-152">INPUTS</span></span>

### <span data-ttu-id="5a90a-153">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="5a90a-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="5a90a-154">System. String</span><span class="sxs-lookup"><span data-stu-id="5a90a-154">System.String</span></span>

### <span data-ttu-id="5a90a-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5a90a-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5a90a-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a90a-156">OUTPUTS</span></span>

### <span data-ttu-id="5a90a-157">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="5a90a-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="5a90a-158">Note</span><span class="sxs-lookup"><span data-stu-id="5a90a-158">NOTES</span></span>

## <span data-ttu-id="5a90a-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a90a-159">RELATED LINKS</span></span>

[<span data-ttu-id="5a90a-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="5a90a-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="5a90a-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="5a90a-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

