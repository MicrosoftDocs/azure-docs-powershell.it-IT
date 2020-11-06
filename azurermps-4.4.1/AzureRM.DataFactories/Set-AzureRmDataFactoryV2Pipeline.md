---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: 510f0f5b943a1a0abab1bc97ac5e70fa6f450898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511244"
---
# <span data-ttu-id="8e7ff-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8e7ff-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="8e7ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7ff-103">Crea una pipeline in data factory.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e7ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e7ff-104">SYNTAX</span></span>

### <span data-ttu-id="8e7ff-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e7ff-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e7ff-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e7ff-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e7ff-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e7ff-107">DESCRIPTION</span></span>
<span data-ttu-id="8e7ff-108">Il cmdlet Set-AzureRmDataFactoryV2Pipeline crea una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="8e7ff-109">Se specifichi un nome per una pipeline già esistente, il cmdlet richiede conferma prima di sostituire la pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="8e7ff-110">Se specifichi il parametro Force, il cmdlet sostituisce la pipeline esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="8e7ff-111">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="8e7ff-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="8e7ff-112">Se nella data factory esiste già una pipeline con lo stesso nome, questo cmdlet richiede di confermare se sovrascrivere la pipeline esistente con la nuova pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-112">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="8e7ff-113">Se si conferma di sovrascrivere la pipeline esistente, viene sostituita anche la definizione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-113">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="8e7ff-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e7ff-114">EXAMPLES</span></span>

### <span data-ttu-id="8e7ff-115">Esempio 1: creare una pipeline</span><span class="sxs-lookup"><span data-stu-id="8e7ff-115">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="8e7ff-116">Questo comando crea una pipeline denominata DPWikisample nella Factory di dati denominata ADF.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-116">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="8e7ff-117">Il comando basa la pipeline sulle informazioni nella DPWikisample.jssu file.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-117">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="8e7ff-118">Questo file include informazioni sulle attività, ad esempio attività di copia e attività di HDInsight nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-118">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="8e7ff-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e7ff-119">PARAMETERS</span></span>

### <span data-ttu-id="8e7ff-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8e7ff-120">-Confirm</span></span>
<span data-ttu-id="8e7ff-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e7ff-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8e7ff-122">-DataFactoryName</span></span>
<span data-ttu-id="8e7ff-123">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8e7ff-124">Questo cmdlet crea una pipeline per la factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-124">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e7ff-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="8e7ff-125">-DefinitionFile</span></span>
<span data-ttu-id="8e7ff-126">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-126">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ff-127">-Force</span><span class="sxs-lookup"><span data-stu-id="8e7ff-127">-Force</span></span>
<span data-ttu-id="8e7ff-128">Indica che questo cmdlet sostituisce una pipeline esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-128">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ff-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e7ff-129">-Name</span></span>
<span data-ttu-id="8e7ff-130">Specifica il nome della pipeline da creare.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-130">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7ff-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7ff-131">-ResourceGroupName</span></span>
<span data-ttu-id="8e7ff-132">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8e7ff-133">Questo cmdlet crea una pipeline per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-133">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e7ff-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e7ff-134">-ResourceId</span></span>
<span data-ttu-id="8e7ff-135">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8e7ff-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e7ff-136">-WhatIf</span></span>
<span data-ttu-id="8e7ff-137">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8e7ff-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7ff-138">-DefaultProfile</span></span>
<span data-ttu-id="8e7ff-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e7ff-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7ff-140">CommonParameters</span></span>
<span data-ttu-id="8e7ff-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e7ff-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7ff-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e7ff-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7ff-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e7ff-143">INPUTS</span></span>

### <span data-ttu-id="8e7ff-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8e7ff-144">System.String</span></span>

## <span data-ttu-id="8e7ff-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e7ff-145">OUTPUTS</span></span>

### <span data-ttu-id="8e7ff-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="8e7ff-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="8e7ff-147">Note</span><span class="sxs-lookup"><span data-stu-id="8e7ff-147">NOTES</span></span>
<span data-ttu-id="8e7ff-148">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="8e7ff-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8e7ff-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e7ff-149">RELATED LINKS</span></span>

[<span data-ttu-id="8e7ff-150">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8e7ff-150">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8e7ff-151">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8e7ff-151">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8e7ff-152">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8e7ff-152">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
