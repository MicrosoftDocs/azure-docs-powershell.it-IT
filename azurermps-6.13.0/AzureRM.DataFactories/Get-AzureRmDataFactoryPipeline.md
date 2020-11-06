---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: a22e38e03d1a754823675abbac7a847d91762d54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515436"
---
# <span data-ttu-id="71de2-101">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="71de2-101">Get-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="71de2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71de2-102">SYNOPSIS</span></span>
<span data-ttu-id="71de2-103">Ottiene informazioni sulle pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="71de2-103">Gets information about pipelines in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71de2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71de2-104">SYNTAX</span></span>

### <span data-ttu-id="71de2-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71de2-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71de2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="71de2-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71de2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71de2-107">DESCRIPTION</span></span>
<span data-ttu-id="71de2-108">Il cmdlet **Get-AzureRmDataFactoryPipeline** ottiene informazioni sulle pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="71de2-108">The **Get-AzureRmDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="71de2-109">Se specifichi il nome di una pipeline, questo cmdlet ottiene le informazioni sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="71de2-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="71de2-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutte le pipeline della data factory.</span><span class="sxs-lookup"><span data-stu-id="71de2-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="71de2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71de2-111">EXAMPLES</span></span>

### <span data-ttu-id="71de2-112">Esempio 1: ottenere informazioni su tutte le pipeline</span><span class="sxs-lookup"><span data-stu-id="71de2-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="71de2-113">Questo comando consente di ottenere informazioni su tutte le pipeline nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="71de2-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="71de2-114">Puoi scegliere uno dei comandi di esempio seguenti.</span><span class="sxs-lookup"><span data-stu-id="71de2-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="71de2-115">Il secondo usa un oggetto **DataFactory** come parametro.</span><span class="sxs-lookup"><span data-stu-id="71de2-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="71de2-116">Esempio 2: ottenere informazioni su una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="71de2-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="71de2-117">Questo comando ottiene le informazioni sulla pipeline denominata DPWikisample nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="71de2-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="71de2-118">Il comando passa le informazioni al cmdlet Format-List usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="71de2-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="71de2-119">Questo cmdlet formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="71de2-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="71de2-120">Per altre informazioni, digitare `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="71de2-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="71de2-121">Esempio 3: ottenere le proprietà di una specifica pipeline</span><span class="sxs-lookup"><span data-stu-id="71de2-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="71de2-122">Questo comando ottiene le informazioni per la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la proprietà **Properties** associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="71de2-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="71de2-123">Esempio 4: ottenere le attività per una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="71de2-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
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

<span data-ttu-id="71de2-124">Questo comando ottiene le informazioni per la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la proprietà **attività** associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="71de2-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="71de2-125">Esempio 5: ottenere le informazioni di runtime per una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="71de2-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="71de2-126">Questo comando ottiene le informazioni per la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la proprietà **RuntimeInfo** associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="71de2-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="71de2-127">Esempio 6: ottenere informazioni sugli input per la prima attività</span><span class="sxs-lookup"><span data-stu-id="71de2-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="71de2-128">Questo comando ottiene le informazioni per la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la proprietà **attività** associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="71de2-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="71de2-129">Il comando Visualizza la proprietà **inputs** del primo elemento della matrice **Activities** usando **Format-List**.</span><span class="sxs-lookup"><span data-stu-id="71de2-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="71de2-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71de2-130">PARAMETERS</span></span>

### <span data-ttu-id="71de2-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="71de2-131">-DataFactory</span></span>
<span data-ttu-id="71de2-132">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="71de2-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="71de2-133">Questo cmdlet ottiene le pipeline che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="71de2-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="71de2-134">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="71de2-134">-DataFactoryName</span></span>
<span data-ttu-id="71de2-135">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="71de2-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="71de2-136">Questo cmdlet ottiene le pipeline che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="71de2-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="71de2-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71de2-137">-DefaultProfile</span></span>
<span data-ttu-id="71de2-138">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="71de2-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71de2-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="71de2-139">-Name</span></span>
<span data-ttu-id="71de2-140">Specifica il nome della pipeline per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="71de2-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="71de2-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71de2-141">-ResourceGroupName</span></span>
<span data-ttu-id="71de2-142">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="71de2-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="71de2-143">Questo cmdlet ottiene le pipeline che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="71de2-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="71de2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71de2-144">CommonParameters</span></span>
<span data-ttu-id="71de2-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71de2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71de2-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71de2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71de2-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71de2-147">INPUTS</span></span>

### <span data-ttu-id="71de2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="71de2-148">System.String</span></span>

### <span data-ttu-id="71de2-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="71de2-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="71de2-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71de2-150">OUTPUTS</span></span>

### <span data-ttu-id="71de2-151">Microsoft. Azure. Commands. datafactories. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="71de2-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="71de2-152">Note</span><span class="sxs-lookup"><span data-stu-id="71de2-152">NOTES</span></span>
* <span data-ttu-id="71de2-153">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="71de2-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="71de2-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71de2-154">RELATED LINKS</span></span>

[<span data-ttu-id="71de2-155">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="71de2-155">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="71de2-156">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="71de2-156">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="71de2-157">Curriculum vitae-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="71de2-157">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="71de2-158">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="71de2-158">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="71de2-159">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="71de2-159">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


