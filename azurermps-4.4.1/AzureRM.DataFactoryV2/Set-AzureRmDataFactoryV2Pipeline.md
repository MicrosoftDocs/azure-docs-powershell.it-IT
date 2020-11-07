---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 2a936b9a75e9fc1053e2202950a6a6b4c49bd3a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688648"
---
# <span data-ttu-id="5e7f3-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5e7f3-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="5e7f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e7f3-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7f3-103">Crea una pipeline in data factory.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e7f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e7f3-104">SYNTAX</span></span>

### <span data-ttu-id="5e7f3-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e7f3-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5e7f3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e7f3-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="5e7f3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e7f3-107">DESCRIPTION</span></span>
<span data-ttu-id="5e7f3-108">Il cmdlet Set-AzureRmDataFactoryV2Pipeline crea una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="5e7f3-109">Se specifichi un nome per una pipeline già esistente, il cmdlet richiede conferma prima di sostituire la pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="5e7f3-110">Se specifichi il parametro Force, il cmdlet sostituisce la pipeline esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="5e7f3-111">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="5e7f3-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="5e7f3-112">Se nella data factory esiste già una pipeline con lo stesso nome, questo cmdlet richiede di confermare se sovrascrivere la pipeline esistente con la nuova pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-112">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="5e7f3-113">Se si conferma di sovrascrivere la pipeline esistente, viene sostituita anche la definizione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-113">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="5e7f3-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e7f3-114">EXAMPLES</span></span>

### <span data-ttu-id="5e7f3-115">Esempio 1: creare una pipeline</span><span class="sxs-lookup"><span data-stu-id="5e7f3-115">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

```

<span data-ttu-id="5e7f3-116">Questo comando crea una pipeline denominata DPWikisample nella Factory di dati denominata ADF.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-116">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="5e7f3-117">Il comando basa la pipeline sulle informazioni nella DPWikisample.jssu file.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-117">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="5e7f3-118">Questo file include informazioni sulle attività, ad esempio attività di copia e attività di HDInsight nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-118">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="5e7f3-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e7f3-119">PARAMETERS</span></span>

### <span data-ttu-id="5e7f3-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e7f3-120">-Confirm</span></span>
<span data-ttu-id="5e7f3-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e7f3-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5e7f3-122">-DataFactoryName</span></span>
<span data-ttu-id="5e7f3-123">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5e7f3-124">Questo cmdlet crea una pipeline per la factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-124">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e7f3-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="5e7f3-125">-DefinitionFile</span></span>
<span data-ttu-id="5e7f3-126">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-126">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e7f3-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5e7f3-127">-Force</span></span>
<span data-ttu-id="5e7f3-128">Indica che questo cmdlet sostituisce una pipeline esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-128">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e7f3-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e7f3-129">-Name</span></span>
<span data-ttu-id="5e7f3-130">Specifica il nome della pipeline da creare.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-130">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e7f3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e7f3-131">-ResourceGroupName</span></span>
<span data-ttu-id="5e7f3-132">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5e7f3-133">Questo cmdlet crea una pipeline per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-133">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e7f3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e7f3-134">-ResourceId</span></span>
<span data-ttu-id="5e7f3-135">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-135">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e7f3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e7f3-136">-WhatIf</span></span>
<span data-ttu-id="5e7f3-137">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e7f3-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="5e7f3-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e7f3-138">INPUTS</span></span>

### <span data-ttu-id="5e7f3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5e7f3-139">System.String</span></span>


## <span data-ttu-id="5e7f3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e7f3-140">OUTPUTS</span></span>

### <span data-ttu-id="5e7f3-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="5e7f3-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="5e7f3-142">Note</span><span class="sxs-lookup"><span data-stu-id="5e7f3-142">NOTES</span></span>
<span data-ttu-id="5e7f3-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="5e7f3-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5e7f3-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e7f3-144">RELATED LINKS</span></span>
[<span data-ttu-id="5e7f3-145">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5e7f3-145">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="5e7f3-146">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5e7f3-146">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="5e7f3-147">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5e7f3-147">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
