---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 8068a560954d94a134205d5e67eab19e641bed74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518780"
---
# <span data-ttu-id="e04db-101">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e04db-101">Get-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="e04db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e04db-102">SYNOPSIS</span></span>
<span data-ttu-id="e04db-103">Ottiene informazioni sui servizi collegati in data factory.</span><span class="sxs-lookup"><span data-stu-id="e04db-103">Gets information about linked services in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e04db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e04db-104">SYNTAX</span></span>

### <span data-ttu-id="e04db-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e04db-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e04db-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e04db-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e04db-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e04db-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e04db-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e04db-108">DESCRIPTION</span></span>
<span data-ttu-id="e04db-109">Il cmdlet Get-AzureRmDataFactoryV2LinkedService ottiene informazioni sui servizi collegati in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e04db-109">The Get-AzureRmDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="e04db-110">Se specifichi il nome di un servizio collegato, questo cmdlet ottiene le informazioni sul servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="e04db-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="e04db-111">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i servizi collegati nella Factory di dati.</span><span class="sxs-lookup"><span data-stu-id="e04db-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="e04db-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e04db-112">EXAMPLES</span></span>

### <span data-ttu-id="e04db-113">Esempio 1: ottenere informazioni su tutti i servizi collegati</span><span class="sxs-lookup"><span data-stu-id="e04db-113">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

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

<span data-ttu-id="e04db-114">Questo comando consente di ottenere informazioni su tutti i servizi collegati nella Factory di dati denominata WikiADF e quindi di passare i servizi collegati al cmdlet Format-List usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="e04db-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e04db-115">Il cmdlet di Windows PowerShell formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="e04db-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="e04db-116">Per altre informazioni, digitare Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="e04db-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="e04db-117">Puoi usare uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e04db-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="e04db-118">Esempio 2: ottenere informazioni su un servizio collegato specifico</span><span class="sxs-lookup"><span data-stu-id="e04db-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="e04db-119">Questo comando consente di ottenere informazioni sul servizio collegato denominato LinkedServiceCuratedWikiData nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e04db-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="e04db-120">Esempio 3: ottenere informazioni su uno specifico servizio collegato specificando il parametro DataFactory</span><span class="sxs-lookup"><span data-stu-id="e04db-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="e04db-121">Il primo comando usa il cmdlet Get-AzureRmDataFactoryV2 per ottenere la data factory denominata ContosoFactory e lo archivia nella variabile $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="e04db-121">The first command uses the Get-AzureRmDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="e04db-122">Il secondo comando recupera le informazioni sul servizio collegato per la factory di dati archiviata in $DataFactory e quindi passa tali informazioni al cmdlet Format-Table tramite l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="e04db-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e04db-123">Il cmdlet Format-Table formatta l'output come DataSet con le proprietà specificate come colonne del set di dati.</span><span class="sxs-lookup"><span data-stu-id="e04db-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="e04db-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e04db-124">PARAMETERS</span></span>

### <span data-ttu-id="e04db-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e04db-125">-DataFactory</span></span>
<span data-ttu-id="e04db-126">Specifica un oggetto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="e04db-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="e04db-127">Questo cmdlet ottiene i servizi collegati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e04db-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e04db-128">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e04db-128">-DataFactoryName</span></span>
<span data-ttu-id="e04db-129">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="e04db-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e04db-130">Questo cmdlet ottiene i servizi collegati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e04db-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e04db-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04db-131">-DefaultProfile</span></span>
<span data-ttu-id="e04db-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e04db-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e04db-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="e04db-133">-Name</span></span>
<span data-ttu-id="e04db-134">Specifica il nome del servizio collegato che consente di ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="e04db-134">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="e04db-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e04db-135">-ResourceGroupName</span></span>
<span data-ttu-id="e04db-136">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="e04db-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e04db-137">Questo cmdlet ottiene i servizi collegati che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e04db-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e04db-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e04db-138">-ResourceId</span></span>
<span data-ttu-id="e04db-139">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="e04db-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e04db-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04db-140">CommonParameters</span></span>
<span data-ttu-id="e04db-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e04db-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04db-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e04db-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04db-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e04db-143">INPUTS</span></span>

### <span data-ttu-id="e04db-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e04db-144">System.String</span></span>

### <span data-ttu-id="e04db-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e04db-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="e04db-146">Parametri: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e04db-146">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="e04db-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e04db-147">OUTPUTS</span></span>

### <span data-ttu-id="e04db-148">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="e04db-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="e04db-149">Note</span><span class="sxs-lookup"><span data-stu-id="e04db-149">NOTES</span></span>
<span data-ttu-id="e04db-150">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="e04db-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e04db-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e04db-151">RELATED LINKS</span></span>

[<span data-ttu-id="e04db-152">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e04db-152">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="e04db-153">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e04db-153">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
