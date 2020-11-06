---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 01c2849c69cfbdd785fae092aeed63117a07b1ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511259"
---
# <span data-ttu-id="2f7de-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2f7de-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="2f7de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f7de-102">SYNOPSIS</span></span>
<span data-ttu-id="2f7de-103">Ottiene informazioni sui set di dati in data factory.</span><span class="sxs-lookup"><span data-stu-id="2f7de-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f7de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f7de-104">SYNTAX</span></span>

### <span data-ttu-id="2f7de-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2f7de-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f7de-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2f7de-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f7de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f7de-107">DESCRIPTION</span></span>
<span data-ttu-id="2f7de-108">Il cmdlet Get-AzureRmDataFactoryV2Dataset ottiene informazioni sui dataset in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2f7de-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="2f7de-109">Se specifichi il nome di un DataSet, questo cmdlet ottiene le informazioni su tale set di dati.</span><span class="sxs-lookup"><span data-stu-id="2f7de-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="2f7de-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i DataSet nella data factory.</span><span class="sxs-lookup"><span data-stu-id="2f7de-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="2f7de-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f7de-111">EXAMPLES</span></span>

### <span data-ttu-id="2f7de-112">Esempio 1: ottenere informazioni su tutti i set di dati</span><span class="sxs-lookup"><span data-stu-id="2f7de-112">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="2f7de-113">Questo comando consente di ottenere informazioni su tutti i DataSet nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2f7de-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="2f7de-114">Esempio 2: ottenere informazioni su un dataset specifico</span><span class="sxs-lookup"><span data-stu-id="2f7de-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="2f7de-115">Questo comando consente di ottenere informazioni sul DataSet denominato DAWikipediaClickEvents nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2f7de-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="2f7de-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f7de-116">PARAMETERS</span></span>

### <span data-ttu-id="2f7de-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2f7de-117">-DataFactory</span></span>
<span data-ttu-id="2f7de-118">Specifica un oggetto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="2f7de-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="2f7de-119">Questo cmdlet ottiene i set di dati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2f7de-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


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

### <span data-ttu-id="2f7de-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2f7de-120">-DataFactoryName</span></span>
<span data-ttu-id="2f7de-121">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="2f7de-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2f7de-122">Questo cmdlet ottiene i set di dati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2f7de-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2f7de-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f7de-123">-Name</span></span>
<span data-ttu-id="2f7de-124">Specifica il nome del DataSet su cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="2f7de-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f7de-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f7de-125">-ResourceGroupName</span></span>
<span data-ttu-id="2f7de-126">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="2f7de-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2f7de-127">Questo cmdlet ottiene i DataSet che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2f7de-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2f7de-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f7de-128">-DefaultProfile</span></span>
<span data-ttu-id="2f7de-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f7de-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f7de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f7de-130">CommonParameters</span></span>
<span data-ttu-id="2f7de-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f7de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f7de-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f7de-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f7de-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f7de-133">INPUTS</span></span>

### <span data-ttu-id="2f7de-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2f7de-134">System.String</span></span>
<span data-ttu-id="2f7de-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2f7de-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2f7de-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f7de-136">OUTPUTS</span></span>

### <span data-ttu-id="2f7de-137">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2f7de-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2f7de-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="2f7de-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="2f7de-139">Note</span><span class="sxs-lookup"><span data-stu-id="2f7de-139">NOTES</span></span>
<span data-ttu-id="2f7de-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="2f7de-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2f7de-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f7de-141">RELATED LINKS</span></span>

[<span data-ttu-id="2f7de-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2f7de-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="2f7de-143">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2f7de-143">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
