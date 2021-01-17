---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c02ce9b0ba62f7baf4879946bd0ab04efdd5c9e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350971"
---
# <span data-ttu-id="a1e8e-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="a1e8e-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="a1e8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e8e-103">Crea un DataSet in data factory.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="a1e8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1e8e-104">SYNTAX</span></span>

### <span data-ttu-id="a1e8e-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1e8e-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1e8e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1e8e-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1e8e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1e8e-107">DESCRIPTION</span></span>
<span data-ttu-id="a1e8e-108">Il cmdlet Set-AzDataFactoryV2Dataset crea un DataSet in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="a1e8e-109">Se si specifica un nome per un set di dati già esistente, questo cmdlet richiede conferma prima di sostituire il DataSet.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="a1e8e-110">Se specifichi il parametro Force, il cmdlet sostituisce il DataSet esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="a1e8e-111">Eseguire queste operazioni nell'ordine seguente:--creare una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="a1e8e-112">--Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-112">-- Create linked services.</span></span>
<span data-ttu-id="a1e8e-113">--Creare DataSet.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-113">-- Create datasets.</span></span>
<span data-ttu-id="a1e8e-114">--Crea una pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-114">-- Create a pipeline.</span></span>
<span data-ttu-id="a1e8e-115">Se nella data factory esiste già un set di dati con lo stesso nome, questo cmdlet richiede di confermare se sovrascrivere il DataSet esistente con il nuovo DataSet.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="a1e8e-116">Se si conferma di sovrascrivere il DataSet esistente, viene sostituita anche la definizione del set di dati.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="a1e8e-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1e8e-117">EXAMPLES</span></span>

### <span data-ttu-id="a1e8e-118">Esempio 1: creare un DataSet</span><span class="sxs-lookup"><span data-stu-id="a1e8e-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="a1e8e-119">Questo comando crea un DataSet denominato DA_WikipediaClickEvents nella data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="a1e8e-120">Il comando basa il DataSet sulle informazioni nella DAWikipediaClickEvents.jssu file.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="a1e8e-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1e8e-121">PARAMETERS</span></span>

### <span data-ttu-id="a1e8e-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a1e8e-122">-DataFactoryName</span></span>
<span data-ttu-id="a1e8e-123">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a1e8e-124">Questo cmdlet crea un DataSet nella Factory di dati specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1e8e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e8e-125">-DefaultProfile</span></span>
<span data-ttu-id="a1e8e-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1e8e-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="a1e8e-127">-DefinitionFile</span></span>
<span data-ttu-id="a1e8e-128">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-128">The JSON file path.</span></span>

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

### <span data-ttu-id="a1e8e-129">-Force</span><span class="sxs-lookup"><span data-stu-id="a1e8e-129">-Force</span></span>
<span data-ttu-id="a1e8e-130">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a1e8e-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1e8e-131">-Name</span></span>
<span data-ttu-id="a1e8e-132">Specifica il nome del DataSet da creare.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-132">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e8e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e8e-133">-ResourceGroupName</span></span>
<span data-ttu-id="a1e8e-134">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a1e8e-135">Questo cmdlet crea un set di dati nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1e8e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1e8e-136">-ResourceId</span></span>
<span data-ttu-id="a1e8e-137">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a1e8e-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1e8e-138">-Confirm</span></span>
<span data-ttu-id="a1e8e-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1e8e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1e8e-140">-WhatIf</span></span>
<span data-ttu-id="a1e8e-141">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a1e8e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e8e-142">CommonParameters</span></span>
<span data-ttu-id="a1e8e-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e8e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e8e-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1e8e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e8e-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1e8e-145">INPUTS</span></span>

### <span data-ttu-id="a1e8e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a1e8e-146">System.String</span></span>

## <span data-ttu-id="a1e8e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1e8e-147">OUTPUTS</span></span>

### <span data-ttu-id="a1e8e-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="a1e8e-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="a1e8e-149">Note</span><span class="sxs-lookup"><span data-stu-id="a1e8e-149">NOTES</span></span>
<span data-ttu-id="a1e8e-150">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="a1e8e-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a1e8e-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1e8e-151">RELATED LINKS</span></span>

[<span data-ttu-id="a1e8e-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="a1e8e-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="a1e8e-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="a1e8e-153">Remove-AzDataFactoryV2Dataset</span></span>]()
