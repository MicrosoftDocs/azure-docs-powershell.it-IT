---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryDataset.md
ms.openlocfilehash: f4944e8413c686f7d6970050db19ddc69cc351d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516260"
---
# <span data-ttu-id="61aa1-101">New-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="61aa1-101">New-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="61aa1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="61aa1-103">Crea un DataSet in data factory.</span><span class="sxs-lookup"><span data-stu-id="61aa1-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61aa1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61aa1-104">SYNTAX</span></span>

### <span data-ttu-id="61aa1-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61aa1-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61aa1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="61aa1-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61aa1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61aa1-107">DESCRIPTION</span></span>
<span data-ttu-id="61aa1-108">Il cmdlet **New-AzureRmDataFactoryDataset** crea un DataSet in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="61aa1-108">The **New-AzureRmDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="61aa1-109">Se si specifica un nome per un set di dati già esistente, questo cmdlet richiede conferma prima di sostituire il DataSet.</span><span class="sxs-lookup"><span data-stu-id="61aa1-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="61aa1-110">Se specifichi il parametro *Force* , il cmdlet sostituisce il DataSet esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="61aa1-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="61aa1-111">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="61aa1-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="61aa1-112">Creare una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="61aa1-112">Create a data factory.</span></span> 
- <span data-ttu-id="61aa1-113">Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="61aa1-113">Create linked services.</span></span> 
- <span data-ttu-id="61aa1-114">Creare set di DataSet.</span><span class="sxs-lookup"><span data-stu-id="61aa1-114">Create datasets.</span></span> 
- <span data-ttu-id="61aa1-115">Creare una pipeline.</span><span class="sxs-lookup"><span data-stu-id="61aa1-115">Create a pipeline.</span></span>

<span data-ttu-id="61aa1-116">Se nella data factory esiste già un set di dati con lo stesso nome, questo cmdlet richiede di confermare se sovrascrivere il DataSet esistente con il nuovo DataSet.</span><span class="sxs-lookup"><span data-stu-id="61aa1-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="61aa1-117">Se si conferma di sovrascrivere il DataSet esistente, viene sostituita anche la definizione del set di dati.</span><span class="sxs-lookup"><span data-stu-id="61aa1-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="61aa1-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61aa1-118">EXAMPLES</span></span>

### <span data-ttu-id="61aa1-119">Esempio 1: creare un DataSet</span><span class="sxs-lookup"><span data-stu-id="61aa1-119">Example 1: Create a dataset</span></span>
```
PS C:\>New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="61aa1-120">Questo comando crea un DataSet denominato DA_WikipediaClickEvents nella data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="61aa1-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="61aa1-121">Il comando basa il DataSet sulle informazioni nella DAWikipediaClickEvents.jssu file.</span><span class="sxs-lookup"><span data-stu-id="61aa1-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="61aa1-122">Esempio 2: visualizzare la disponibilità per un nuovo set di dati</span><span class="sxs-lookup"><span data-stu-id="61aa1-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="61aa1-123">Il primo comando crea un DataSet denominato DA_WikipediaClickEvents, come in un esempio precedente, e quindi assegna tale DataSet alla variabile $Dataset.</span><span class="sxs-lookup"><span data-stu-id="61aa1-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>

<span data-ttu-id="61aa1-124">Il secondo comando usa la notazione standard del punto per visualizzare i dettagli sulla proprietà Availability del DataSet.</span><span class="sxs-lookup"><span data-stu-id="61aa1-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="61aa1-125">Esempio 3: visualizzare la posizione di un nuovo set di dati</span><span class="sxs-lookup"><span data-stu-id="61aa1-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="61aa1-126">Il primo comando crea un DataSet denominato DA_WikipediaClickEvents, come in un esempio precedente, e quindi assegna tale DataSet alla variabile $Dataset.</span><span class="sxs-lookup"><span data-stu-id="61aa1-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>

<span data-ttu-id="61aa1-127">Il secondo comando Visualizza i dettagli sulla proprietà Location del DataSet.</span><span class="sxs-lookup"><span data-stu-id="61aa1-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="61aa1-128">Esempio 4: visualizzare le regole di convalida per un nuovo set di dati</span><span class="sxs-lookup"><span data-stu-id="61aa1-128">Example 4: View validation rules for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

<span data-ttu-id="61aa1-129">Il primo comando crea un DataSet denominato DA_WikipediaClickEvents, come in un esempio precedente, e quindi assegna tale DataSet alla variabile $Dataset.</span><span class="sxs-lookup"><span data-stu-id="61aa1-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>

<span data-ttu-id="61aa1-130">Il secondo comando consente di ottenere informazioni dettagliate sulle regole di convalida per il DataSet e quindi di passarle al cmdlet Format-List usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="61aa1-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="61aa1-131">Il cmdlet di Windows PowerShell formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="61aa1-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="61aa1-132">Per altre informazioni, digitare `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="61aa1-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="61aa1-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61aa1-133">PARAMETERS</span></span>

