---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 7034e17e119acb1077cf17dca85ded8a40cb2e2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516799"
---
# <span data-ttu-id="3085e-101">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="3085e-101">Get-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="3085e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3085e-102">SYNOPSIS</span></span>
<span data-ttu-id="3085e-103">Ottiene informazioni sui servizi collegati in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3085e-103">Gets information about linked services in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3085e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3085e-104">SYNTAX</span></span>

### <span data-ttu-id="3085e-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3085e-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3085e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3085e-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3085e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3085e-107">DESCRIPTION</span></span>
<span data-ttu-id="3085e-108">Il cmdlet **Get-AzureRmDataFactoryLinkedService** ottiene le informazioni sui servizi collegati in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3085e-108">The **Get-AzureRmDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="3085e-109">Se specifichi il nome di un servizio collegato, questo cmdlet ottiene le informazioni sul servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="3085e-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="3085e-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i servizi collegati nella Factory di dati.</span><span class="sxs-lookup"><span data-stu-id="3085e-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="3085e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3085e-111">EXAMPLES</span></span>

### <span data-ttu-id="3085e-112">Esempio 1: ottenere informazioni su tutti i servizi collegati</span><span class="sxs-lookup"><span data-stu-id="3085e-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="3085e-113">Questo comando consente di ottenere informazioni su tutti i servizi collegati nella Factory di dati denominata WikiADF e quindi di passare i servizi collegati al cmdlet Format-List usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="3085e-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3085e-114">Questo cmdlet formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="3085e-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="3085e-115">Per altre informazioni, digitare `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="3085e-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="3085e-116">Esempio 2: ottenere informazioni su un servizio collegato specifico</span><span class="sxs-lookup"><span data-stu-id="3085e-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="3085e-117">Questo comando consente di ottenere informazioni sul servizio collegato denominato HDILinkedService nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3085e-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="3085e-118">Esempio 3: ottenere informazioni su uno specifico servizio collegato specificando il parametro DataFactory</span><span class="sxs-lookup"><span data-stu-id="3085e-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzureRmDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="3085e-119">Il primo comando usa il cmdlet Get-AzureRmDataFactory per ottenere la data factory denominata ContosoFactory e lo archivia nella variabile $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="3085e-119">The first command uses the Get-AzureRmDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="3085e-120">Il secondo comando recupera le informazioni sul servizio collegato per la factory di dati archiviata in $DataFactory e quindi passa tali informazioni al cmdlet Format-Table tramite l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="3085e-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3085e-121">**Format-Table** formatta l'output come DataSet con le proprietà specificate come colonne del set di dati.</span><span class="sxs-lookup"><span data-stu-id="3085e-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="3085e-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3085e-122">PARAMETERS</span></span>

### <span data-ttu-id="3085e-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3085e-123">-DataFactory</span></span>
<span data-ttu-id="3085e-124">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="3085e-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3085e-125">Questo cmdlet ottiene i servizi collegati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3085e-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3085e-126">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3085e-126">-DataFactoryName</span></span>
<span data-ttu-id="3085e-127">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="3085e-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3085e-128">Questo cmdlet ottiene i servizi collegati che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3085e-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3085e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3085e-129">-DefaultProfile</span></span>
<span data-ttu-id="3085e-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3085e-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3085e-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="3085e-131">-Name</span></span>
<span data-ttu-id="3085e-132">Specifica il nome del servizio collegato che consente di ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="3085e-132">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="3085e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3085e-133">-ResourceGroupName</span></span>
<span data-ttu-id="3085e-134">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="3085e-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3085e-135">Questo cmdlet ottiene i servizi collegati che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3085e-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3085e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3085e-136">CommonParameters</span></span>
<span data-ttu-id="3085e-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3085e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3085e-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3085e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3085e-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3085e-139">INPUTS</span></span>

### <span data-ttu-id="3085e-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3085e-140">None</span></span>
<span data-ttu-id="3085e-141">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3085e-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3085e-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3085e-142">OUTPUTS</span></span>

### <span data-ttu-id="3085e-143">System. Collections. Generic. list ' 1 [[Microsoft. WindowsAzure. Commands. Utilities. PSLinkedService, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft. WindowsAzure. Commands. Utilities. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="3085e-143">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService</span></span>

## <span data-ttu-id="3085e-144">Note</span><span class="sxs-lookup"><span data-stu-id="3085e-144">NOTES</span></span>
* <span data-ttu-id="3085e-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="3085e-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3085e-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3085e-146">RELATED LINKS</span></span>

[<span data-ttu-id="3085e-147">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="3085e-147">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="3085e-148">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="3085e-148">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)


