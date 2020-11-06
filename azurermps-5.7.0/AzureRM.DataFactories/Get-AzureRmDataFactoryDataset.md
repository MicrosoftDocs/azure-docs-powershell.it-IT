---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 10e4af67d76e6c9d367de4d9b512d003e211ddae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516823"
---
# <span data-ttu-id="56a7c-101">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="56a7c-101">Get-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="56a7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="56a7c-103">Ottiene informazioni sui set di dati in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="56a7c-103">Gets information about datasets in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56a7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56a7c-104">SYNTAX</span></span>

### <span data-ttu-id="56a7c-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56a7c-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56a7c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="56a7c-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56a7c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56a7c-107">DESCRIPTION</span></span>
<span data-ttu-id="56a7c-108">Il cmdlet **Get-AzureRmDataFactoryDataset** ottiene le informazioni sui set di dati in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="56a7c-108">The **Get-AzureRmDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="56a7c-109">Se specifichi il nome di un DataSet, questo cmdlet ottiene le informazioni su tale set di dati.</span><span class="sxs-lookup"><span data-stu-id="56a7c-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="56a7c-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i DataSet nella data factory.</span><span class="sxs-lookup"><span data-stu-id="56a7c-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="56a7c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56a7c-111">EXAMPLES</span></span>

### <span data-ttu-id="56a7c-112">Esempio 1: ottenere informazioni su tutti i set di dati</span><span class="sxs-lookup"><span data-stu-id="56a7c-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
DatasetName       : DACuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName         : DAWikiAggregatedData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}
```

<span data-ttu-id="56a7c-113">Questo comando consente di ottenere informazioni su tutti i DataSet nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="56a7c-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="56a7c-114">Esempio 2: ottenere informazioni su un dataset specifico</span><span class="sxs-lookup"><span data-stu-id="56a7c-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="56a7c-115">Questo comando consente di ottenere informazioni sul DataSet denominato DAWikipediaClickEvents nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="56a7c-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="56a7c-116">Esempio 3: ottenere la posizione di un set di dati specifico</span><span class="sxs-lookup"><span data-stu-id="56a7c-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="56a7c-117">Questo comando ottiene le informazioni per il DataSet denominato DAWikipediaClickEvents nella data factory denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la **posizione** associata a tale set di dati.</span><span class="sxs-lookup"><span data-stu-id="56a7c-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="56a7c-118">In alternativa, assegnare l'output del cmdlet **Get-AzureRmDataFactoryDataset** a una variabile e quindi usare la notazione del punto per visualizzare la proprietà Location associata all'oggetto DataSet archiviato in tale variabile.</span><span class="sxs-lookup"><span data-stu-id="56a7c-118">Alternatively, assign the output of the **Get-AzureRmDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="56a7c-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56a7c-119">PARAMETERS</span></span>

### <span data-ttu-id="56a7c-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="56a7c-120">-DataFactory</span></span>
<span data-ttu-id="56a7c-121">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="56a7c-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="56a7c-122">Questo cmdlet ottiene i set di dati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="56a7c-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56a7c-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="56a7c-123">-DataFactoryName</span></span>
<span data-ttu-id="56a7c-124">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="56a7c-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="56a7c-125">Questo cmdlet ottiene i set di dati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="56a7c-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="56a7c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56a7c-126">-DefaultProfile</span></span>
<span data-ttu-id="56a7c-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="56a7c-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56a7c-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="56a7c-128">-Name</span></span>
<span data-ttu-id="56a7c-129">Specifica il nome del DataSet sul quale questo cmdlet ottiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="56a7c-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56a7c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56a7c-130">-ResourceGroupName</span></span>
<span data-ttu-id="56a7c-131">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="56a7c-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="56a7c-132">Questo cmdlet ottiene i DataSet che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="56a7c-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="56a7c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56a7c-133">CommonParameters</span></span>
<span data-ttu-id="56a7c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56a7c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56a7c-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56a7c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56a7c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56a7c-136">INPUTS</span></span>

### <span data-ttu-id="56a7c-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="56a7c-137">None</span></span>
<span data-ttu-id="56a7c-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="56a7c-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56a7c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56a7c-139">OUTPUTS</span></span>

### <span data-ttu-id="56a7c-140">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span><span class="sxs-lookup"><span data-stu-id="56a7c-140">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span></span>

## <span data-ttu-id="56a7c-141">Note</span><span class="sxs-lookup"><span data-stu-id="56a7c-141">NOTES</span></span>
* <span data-ttu-id="56a7c-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="56a7c-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="56a7c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56a7c-143">RELATED LINKS</span></span>

[<span data-ttu-id="56a7c-144">New-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="56a7c-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="56a7c-145">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="56a7c-145">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)


