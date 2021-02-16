---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 38af817205f8d80615fa94799eee5a7a54f05e78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208739"
---
# <span data-ttu-id="f93db-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="f93db-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="f93db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f93db-102">SYNOPSIS</span></span>
<span data-ttu-id="f93db-103">Crea un set di dati in Data factory.</span><span class="sxs-lookup"><span data-stu-id="f93db-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="f93db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f93db-104">SYNTAX</span></span>

### <span data-ttu-id="f93db-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="f93db-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f93db-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f93db-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f93db-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f93db-107">DESCRIPTION</span></span>
<span data-ttu-id="f93db-108">Il cmdlet **New-AzDataFactoryDataset** crea un set di dati in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="f93db-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="f93db-109">Se si specifica un nome per un set di dati già esistente, questo cmdlet richiede conferma prima che sostituisca il set di dati.</span><span class="sxs-lookup"><span data-stu-id="f93db-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="f93db-110">Se si specifica il *parametro Force,* il cmdlet sostituisce il set di dati esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="f93db-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="f93db-111">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="f93db-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="f93db-112">Creare un data factory.</span><span class="sxs-lookup"><span data-stu-id="f93db-112">Create a data factory.</span></span> 
- <span data-ttu-id="f93db-113">Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="f93db-113">Create linked services.</span></span> 
- <span data-ttu-id="f93db-114">Creare set di dati.</span><span class="sxs-lookup"><span data-stu-id="f93db-114">Create datasets.</span></span> 
- <span data-ttu-id="f93db-115">Creare una pipeline.</span><span class="sxs-lookup"><span data-stu-id="f93db-115">Create a pipeline.</span></span>
<span data-ttu-id="f93db-116">Se esiste già un set di dati con lo stesso nome nel data factory, questo cmdlet chiede di confermare se sovrascrivere il set di dati esistente con il nuovo set di dati.</span><span class="sxs-lookup"><span data-stu-id="f93db-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="f93db-117">Se si conferma di sovrascrivere il set di dati esistente, viene sostituita anche la definizione del set di dati.</span><span class="sxs-lookup"><span data-stu-id="f93db-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="f93db-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f93db-118">EXAMPLES</span></span>

### <span data-ttu-id="f93db-119">Esempio 1: Creare un set di dati</span><span class="sxs-lookup"><span data-stu-id="f93db-119">Example 1: Create a dataset</span></span>
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="f93db-120">Questo comando crea un set di DA_WikipediaClickEvents dati denominato WikiADF nel data factory.</span><span class="sxs-lookup"><span data-stu-id="f93db-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="f93db-121">Il comando basa il set di dati sulle informazioni DAWikipediaClickEvents.jssu file.</span><span class="sxs-lookup"><span data-stu-id="f93db-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="f93db-122">Esempio 2: Visualizzare la disponibilità per un nuovo set di dati</span><span class="sxs-lookup"><span data-stu-id="f93db-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="f93db-123">Il primo comando crea un set di DA_WikipediaClickEvents denominato, come nell'esempio precedente, e quindi lo assegna alla $Dataset variabile.</span><span class="sxs-lookup"><span data-stu-id="f93db-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="f93db-124">Il secondo comando usa la notazione punto standard per visualizzare i dettagli sulla proprietà Disponibilità del set di dati.</span><span class="sxs-lookup"><span data-stu-id="f93db-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="f93db-125">Esempio 3: Visualizzare la posizione per un nuovo set di dati</span><span class="sxs-lookup"><span data-stu-id="f93db-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="f93db-126">Il primo comando crea un set di DA_WikipediaClickEvents denominato, come nell'esempio precedente, e quindi lo assegna alla $Dataset variabile.</span><span class="sxs-lookup"><span data-stu-id="f93db-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="f93db-127">Il secondo comando visualizza dettagli sulla proprietà Location del set di dati.</span><span class="sxs-lookup"><span data-stu-id="f93db-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="f93db-128">Esempio 4: Visualizzare le regole di convalida per un nuovo set di dati</span><span class="sxs-lookup"><span data-stu-id="f93db-128">Example 4: View validation rules for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

<span data-ttu-id="f93db-129">Il primo comando crea un set di DA_WikipediaClickEvents denominato, come nell'esempio precedente, e quindi lo assegna alla $Dataset variabile.</span><span class="sxs-lookup"><span data-stu-id="f93db-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="f93db-130">Il secondo comando ottiene dettagli sulle regole di convalida per il set di dati e quindi le passa al cmdlet Format-List usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="f93db-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f93db-131">Questo Windows PowerShell cmdlet formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="f93db-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="f93db-132">Per altre informazioni, digitare `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="f93db-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="f93db-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f93db-133">PARAMETERS</span></span>

### <span data-ttu-id="f93db-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f93db-134">-DataFactory</span></span>
<span data-ttu-id="f93db-135">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="f93db-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f93db-136">Questo cmdlet crea un set di dati nel data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f93db-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f93db-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f93db-137">-DataFactoryName</span></span>
<span data-ttu-id="f93db-138">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="f93db-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f93db-139">Questo cmdlet crea un set di dati nel data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f93db-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f93db-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f93db-140">-DefaultProfile</span></span>
<span data-ttu-id="f93db-141">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f93db-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f93db-142">-File</span><span class="sxs-lookup"><span data-stu-id="f93db-142">-File</span></span>
<span data-ttu-id="f93db-143">Specifica il percorso completo del file JSON (JavaScript Object Notation) che contiene la descrizione del set di dati.</span><span class="sxs-lookup"><span data-stu-id="f93db-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

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

### <span data-ttu-id="f93db-144">-Force</span><span class="sxs-lookup"><span data-stu-id="f93db-144">-Force</span></span>
<span data-ttu-id="f93db-145">Indica che questo cmdlet sostituisce un set di dati esistente senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="f93db-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f93db-146">-Name</span><span class="sxs-lookup"><span data-stu-id="f93db-146">-Name</span></span>
<span data-ttu-id="f93db-147">Specifica il nome del set di dati da creare.</span><span class="sxs-lookup"><span data-stu-id="f93db-147">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="f93db-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f93db-148">-ResourceGroupName</span></span>
<span data-ttu-id="f93db-149">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f93db-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f93db-150">Questo cmdlet crea un set di dati nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f93db-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f93db-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f93db-151">-Confirm</span></span>
<span data-ttu-id="f93db-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f93db-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f93db-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f93db-153">-WhatIf</span></span>
<span data-ttu-id="f93db-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f93db-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f93db-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f93db-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f93db-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f93db-156">CommonParameters</span></span>
<span data-ttu-id="f93db-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f93db-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f93db-158">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f93db-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f93db-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="f93db-159">INPUTS</span></span>

### <span data-ttu-id="f93db-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f93db-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f93db-161">System.String</span><span class="sxs-lookup"><span data-stu-id="f93db-161">System.String</span></span>

## <span data-ttu-id="f93db-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f93db-162">OUTPUTS</span></span>

### <span data-ttu-id="f93db-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="f93db-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="f93db-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="f93db-164">NOTES</span></span>
* <span data-ttu-id="f93db-165">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="f93db-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f93db-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f93db-166">RELATED LINKS</span></span>

[<span data-ttu-id="f93db-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="f93db-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="f93db-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="f93db-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


