---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 6605fa005d8ca5c41c0ea60ee21a15c0196ae832
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188623"
---
# <span data-ttu-id="8838f-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8838f-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="8838f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8838f-102">SYNOPSIS</span></span>
<span data-ttu-id="8838f-103">Ottiene informazioni sulle pipeline in Data factory.</span><span class="sxs-lookup"><span data-stu-id="8838f-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="8838f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8838f-104">SYNTAX</span></span>

### <span data-ttu-id="8838f-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="8838f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8838f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8838f-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8838f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8838f-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8838f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8838f-108">DESCRIPTION</span></span>
<span data-ttu-id="8838f-109">Il Get-AzDataFactoryV2Pipeline cmdlet recupera informazioni sulle pipeline in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="8838f-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="8838f-110">Se si specifica il nome di una pipeline, questo cmdlet ottiene informazioni sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="8838f-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="8838f-111">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutte le pipeline nel data factory.</span><span class="sxs-lookup"><span data-stu-id="8838f-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="8838f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8838f-112">EXAMPLES</span></span>

### <span data-ttu-id="8838f-113">Esempio 1: Ottenere informazioni su tutte le pipeline</span><span class="sxs-lookup"><span data-stu-id="8838f-113">Example 1: Get information about all pipelines</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

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

<span data-ttu-id="8838f-114">Questo comando recupera informazioni su tutte le pipeline del data factory denominate WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8838f-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="8838f-115">È possibile usare uno dei comandi di esempio seguenti.</span><span class="sxs-lookup"><span data-stu-id="8838f-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="8838f-116">Il secondo usa un oggetto DataFactory come parametro.</span><span class="sxs-lookup"><span data-stu-id="8838f-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="8838f-117">Esempio 2: Ottenere informazioni su una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="8838f-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="8838f-118">Questo comando recupera informazioni sulla pipeline denominata DPWikisample nel data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8838f-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="8838f-119">Il comando passa queste informazioni al cmdlet Format-List tramite l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="8838f-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8838f-120">Questo Windows PowerShell cmdlet formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="8838f-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="8838f-121">Per altre informazioni, digitare Get-Help-List.</span><span class="sxs-lookup"><span data-stu-id="8838f-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="8838f-122">Esempio 3: Ottenere le proprietà per una pipeline specifica</span><span class="sxs-lookup"><span data-stu-id="8838f-122">Example 3: Get the properties for a specific pipeline</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

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

<span data-ttu-id="8838f-123">Questo comando recupera le informazioni per la pipeline denominata DPWikisample nel data factory denominato WikiADF e quindi usa la notazione punto standard per visualizzare la proprietà Attività associata a tale pipeline.</span><span class="sxs-lookup"><span data-stu-id="8838f-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="8838f-124">Esempio 4: Ottenere informazioni sugli input per la prima attività</span><span class="sxs-lookup"><span data-stu-id="8838f-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="8838f-125">Questo comando recupera le informazioni per la pipeline denominata DPWikisample nel data factory denominato WikiADF e quindi usa la notazione punto standard per visualizzare la proprietà Attività associata a tale pipeline.</span><span class="sxs-lookup"><span data-stu-id="8838f-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="8838f-126">Il comando visualizza la proprietà Inputs del primo elemento della matrice Activities usando il cmdlet Format-List.</span><span class="sxs-lookup"><span data-stu-id="8838f-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="8838f-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8838f-127">PARAMETERS</span></span>

### <span data-ttu-id="8838f-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8838f-128">-DataFactory</span></span>
<span data-ttu-id="8838f-129">Specifica un oggetto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="8838f-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="8838f-130">Questo cmdlet ottiene pipeline che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8838f-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8838f-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8838f-131">-DataFactoryName</span></span>
<span data-ttu-id="8838f-132">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="8838f-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8838f-133">Questo cmdlet ottiene pipeline che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8838f-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8838f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8838f-134">-DefaultProfile</span></span>
<span data-ttu-id="8838f-135">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8838f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8838f-136">-Name</span><span class="sxs-lookup"><span data-stu-id="8838f-136">-Name</span></span>
<span data-ttu-id="8838f-137">Specifica il nome della pipeline su cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="8838f-137">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="8838f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8838f-138">-ResourceGroupName</span></span>
<span data-ttu-id="8838f-139">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="8838f-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8838f-140">Questo cmdlet ottiene pipeline che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8838f-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8838f-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8838f-141">-ResourceId</span></span>
<span data-ttu-id="8838f-142">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="8838f-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8838f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8838f-143">CommonParameters</span></span>
<span data-ttu-id="8838f-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8838f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8838f-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8838f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8838f-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="8838f-146">INPUTS</span></span>

### <span data-ttu-id="8838f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="8838f-147">System.String</span></span>

### <span data-ttu-id="8838f-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8838f-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="8838f-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8838f-149">OUTPUTS</span></span>

### <span data-ttu-id="8838f-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="8838f-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="8838f-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="8838f-151">NOTES</span></span>
<span data-ttu-id="8838f-152">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="8838f-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8838f-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8838f-153">RELATED LINKS</span></span>

[<span data-ttu-id="8838f-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8838f-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8838f-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8838f-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8838f-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8838f-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
