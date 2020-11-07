---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: fe5359740975776e5796dce2a6d4959ed289cae6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675045"
---
# <span data-ttu-id="e5092-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="e5092-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="e5092-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5092-102">SYNOPSIS</span></span>
<span data-ttu-id="e5092-103">Ottiene informazioni sui set di dati in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e5092-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="e5092-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5092-104">SYNTAX</span></span>

### <span data-ttu-id="e5092-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5092-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5092-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e5092-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5092-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5092-107">DESCRIPTION</span></span>
<span data-ttu-id="e5092-108">Il cmdlet **Get-AzDataFactoryDataset** ottiene le informazioni sui set di dati in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e5092-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="e5092-109">Se specifichi il nome di un DataSet, questo cmdlet ottiene le informazioni su tale set di dati.</span><span class="sxs-lookup"><span data-stu-id="e5092-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="e5092-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i DataSet nella data factory.</span><span class="sxs-lookup"><span data-stu-id="e5092-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="e5092-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5092-111">EXAMPLES</span></span>

### <span data-ttu-id="e5092-112">Esempio 1: ottenere informazioni su tutti i set di dati</span><span class="sxs-lookup"><span data-stu-id="e5092-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
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

<span data-ttu-id="e5092-113">Questo comando consente di ottenere informazioni su tutti i DataSet nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e5092-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="e5092-114">Esempio 2: ottenere informazioni su un dataset specifico</span><span class="sxs-lookup"><span data-stu-id="e5092-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="e5092-115">Questo comando consente di ottenere informazioni sul DataSet denominato DAWikipediaClickEvents nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e5092-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="e5092-116">Esempio 3: ottenere la posizione di un set di dati specifico</span><span class="sxs-lookup"><span data-stu-id="e5092-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="e5092-117">Questo comando ottiene le informazioni per il DataSet denominato DAWikipediaClickEvents nella data factory denominata WikiADF e quindi usa la notazione a punti standard per visualizzare la **posizione** associata a tale set di dati.</span><span class="sxs-lookup"><span data-stu-id="e5092-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="e5092-118">In alternativa, assegnare l'output del cmdlet **Get-AzDataFactoryDataset** a una variabile e quindi usare la notazione del punto per visualizzare la proprietà Location associata all'oggetto DataSet archiviato in tale variabile.</span><span class="sxs-lookup"><span data-stu-id="e5092-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="e5092-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5092-119">PARAMETERS</span></span>

### <span data-ttu-id="e5092-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5092-120">-DataFactory</span></span>
<span data-ttu-id="e5092-121">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="e5092-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e5092-122">Questo cmdlet ottiene i set di dati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e5092-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5092-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e5092-123">-DataFactoryName</span></span>
<span data-ttu-id="e5092-124">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="e5092-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e5092-125">Questo cmdlet ottiene i set di dati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e5092-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5092-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5092-126">-DefaultProfile</span></span>
<span data-ttu-id="e5092-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e5092-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5092-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5092-128">-Name</span></span>
<span data-ttu-id="e5092-129">Specifica il nome del DataSet sul quale questo cmdlet ottiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="e5092-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="e5092-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5092-130">-ResourceGroupName</span></span>
<span data-ttu-id="e5092-131">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="e5092-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e5092-132">Questo cmdlet ottiene i DataSet che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e5092-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5092-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5092-133">CommonParameters</span></span>
<span data-ttu-id="e5092-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5092-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5092-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5092-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5092-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5092-136">INPUTS</span></span>

### <span data-ttu-id="e5092-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e5092-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="e5092-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e5092-138">System.String</span></span>

## <span data-ttu-id="e5092-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5092-139">OUTPUTS</span></span>

### <span data-ttu-id="e5092-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="e5092-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="e5092-141">Note</span><span class="sxs-lookup"><span data-stu-id="e5092-141">NOTES</span></span>
* <span data-ttu-id="e5092-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="e5092-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e5092-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5092-143">RELATED LINKS</span></span>

[<span data-ttu-id="e5092-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="e5092-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="e5092-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="e5092-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)

