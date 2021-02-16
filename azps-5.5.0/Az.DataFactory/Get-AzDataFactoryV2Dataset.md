---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5af8053f3d504cfc3eb28a2f8ad71f83492f0e3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204459"
---
# <span data-ttu-id="ee2f2-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ee2f2-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="ee2f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee2f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2f2-103">Ottiene informazioni sui set di dati in Data factory.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="ee2f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee2f2-104">SYNTAX</span></span>

### <span data-ttu-id="ee2f2-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="ee2f2-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee2f2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ee2f2-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee2f2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ee2f2-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee2f2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ee2f2-108">DESCRIPTION</span></span>
<span data-ttu-id="ee2f2-109">Il Get-AzDataFactoryV2Dataset cmdlet recupera informazioni sui set di dati in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="ee2f2-110">Se si specifica il nome di un set di dati, questo cmdlet ottiene informazioni sul set di dati.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="ee2f2-111">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i set di dati nel data factory.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="ee2f2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee2f2-112">EXAMPLES</span></span>

### <span data-ttu-id="ee2f2-113">Esempio 1: Ottenere informazioni su tutti i set di dati</span><span class="sxs-lookup"><span data-stu-id="ee2f2-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="ee2f2-114">Questo comando recupera informazioni su tutti i set di dati del data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="ee2f2-115">Esempio 2: Ottenere informazioni su un set di dati specifico</span><span class="sxs-lookup"><span data-stu-id="ee2f2-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="ee2f2-116">Questo comando recupera informazioni sul set di dati denominato DAWikipediaClickEvents nel data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="ee2f2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee2f2-117">PARAMETERS</span></span>

### <span data-ttu-id="ee2f2-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ee2f2-118">-DataFactory</span></span>
<span data-ttu-id="ee2f2-119">Specifica un oggetto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="ee2f2-120">Questo cmdlet ottiene i set di dati che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee2f2-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ee2f2-121">-DataFactoryName</span></span>
<span data-ttu-id="ee2f2-122">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ee2f2-123">Questo cmdlet ottiene i set di dati che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee2f2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2f2-124">-DefaultProfile</span></span>
<span data-ttu-id="ee2f2-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee2f2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ee2f2-126">-Name</span></span>
<span data-ttu-id="ee2f2-127">Specifica il nome del set di dati su cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-127">Specifies the name of the dataset about which to get information.</span></span>

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

### <span data-ttu-id="ee2f2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee2f2-128">-ResourceGroupName</span></span>
<span data-ttu-id="ee2f2-129">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ee2f2-130">Questo cmdlet ottiene i set di dati che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee2f2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee2f2-131">-ResourceId</span></span>
<span data-ttu-id="ee2f2-132">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ee2f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2f2-133">CommonParameters</span></span>
<span data-ttu-id="ee2f2-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee2f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2f2-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee2f2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2f2-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="ee2f2-136">INPUTS</span></span>

### <span data-ttu-id="ee2f2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ee2f2-137">System.String</span></span>

### <span data-ttu-id="ee2f2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ee2f2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ee2f2-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee2f2-139">OUTPUTS</span></span>

### <span data-ttu-id="ee2f2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="ee2f2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="ee2f2-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="ee2f2-141">NOTES</span></span>
<span data-ttu-id="ee2f2-142">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="ee2f2-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ee2f2-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee2f2-143">RELATED LINKS</span></span>

[<span data-ttu-id="ee2f2-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ee2f2-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="ee2f2-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ee2f2-145">Remove-AzDataFactoryV2Dataset</span></span>]()