### <span data-ttu-id="61aa1-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="61aa1-134">-DataFactory</span></span>
<span data-ttu-id="61aa1-135">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="61aa1-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="61aa1-136">Questo cmdlet crea un DataSet nella Factory di dati specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61aa1-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="61aa1-137">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="61aa1-137">-DataFactoryName</span></span>
<span data-ttu-id="61aa1-138">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="61aa1-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="61aa1-139">Questo cmdlet crea un DataSet nella Factory di dati specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61aa1-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="61aa1-140">-File</span><span class="sxs-lookup"><span data-stu-id="61aa1-140">-File</span></span>
<span data-ttu-id="61aa1-141">Specifica il percorso completo del file JSON (JavaScript Object Notation) che contiene la descrizione del DataSet.</span><span class="sxs-lookup"><span data-stu-id="61aa1-141">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61aa1-142">-Force</span><span class="sxs-lookup"><span data-stu-id="61aa1-142">-Force</span></span>
<span data-ttu-id="61aa1-143">Indica che questo cmdlet sostituisce un set di dati esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="61aa1-143">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="61aa1-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="61aa1-144">-Name</span></span>
<span data-ttu-id="61aa1-145">Specifica il nome del DataSet da creare.</span><span class="sxs-lookup"><span data-stu-id="61aa1-145">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61aa1-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61aa1-146">-ResourceGroupName</span></span>
<span data-ttu-id="61aa1-147">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="61aa1-147">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="61aa1-148">Questo cmdlet crea un set di dati nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61aa1-148">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="61aa1-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61aa1-149">-Confirm</span></span>
<span data-ttu-id="61aa1-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61aa1-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61aa1-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61aa1-151">-WhatIf</span></span>
<span data-ttu-id="61aa1-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61aa1-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61aa1-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61aa1-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61aa1-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61aa1-154">-DefaultProfile</span></span>
<span data-ttu-id="61aa1-155">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61aa1-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61aa1-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61aa1-156">CommonParameters</span></span>
<span data-ttu-id="61aa1-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61aa1-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61aa1-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61aa1-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61aa1-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61aa1-159">INPUTS</span></span>

## <span data-ttu-id="61aa1-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61aa1-160">OUTPUTS</span></span>

### <span data-ttu-id="61aa1-161">Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span><span class="sxs-lookup"><span data-stu-id="61aa1-161">Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span></span>

## <span data-ttu-id="61aa1-162">Note</span><span class="sxs-lookup"><span data-stu-id="61aa1-162">NOTES</span></span>
* <span data-ttu-id="61aa1-163">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="61aa1-163">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="61aa1-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61aa1-164">RELATED LINKS</span></span>

[<span data-ttu-id="61aa1-165">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="61aa1-165">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="61aa1-166">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="61aa1-166">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)


