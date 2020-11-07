---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 1fb9b4a80faca7681154d375123b7e19be65e5c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675022"
---
# <span data-ttu-id="026ad-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="026ad-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="026ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="026ad-102">SYNOPSIS</span></span>
<span data-ttu-id="026ad-103">Ottiene informazioni sui set di dati in data factory.</span><span class="sxs-lookup"><span data-stu-id="026ad-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="026ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="026ad-104">SYNTAX</span></span>

### <span data-ttu-id="026ad-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="026ad-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="026ad-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="026ad-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="026ad-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="026ad-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="026ad-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="026ad-108">DESCRIPTION</span></span>
<span data-ttu-id="026ad-109">Il cmdlet Get-AzDataFactoryV2Dataset ottiene informazioni sui dataset in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="026ad-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="026ad-110">Se specifichi il nome di un DataSet, questo cmdlet ottiene le informazioni su tale set di dati.</span><span class="sxs-lookup"><span data-stu-id="026ad-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="026ad-111">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i DataSet nella data factory.</span><span class="sxs-lookup"><span data-stu-id="026ad-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="026ad-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="026ad-112">EXAMPLES</span></span>

### <span data-ttu-id="026ad-113">Esempio 1: ottenere informazioni su tutti i set di dati</span><span class="sxs-lookup"><span data-stu-id="026ad-113">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="026ad-114">Questo comando consente di ottenere informazioni su tutti i DataSet nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="026ad-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="026ad-115">Esempio 2: ottenere informazioni su un dataset specifico</span><span class="sxs-lookup"><span data-stu-id="026ad-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="026ad-116">Questo comando consente di ottenere informazioni sul DataSet denominato DAWikipediaClickEvents nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="026ad-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="026ad-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="026ad-117">PARAMETERS</span></span>

### <span data-ttu-id="026ad-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="026ad-118">-DataFactory</span></span>
<span data-ttu-id="026ad-119">Specifica un oggetto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="026ad-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="026ad-120">Questo cmdlet ottiene i set di dati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="026ad-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="026ad-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="026ad-121">-DataFactoryName</span></span>
<span data-ttu-id="026ad-122">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="026ad-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="026ad-123">Questo cmdlet ottiene i set di dati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="026ad-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="026ad-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="026ad-124">-DefaultProfile</span></span>
<span data-ttu-id="026ad-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="026ad-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="026ad-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="026ad-126">-Name</span></span>
<span data-ttu-id="026ad-127">Specifica il nome del DataSet su cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="026ad-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="026ad-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="026ad-128">-ResourceGroupName</span></span>
<span data-ttu-id="026ad-129">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="026ad-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="026ad-130">Questo cmdlet ottiene i DataSet che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="026ad-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="026ad-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="026ad-131">-ResourceId</span></span>
<span data-ttu-id="026ad-132">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="026ad-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="026ad-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="026ad-133">CommonParameters</span></span>
<span data-ttu-id="026ad-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="026ad-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="026ad-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="026ad-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="026ad-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="026ad-136">INPUTS</span></span>

### <span data-ttu-id="026ad-137">System. String</span><span class="sxs-lookup"><span data-stu-id="026ad-137">System.String</span></span>

### <span data-ttu-id="026ad-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="026ad-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="026ad-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="026ad-139">OUTPUTS</span></span>

### <span data-ttu-id="026ad-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="026ad-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="026ad-141">Note</span><span class="sxs-lookup"><span data-stu-id="026ad-141">NOTES</span></span>
<span data-ttu-id="026ad-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="026ad-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="026ad-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="026ad-143">RELATED LINKS</span></span>

[<span data-ttu-id="026ad-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="026ad-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="026ad-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="026ad-145">Remove-AzDataFactoryV2Dataset</span></span>]()