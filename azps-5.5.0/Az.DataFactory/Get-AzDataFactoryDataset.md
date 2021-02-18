---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: 44db491986f42bc37df250f5949690efe874c997
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181055"
---
# <span data-ttu-id="bc95f-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="bc95f-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="bc95f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc95f-102">SYNOPSIS</span></span>
<span data-ttu-id="bc95f-103">Ottiene informazioni sui set di dati in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="bc95f-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="bc95f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc95f-104">SYNTAX</span></span>

### <span data-ttu-id="bc95f-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="bc95f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc95f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bc95f-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc95f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bc95f-107">DESCRIPTION</span></span>
<span data-ttu-id="bc95f-108">Il **cmdlet Get-AzDataFactoryDataset** ottiene informazioni sui set di dati in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="bc95f-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="bc95f-109">Se si specifica il nome di un set di dati, questo cmdlet ottiene informazioni sul set di dati.</span><span class="sxs-lookup"><span data-stu-id="bc95f-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="bc95f-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i set di dati nel data factory.</span><span class="sxs-lookup"><span data-stu-id="bc95f-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="bc95f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc95f-111">EXAMPLES</span></span>

### <span data-ttu-id="bc95f-112">Esempio 1: Ottenere informazioni su tutti i set di dati</span><span class="sxs-lookup"><span data-stu-id="bc95f-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="bc95f-113">Questo comando recupera informazioni su tutti i set di dati del data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="bc95f-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="bc95f-114">Esempio 2: Ottenere informazioni su un set di dati specifico</span><span class="sxs-lookup"><span data-stu-id="bc95f-114">Example 2: Get information about a specific dataset</span></span>
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

<span data-ttu-id="bc95f-115">Questo comando recupera informazioni sul set di dati denominato DAWikipediaClickEvents nel data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="bc95f-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="bc95f-116">Esempio 3: Ottenere la posizione per un set di dati specifico</span><span class="sxs-lookup"><span data-stu-id="bc95f-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="bc95f-117">Questo comando recupera informazioni per il set di dati denominato DAWikipediaClickEvents nel data factory  denominato WikiADF e quindi usa la notazione punto standard per visualizzare la posizione associata al set di dati.</span><span class="sxs-lookup"><span data-stu-id="bc95f-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="bc95f-118">In alternativa, assegnare l'output del cmdlet **Get-AzDataFactoryDataset** a una variabile e quindi usare la notazione punto per visualizzare la proprietà Location associata all'oggetto set di dati archiviato nella variabile.</span><span class="sxs-lookup"><span data-stu-id="bc95f-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="bc95f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc95f-119">PARAMETERS</span></span>

### <span data-ttu-id="bc95f-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bc95f-120">-DataFactory</span></span>
<span data-ttu-id="bc95f-121">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="bc95f-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="bc95f-122">Questo cmdlet ottiene i set di dati che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bc95f-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bc95f-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bc95f-123">-DataFactoryName</span></span>
<span data-ttu-id="bc95f-124">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="bc95f-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bc95f-125">Questo cmdlet ottiene i set di dati che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bc95f-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bc95f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc95f-126">-DefaultProfile</span></span>
<span data-ttu-id="bc95f-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="bc95f-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc95f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="bc95f-128">-Name</span></span>
<span data-ttu-id="bc95f-129">Specifica il nome del set di dati su cui il cmdlet riceve informazioni.</span><span class="sxs-lookup"><span data-stu-id="bc95f-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="bc95f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc95f-130">-ResourceGroupName</span></span>
<span data-ttu-id="bc95f-131">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="bc95f-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bc95f-132">Questo cmdlet ottiene i set di dati che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bc95f-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bc95f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc95f-133">CommonParameters</span></span>
<span data-ttu-id="bc95f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc95f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc95f-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc95f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc95f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="bc95f-136">INPUTS</span></span>

### <span data-ttu-id="bc95f-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bc95f-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="bc95f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bc95f-138">System.String</span></span>

## <span data-ttu-id="bc95f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc95f-139">OUTPUTS</span></span>

### <span data-ttu-id="bc95f-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="bc95f-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="bc95f-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="bc95f-141">NOTES</span></span>
* <span data-ttu-id="bc95f-142">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="bc95f-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bc95f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc95f-143">RELATED LINKS</span></span>

[<span data-ttu-id="bc95f-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="bc95f-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="bc95f-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="bc95f-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


