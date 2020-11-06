---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 93e64c4a64eecbe66fc3f9b2923ade65405a05a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508191"
---
# <span data-ttu-id="7ed06-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7ed06-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="7ed06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ed06-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed06-103">Ottiene un'origine dati di data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7ed06-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ed06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ed06-104">SYNTAX</span></span>

### <span data-ttu-id="7ed06-105">GetAllDataSources (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7ed06-105">GetAllDataSources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ed06-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7ed06-106">GetDataLakeStoreAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ed06-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ed06-107">GetBlobStorageAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ed06-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ed06-108">DESCRIPTION</span></span>
<span data-ttu-id="7ed06-109">Il cmdlet **Get-AzureRmDataLakeAnalyticsDataSource** ottiene un'origine dati di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="7ed06-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="7ed06-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ed06-110">EXAMPLES</span></span>

### <span data-ttu-id="7ed06-111">Esempio 1: ottenere un'origine dati da un account</span><span class="sxs-lookup"><span data-stu-id="7ed06-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="7ed06-112">Questo comando consente di ottenere un'origine dati di data Lake Store denominata ContosoAdls da un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="7ed06-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="7ed06-113">Esempio 2: ottenere l'elenco degli account di data Lake Store in un account di analisi dei dati sul lago</span><span class="sxs-lookup"><span data-stu-id="7ed06-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="7ed06-114">Questo comando consente di ottenere tutti gli account dello Store Data Lake da un account di analisi dei dati del lago.</span><span class="sxs-lookup"><span data-stu-id="7ed06-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="7ed06-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ed06-115">PARAMETERS</span></span>

### <span data-ttu-id="7ed06-116">-Account</span><span class="sxs-lookup"><span data-stu-id="7ed06-116">-Account</span></span>
<span data-ttu-id="7ed06-117">Specifica l'account di analisi del lago dati che questo cmdlet ottiene le origini dati.</span><span class="sxs-lookup"><span data-stu-id="7ed06-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed06-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="7ed06-118">-Blob</span></span>
<span data-ttu-id="7ed06-119">Specifica il nome dell'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed06-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed06-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ed06-120">-DataLakeStore</span></span>
<span data-ttu-id="7ed06-121">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7ed06-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: GetDataLakeStoreAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed06-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed06-122">-DefaultProfile</span></span>
<span data-ttu-id="7ed06-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7ed06-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ed06-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed06-124">-ResourceGroupName</span></span>
<span data-ttu-id="7ed06-125">Specifica il nome del gruppo di risorse che contiene l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="7ed06-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="7ed06-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed06-126">CommonParameters</span></span>
<span data-ttu-id="7ed06-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed06-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed06-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ed06-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed06-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ed06-129">INPUTS</span></span>

### <span data-ttu-id="7ed06-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7ed06-130">None</span></span>
<span data-ttu-id="7ed06-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7ed06-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7ed06-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ed06-132">OUTPUTS</span></span>

### <span data-ttu-id="7ed06-133">PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="7ed06-133">PSStorageAccountInfo</span></span>
<span data-ttu-id="7ed06-134">Dettagli dell'account di archiviazione di Azure specificati.</span><span class="sxs-lookup"><span data-stu-id="7ed06-134">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="7ed06-135">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="7ed06-135">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="7ed06-136">Dettagli dell'account dell'archivio dati specificato del lago</span><span class="sxs-lookup"><span data-stu-id="7ed06-136">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="7ed06-137">Elenco<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="7ed06-137">List<AdlDataSource></span></span>
<span data-ttu-id="7ed06-138">Elenco di account di archiviazione di Azure e di data Lake Store nell'account di analisi dei dati del lago specificato.</span><span class="sxs-lookup"><span data-stu-id="7ed06-138">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="7ed06-139">Note</span><span class="sxs-lookup"><span data-stu-id="7ed06-139">NOTES</span></span>

## <span data-ttu-id="7ed06-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ed06-140">RELATED LINKS</span></span>

[<span data-ttu-id="7ed06-141">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7ed06-141">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="7ed06-142">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7ed06-142">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="7ed06-143">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7ed06-143">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


