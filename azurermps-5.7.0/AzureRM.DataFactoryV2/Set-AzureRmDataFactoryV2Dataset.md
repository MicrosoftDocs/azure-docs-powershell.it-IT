---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 405ec877f139865082d21eb2c05ace17f1100e2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508199"
---
# <span data-ttu-id="97afd-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="97afd-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="97afd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97afd-102">SYNOPSIS</span></span>
<span data-ttu-id="97afd-103">Crea un DataSet in data factory.</span><span class="sxs-lookup"><span data-stu-id="97afd-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97afd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97afd-104">SYNTAX</span></span>

### <span data-ttu-id="97afd-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97afd-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97afd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="97afd-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97afd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97afd-107">DESCRIPTION</span></span>
<span data-ttu-id="97afd-108">Il cmdlet Set-AzureRmDataFactoryV2Dataset crea un DataSet in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="97afd-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="97afd-109">Se si specifica un nome per un set di dati già esistente, questo cmdlet richiede conferma prima di sostituire il DataSet.</span><span class="sxs-lookup"><span data-stu-id="97afd-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="97afd-110">Se specifichi il parametro Force, il cmdlet sostituisce il DataSet esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="97afd-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="97afd-111">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="97afd-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="97afd-112">Se nella data factory esiste già un set di dati con lo stesso nome, questo cmdlet richiede di confermare se sovrascrivere il DataSet esistente con il nuovo DataSet.</span><span class="sxs-lookup"><span data-stu-id="97afd-112">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="97afd-113">Se si conferma di sovrascrivere il DataSet esistente, viene sostituita anche la definizione del set di dati.</span><span class="sxs-lookup"><span data-stu-id="97afd-113">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="97afd-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97afd-114">EXAMPLES</span></span>

### <span data-ttu-id="97afd-115">Esempio 1: creare un DataSet</span><span class="sxs-lookup"><span data-stu-id="97afd-115">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="97afd-116">Questo comando crea un DataSet denominato DA_WikipediaClickEvents nella data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="97afd-116">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="97afd-117">Il comando basa il DataSet sulle informazioni nella DAWikipediaClickEvents.jssu file.</span><span class="sxs-lookup"><span data-stu-id="97afd-117">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="97afd-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97afd-118">PARAMETERS</span></span>

### <span data-ttu-id="97afd-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="97afd-119">-DataFactoryName</span></span>
<span data-ttu-id="97afd-120">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="97afd-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="97afd-121">Questo cmdlet crea un DataSet nella Factory di dati specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="97afd-121">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="97afd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97afd-122">-DefaultProfile</span></span>
<span data-ttu-id="97afd-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97afd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97afd-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="97afd-124">-DefinitionFile</span></span>
<span data-ttu-id="97afd-125">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="97afd-125">The JSON file path.</span></span>

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

### <span data-ttu-id="97afd-126">-Force</span><span class="sxs-lookup"><span data-stu-id="97afd-126">-Force</span></span>
<span data-ttu-id="97afd-127">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="97afd-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="97afd-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="97afd-128">-Name</span></span>
<span data-ttu-id="97afd-129">Specifica il nome del DataSet da creare.</span><span class="sxs-lookup"><span data-stu-id="97afd-129">Specifies the name of the dataset to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97afd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97afd-130">-ResourceGroupName</span></span>
<span data-ttu-id="97afd-131">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="97afd-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="97afd-132">Questo cmdlet crea un set di dati nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="97afd-132">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="97afd-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97afd-133">-ResourceId</span></span>
<span data-ttu-id="97afd-134">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="97afd-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="97afd-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97afd-135">-Confirm</span></span>
<span data-ttu-id="97afd-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97afd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97afd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97afd-137">-WhatIf</span></span>
<span data-ttu-id="97afd-138">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97afd-138">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="97afd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97afd-139">CommonParameters</span></span>
<span data-ttu-id="97afd-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97afd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97afd-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97afd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97afd-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97afd-142">INPUTS</span></span>

### <span data-ttu-id="97afd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="97afd-143">System.String</span></span>

## <span data-ttu-id="97afd-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97afd-144">OUTPUTS</span></span>

### <span data-ttu-id="97afd-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="97afd-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="97afd-146">Note</span><span class="sxs-lookup"><span data-stu-id="97afd-146">NOTES</span></span>
<span data-ttu-id="97afd-147">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="97afd-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="97afd-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97afd-148">RELATED LINKS</span></span>

[<span data-ttu-id="97afd-149">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="97afd-149">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="97afd-150">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="97afd-150">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
