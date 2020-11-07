---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: bff3a3910393a3708e416396fa21573adadebc60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686432"
---
# <span data-ttu-id="90d6e-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="90d6e-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="90d6e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="90d6e-103">Ottiene informazioni sulle pipeline in data factory.</span><span class="sxs-lookup"><span data-stu-id="90d6e-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90d6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90d6e-104">SYNTAX</span></span>

### <span data-ttu-id="90d6e-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="90d6e-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d6e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="90d6e-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d6e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="90d6e-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90d6e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90d6e-108">DESCRIPTION</span></span>
<span data-ttu-id="90d6e-109">Il cmdlet Get-AzureRmDataFactoryV2Pipeline ottiene informazioni sulle pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="90d6e-109">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="90d6e-110">Se specifichi il nome di una pipeline, questo cmdlet ottiene le informazioni sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="90d6e-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="90d6e-111">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutte le pipeline della data factory.</span><span class="sxs-lookup"><span data-stu-id="90d6e-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="90d6e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90d6e-112">EXAMPLES</span></span>

### <span data-ttu-id="90d6e-113">Esempio 1: ottenere informazioni su tutte le pipeline</span><span class="sxs-lookup"><span data-stu-id="90d6e-113">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="90d6e-114">Questo comando consente di ottenere informazioni su tutte le pipeline nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="90d6e-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="90d6e-115">Puoi usare uno dei comandi di esempio seguenti.</span><span class="sxs-lookup"><span data-stu-id="90d6e-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="90d6e-116">Il secondo usa un oggetto DataFactory come parametro.</span><span class="sxs-lookup"><span data-stu-id="90d6e-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="90d6e-117">Esempio 2: ottenere informazioni su una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="90d6e-117">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="90d6e-118">Questo comando ottiene le informazioni sulla pipeline denominata DPWikisample nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="90d6e-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="90d6e-119">Il comando passa le informazioni al cmdlet Format-List usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="90d6e-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="90d6e-120">Il cmdlet di Windows PowerShell formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="90d6e-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="90d6e-121">Per altre informazioni, digitare Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="90d6e-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="90d6e-122">Esempio 3: ottenere le proprietà di una specifica pipeline</span><span class="sxs-lookup"><span data-stu-id="90d6e-122">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}
```

<span data-ttu-id="90d6e-123">Questo comando ottiene le informazioni per la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la proprietà attività associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="90d6e-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="90d6e-124">Esempio 6: ottenere informazioni sugli input per la prima attività</span><span class="sxs-lookup"><span data-stu-id="90d6e-124">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="90d6e-125">Questo comando ottiene le informazioni per la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la proprietà attività associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="90d6e-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="90d6e-126">Il comando Visualizza la proprietà inputs del primo elemento della matrice Activities usando il cmdlet Format-List.</span><span class="sxs-lookup"><span data-stu-id="90d6e-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="90d6e-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90d6e-127">PARAMETERS</span></span>

### <span data-ttu-id="90d6e-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="90d6e-128">-DataFactory</span></span>
<span data-ttu-id="90d6e-129">Specifica un oggetto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="90d6e-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="90d6e-130">Questo cmdlet ottiene le pipeline che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="90d6e-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90d6e-131">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="90d6e-131">-DataFactoryName</span></span>
<span data-ttu-id="90d6e-132">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="90d6e-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="90d6e-133">Questo cmdlet ottiene le pipeline che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="90d6e-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="90d6e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d6e-134">-DefaultProfile</span></span>
<span data-ttu-id="90d6e-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90d6e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90d6e-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="90d6e-136">-Name</span></span>
<span data-ttu-id="90d6e-137">Specifica il nome della pipeline per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="90d6e-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d6e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90d6e-138">-ResourceGroupName</span></span>
<span data-ttu-id="90d6e-139">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="90d6e-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="90d6e-140">Questo cmdlet ottiene le pipeline che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="90d6e-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="90d6e-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90d6e-141">-ResourceId</span></span>
<span data-ttu-id="90d6e-142">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="90d6e-142">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d6e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d6e-143">CommonParameters</span></span>
<span data-ttu-id="90d6e-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d6e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d6e-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90d6e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d6e-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90d6e-146">INPUTS</span></span>

### <span data-ttu-id="90d6e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="90d6e-147">System.String</span></span>

### <span data-ttu-id="90d6e-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="90d6e-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="90d6e-149">Parametri: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="90d6e-149">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="90d6e-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90d6e-150">OUTPUTS</span></span>

### <span data-ttu-id="90d6e-151">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="90d6e-151">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="90d6e-152">Note</span><span class="sxs-lookup"><span data-stu-id="90d6e-152">NOTES</span></span>
<span data-ttu-id="90d6e-153">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="90d6e-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="90d6e-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90d6e-154">RELATED LINKS</span></span>

[<span data-ttu-id="90d6e-155">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="90d6e-155">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="90d6e-156">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="90d6e-156">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="90d6e-157">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="90d6e-157">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
