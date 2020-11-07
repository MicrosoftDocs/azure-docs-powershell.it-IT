---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 2f08d81820ab28688b645ef3ec6a8f519985585c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684623"
---
# <span data-ttu-id="d0dfe-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d0dfe-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="d0dfe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="d0dfe-103">Ottiene informazioni sulle pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="d0dfe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0dfe-104">SYNTAX</span></span>

### <span data-ttu-id="d0dfe-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0dfe-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0dfe-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d0dfe-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0dfe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0dfe-107">DESCRIPTION</span></span>
<span data-ttu-id="d0dfe-108">Il cmdlet **Get-AzDataFactoryPipeline** ottiene informazioni sulle pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="d0dfe-109">Se specifichi il nome di una pipeline, questo cmdlet ottiene le informazioni sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="d0dfe-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutte le pipeline della data factory.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="d0dfe-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0dfe-111">EXAMPLES</span></span>

### <span data-ttu-id="d0dfe-112">Esempio 1: ottenere informazioni su tutte le pipeline</span><span class="sxs-lookup"><span data-stu-id="d0dfe-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="d0dfe-113">Questo comando consente di ottenere informazioni su tutte le pipeline nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="d0dfe-114">Puoi scegliere uno dei comandi di esempio seguenti.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="d0dfe-115">Il secondo usa un oggetto **DataFactory** come parametro.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="d0dfe-116">Esempio 2: ottenere informazioni su una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="d0dfe-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="d0dfe-117">Questo comando ottiene le informazioni sulla pipeline denominata DPWikisample nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="d0dfe-118">Il comando passa le informazioni al cmdlet Format-List usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d0dfe-119">Questo cmdlet formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="d0dfe-120">Per altre informazioni, digitare `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="d0dfe-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="d0dfe-121">Esempio 3: ottenere le proprietà di una specifica pipeline</span><span class="sxs-lookup"><span data-stu-id="d0dfe-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="d0dfe-122">Questo comando ottiene le informazioni per la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la proprietà **Properties** associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="d0dfe-123">Esempio 4: ottenere le attività per una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="d0dfe-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

<span data-ttu-id="d0dfe-124">Questo comando ottiene le informazioni per la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la proprietà **attività** associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="d0dfe-125">Esempio 5: ottenere le informazioni di runtime per una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="d0dfe-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="d0dfe-126">Questo comando ottiene le informazioni per la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la proprietà **RuntimeInfo** associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="d0dfe-127">Esempio 6: ottenere informazioni sugli input per la prima attività</span><span class="sxs-lookup"><span data-stu-id="d0dfe-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="d0dfe-128">Questo comando ottiene le informazioni per la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la proprietà **attività** associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="d0dfe-129">Il comando Visualizza la proprietà **inputs** del primo elemento della matrice **Activities** usando **Format-List**.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="d0dfe-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0dfe-130">PARAMETERS</span></span>

### <span data-ttu-id="d0dfe-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d0dfe-131">-DataFactory</span></span>
<span data-ttu-id="d0dfe-132">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d0dfe-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d0dfe-133">Questo cmdlet ottiene le pipeline che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0dfe-134">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d0dfe-134">-DataFactoryName</span></span>
<span data-ttu-id="d0dfe-135">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d0dfe-136">Questo cmdlet ottiene le pipeline che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d0dfe-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0dfe-137">-DefaultProfile</span></span>
<span data-ttu-id="d0dfe-138">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d0dfe-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0dfe-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0dfe-139">-Name</span></span>
<span data-ttu-id="d0dfe-140">Specifica il nome della pipeline per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-140">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0dfe-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0dfe-141">-ResourceGroupName</span></span>
<span data-ttu-id="d0dfe-142">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d0dfe-143">Questo cmdlet ottiene le pipeline che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d0dfe-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0dfe-144">CommonParameters</span></span>
<span data-ttu-id="d0dfe-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0dfe-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0dfe-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0dfe-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0dfe-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0dfe-147">INPUTS</span></span>

### <span data-ttu-id="d0dfe-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d0dfe-148">System.String</span></span>

### <span data-ttu-id="d0dfe-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d0dfe-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="d0dfe-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0dfe-150">OUTPUTS</span></span>

### <span data-ttu-id="d0dfe-151">Microsoft. Azure. Commands. datafactories. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="d0dfe-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="d0dfe-152">Note</span><span class="sxs-lookup"><span data-stu-id="d0dfe-152">NOTES</span></span>
* <span data-ttu-id="d0dfe-153">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="d0dfe-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d0dfe-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0dfe-154">RELATED LINKS</span></span>

[<span data-ttu-id="d0dfe-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d0dfe-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="d0dfe-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d0dfe-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="d0dfe-157">Curriculum vitae-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d0dfe-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="d0dfe-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d0dfe-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="d0dfe-159">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d0dfe-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


