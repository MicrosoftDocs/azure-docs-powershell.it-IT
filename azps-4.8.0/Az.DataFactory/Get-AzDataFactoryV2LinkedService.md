---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: ac3a45f9e150d65829a222e75e7072c6a2bdcd1e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94193007"
---
# <span data-ttu-id="66933-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="66933-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="66933-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66933-102">SYNOPSIS</span></span>
<span data-ttu-id="66933-103">Ottiene informazioni sui servizi collegati in data factory.</span><span class="sxs-lookup"><span data-stu-id="66933-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="66933-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66933-104">SYNTAX</span></span>

### <span data-ttu-id="66933-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="66933-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66933-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="66933-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66933-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="66933-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66933-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66933-108">DESCRIPTION</span></span>
<span data-ttu-id="66933-109">Il cmdlet Get-AzDataFactoryV2LinkedService ottiene informazioni sui servizi collegati in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="66933-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="66933-110">Se specifichi il nome di un servizio collegato, questo cmdlet ottiene le informazioni sul servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="66933-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="66933-111">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i servizi collegati nella Factory di dati.</span><span class="sxs-lookup"><span data-stu-id="66933-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="66933-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66933-112">EXAMPLES</span></span>

### <span data-ttu-id="66933-113">Esempio 1: ottenere informazioni su tutti i servizi collegati</span><span class="sxs-lookup"><span data-stu-id="66933-113">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="66933-114">Questo comando consente di ottenere informazioni su tutti i servizi collegati nella Factory di dati denominata WikiADF e quindi di passare i servizi collegati al cmdlet Format-List usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="66933-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="66933-115">Il cmdlet di Windows PowerShell formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="66933-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="66933-116">Per altre informazioni, digitare Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="66933-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="66933-117">Puoi usare uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="66933-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="66933-118">Esempio 2: ottenere informazioni su un servizio collegato specifico</span><span class="sxs-lookup"><span data-stu-id="66933-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="66933-119">Questo comando consente di ottenere informazioni sul servizio collegato denominato LinkedServiceCuratedWikiData nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="66933-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="66933-120">Esempio 3: ottenere informazioni su uno specifico servizio collegato specificando il parametro DataFactory</span><span class="sxs-lookup"><span data-stu-id="66933-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="66933-121">Il primo comando usa il cmdlet Get-AzDataFactoryV2 per ottenere la data factory denominata ContosoFactory e lo archivia nella variabile $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="66933-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="66933-122">Il secondo comando recupera le informazioni sul servizio collegato per la factory di dati archiviata in $DataFactory e quindi passa tali informazioni al cmdlet Format-Table tramite l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="66933-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="66933-123">Il cmdlet Format-Table formatta l'output come DataSet con le proprietà specificate come colonne del set di dati.</span><span class="sxs-lookup"><span data-stu-id="66933-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="66933-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66933-124">PARAMETERS</span></span>

### <span data-ttu-id="66933-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="66933-125">-DataFactory</span></span>
<span data-ttu-id="66933-126">Specifica un oggetto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="66933-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="66933-127">Questo cmdlet ottiene i servizi collegati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="66933-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="66933-128">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="66933-128">-DataFactoryName</span></span>
<span data-ttu-id="66933-129">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="66933-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="66933-130">Questo cmdlet ottiene i servizi collegati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="66933-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="66933-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66933-131">-DefaultProfile</span></span>
<span data-ttu-id="66933-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66933-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66933-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="66933-133">-Name</span></span>
<span data-ttu-id="66933-134">Specifica il nome del servizio collegato che consente di ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="66933-134">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66933-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66933-135">-ResourceGroupName</span></span>
<span data-ttu-id="66933-136">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="66933-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="66933-137">Questo cmdlet ottiene i servizi collegati che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="66933-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="66933-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66933-138">-ResourceId</span></span>
<span data-ttu-id="66933-139">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="66933-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="66933-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66933-140">CommonParameters</span></span>
<span data-ttu-id="66933-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66933-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66933-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66933-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66933-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66933-143">INPUTS</span></span>

### <span data-ttu-id="66933-144">System. String</span><span class="sxs-lookup"><span data-stu-id="66933-144">System.String</span></span>

### <span data-ttu-id="66933-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="66933-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="66933-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66933-146">OUTPUTS</span></span>

### <span data-ttu-id="66933-147">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="66933-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="66933-148">Note</span><span class="sxs-lookup"><span data-stu-id="66933-148">NOTES</span></span>
<span data-ttu-id="66933-149">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="66933-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="66933-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66933-150">RELATED LINKS</span></span>

[<span data-ttu-id="66933-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="66933-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="66933-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="66933-152">Remove-AzDataFactoryV2LinkedService</span></span>]()