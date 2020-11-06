---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: e0abd64298d74c52f2081e6d36f42b1ad2dee913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510720"
---
# <span data-ttu-id="6adb1-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="6adb1-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="6adb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6adb1-102">SYNOPSIS</span></span>
<span data-ttu-id="6adb1-103">Ottiene informazioni sulle pipeline in data factory.</span><span class="sxs-lookup"><span data-stu-id="6adb1-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6adb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6adb1-104">SYNTAX</span></span>

### <span data-ttu-id="6adb1-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6adb1-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6adb1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6adb1-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6adb1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6adb1-107">DESCRIPTION</span></span>
<span data-ttu-id="6adb1-108">Il cmdlet Get-AzureRmDataFactoryV2Pipeline ottiene informazioni sulle pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="6adb1-108">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="6adb1-109">Se specifichi il nome di una pipeline, questo cmdlet ottiene le informazioni sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="6adb1-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="6adb1-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutte le pipeline della data factory.</span><span class="sxs-lookup"><span data-stu-id="6adb1-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="6adb1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6adb1-111">EXAMPLES</span></span>

### <span data-ttu-id="6adb1-112">Esempio 1: ottenere informazioni su tutte le pipeline</span><span class="sxs-lookup"><span data-stu-id="6adb1-112">Example 1: Get information about all pipelines</span></span>
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

<span data-ttu-id="6adb1-113">Questo comando consente di ottenere informazioni su tutte le pipeline nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="6adb1-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="6adb1-114">Puoi usare uno dei comandi di esempio seguenti.</span><span class="sxs-lookup"><span data-stu-id="6adb1-114">You can use either one of the following example commands.</span></span>
<span data-ttu-id="6adb1-115">Il secondo usa un oggetto DataFactory come parametro.</span><span class="sxs-lookup"><span data-stu-id="6adb1-115">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="6adb1-116">Esempio 2: ottenere informazioni su una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="6adb1-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="6adb1-117">Questo comando ottiene le informazioni sulla pipeline denominata DPWikisample nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="6adb1-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="6adb1-118">Il comando passa le informazioni al cmdlet Format-List usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="6adb1-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6adb1-119">Il cmdlet di Windows PowerShell formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="6adb1-119">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="6adb1-120">Per altre informazioni, digitare Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="6adb1-120">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="6adb1-121">Esempio 3: ottenere le proprietà di una specifica pipeline</span><span class="sxs-lookup"><span data-stu-id="6adb1-121">Example 3: Get the properties for a specific pipeline</span></span>
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

<span data-ttu-id="6adb1-122">Questo comando ottiene le informazioni per la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la proprietà attività associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="6adb1-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="6adb1-123">Esempio 6: ottenere informazioni sugli input per la prima attività</span><span class="sxs-lookup"><span data-stu-id="6adb1-123">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="6adb1-124">Questo comando ottiene le informazioni per la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la proprietà attività associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="6adb1-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="6adb1-125">Il comando Visualizza la proprietà inputs del primo elemento della matrice Activities usando il cmdlet Format-List.</span><span class="sxs-lookup"><span data-stu-id="6adb1-125">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="6adb1-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6adb1-126">PARAMETERS</span></span>

### <span data-ttu-id="6adb1-127">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6adb1-127">-DataFactory</span></span>
<span data-ttu-id="6adb1-128">Specifica un oggetto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="6adb1-128">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="6adb1-129">Questo cmdlet ottiene le pipeline che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6adb1-129">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6adb1-130">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6adb1-130">-DataFactoryName</span></span>
<span data-ttu-id="6adb1-131">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="6adb1-131">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6adb1-132">Questo cmdlet ottiene le pipeline che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6adb1-132">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6adb1-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="6adb1-133">-Name</span></span>
<span data-ttu-id="6adb1-134">Specifica il nome della pipeline per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="6adb1-134">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6adb1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6adb1-135">-ResourceGroupName</span></span>
<span data-ttu-id="6adb1-136">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="6adb1-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6adb1-137">Questo cmdlet ottiene le pipeline che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6adb1-137">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6adb1-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6adb1-138">-DefaultProfile</span></span>
<span data-ttu-id="6adb1-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6adb1-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6adb1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6adb1-140">CommonParameters</span></span>
<span data-ttu-id="6adb1-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6adb1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6adb1-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6adb1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6adb1-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6adb1-143">INPUTS</span></span>

### <span data-ttu-id="6adb1-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6adb1-144">System.String</span></span>
<span data-ttu-id="6adb1-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6adb1-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="6adb1-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6adb1-146">OUTPUTS</span></span>

### <span data-ttu-id="6adb1-147">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6adb1-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="6adb1-148">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="6adb1-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="6adb1-149">Note</span><span class="sxs-lookup"><span data-stu-id="6adb1-149">NOTES</span></span>
<span data-ttu-id="6adb1-150">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="6adb1-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6adb1-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6adb1-151">RELATED LINKS</span></span>

[<span data-ttu-id="6adb1-152">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="6adb1-152">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="6adb1-153">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="6adb1-153">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="6adb1-154">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="6adb1-154">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
