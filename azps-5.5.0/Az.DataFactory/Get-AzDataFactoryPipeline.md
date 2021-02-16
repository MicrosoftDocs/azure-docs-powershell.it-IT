---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188647"
---
# <span data-ttu-id="14840-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="14840-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="14840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14840-102">SYNOPSIS</span></span>
<span data-ttu-id="14840-103">Ottiene informazioni sulle pipeline in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="14840-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="14840-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14840-104">SYNTAX</span></span>

### <span data-ttu-id="14840-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="14840-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14840-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="14840-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14840-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14840-107">DESCRIPTION</span></span>
<span data-ttu-id="14840-108">Il **cmdlet Get-AzDataFactoryPipeline** ottiene informazioni sulle pipeline in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="14840-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="14840-109">Se si specifica il nome di una pipeline, questo cmdlet ottiene informazioni sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="14840-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="14840-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutte le pipeline nel data factory.</span><span class="sxs-lookup"><span data-stu-id="14840-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="14840-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14840-111">EXAMPLES</span></span>

### <span data-ttu-id="14840-112">Esempio 1: Ottenere informazioni su tutte le pipeline</span><span class="sxs-lookup"><span data-stu-id="14840-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="14840-113">Questo comando recupera informazioni su tutte le pipeline del data factory denominate WikiADF.</span><span class="sxs-lookup"><span data-stu-id="14840-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="14840-114">È possibile eseguire uno dei comandi di esempio seguenti.</span><span class="sxs-lookup"><span data-stu-id="14840-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="14840-115">Il secondo usa un **oggetto DataFactory** come parametro.</span><span class="sxs-lookup"><span data-stu-id="14840-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="14840-116">Esempio 2: Ottenere informazioni su una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="14840-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="14840-117">Questo comando recupera informazioni sulla pipeline denominata DPWikisample nel data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="14840-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="14840-118">Il comando passa queste informazioni al cmdlet Format-List tramite l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="14840-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="14840-119">Questo cmdlet formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="14840-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="14840-120">Per altre informazioni, digitare `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="14840-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="14840-121">Esempio 3: Ottenere le proprietà per una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="14840-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="14840-122">Questo comando recupera informazioni per la pipeline denominata DPWikisample nel data factory denominato WikiADF e quindi usa la notazione punto standard per visualizzare la proprietà **Properties** associata a tale pipeline.</span><span class="sxs-lookup"><span data-stu-id="14840-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="14840-123">Esempio 4: Ottenere le attività per una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="14840-123">Example 4: Get the activities for a specific pipeline</span></span>
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

<span data-ttu-id="14840-124">Questo comando recupera le informazioni per la pipeline denominata DPWikisample nel data factory denominato  WikiADF e quindi usa la notazione punto standard per visualizzare la proprietà Attività associata a tale pipeline.</span><span class="sxs-lookup"><span data-stu-id="14840-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="14840-125">Esempio 5: Ottenere le informazioni di runtime per una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="14840-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="14840-126">Questo comando recupera informazioni per la pipeline denominata DPWikisample nel data factory denominato WikiADF e quindi usa la notazione punto standard per visualizzare la proprietà **RuntimeInfo** associata a tale pipeline.</span><span class="sxs-lookup"><span data-stu-id="14840-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="14840-127">Esempio 6: Ottenere informazioni sugli input per la prima attività</span><span class="sxs-lookup"><span data-stu-id="14840-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="14840-128">Questo comando recupera le informazioni per la pipeline denominata DPWikisample nel data factory denominato  WikiADF e quindi usa la notazione punto standard per visualizzare la proprietà Attività associata a tale pipeline.</span><span class="sxs-lookup"><span data-stu-id="14840-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="14840-129">Il comando visualizza **la proprietà Inputs** del primo elemento della matrice **Activities** usando **Format-List.**</span><span class="sxs-lookup"><span data-stu-id="14840-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="14840-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14840-130">PARAMETERS</span></span>

### <span data-ttu-id="14840-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="14840-131">-DataFactory</span></span>
<span data-ttu-id="14840-132">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="14840-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="14840-133">Questo cmdlet ottiene pipeline che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="14840-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="14840-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="14840-134">-DataFactoryName</span></span>
<span data-ttu-id="14840-135">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="14840-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="14840-136">Questo cmdlet ottiene pipeline che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="14840-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="14840-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14840-137">-DefaultProfile</span></span>
<span data-ttu-id="14840-138">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="14840-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14840-139">-Name</span><span class="sxs-lookup"><span data-stu-id="14840-139">-Name</span></span>
<span data-ttu-id="14840-140">Specifica il nome della pipeline su cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="14840-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="14840-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14840-141">-ResourceGroupName</span></span>
<span data-ttu-id="14840-142">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="14840-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="14840-143">Questo cmdlet ottiene pipeline che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="14840-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="14840-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14840-144">CommonParameters</span></span>
<span data-ttu-id="14840-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14840-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14840-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14840-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14840-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="14840-147">INPUTS</span></span>

### <span data-ttu-id="14840-148">System.String</span><span class="sxs-lookup"><span data-stu-id="14840-148">System.String</span></span>

### <span data-ttu-id="14840-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="14840-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="14840-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14840-150">OUTPUTS</span></span>

### <span data-ttu-id="14840-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="14840-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="14840-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="14840-152">NOTES</span></span>
* <span data-ttu-id="14840-153">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="14840-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="14840-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14840-154">RELATED LINKS</span></span>

[<span data-ttu-id="14840-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="14840-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="14840-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="14840-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="14840-157">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="14840-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="14840-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="14840-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="14840-159">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="14840-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


