---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: b7f2c6f2077d0b7e9c7510f6984ada15a65d6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688328"
---
# <span data-ttu-id="bd59b-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bd59b-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="bd59b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd59b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd59b-103">Ottiene un'origine dati di data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bd59b-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd59b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd59b-104">SYNTAX</span></span>

### <span data-ttu-id="bd59b-105">Elenca tutte le origini dati (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bd59b-105">List all data sources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd59b-106">Ottenere un account di data Lake Store</span><span class="sxs-lookup"><span data-stu-id="bd59b-106">Get a Data Lake Store account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd59b-107">Ottenere un account di archiviazione BLOB</span><span class="sxs-lookup"><span data-stu-id="bd59b-107">Get a Blob storage account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd59b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd59b-108">DESCRIPTION</span></span>
<span data-ttu-id="bd59b-109">Il cmdlet **Get-AzureRmDataLakeAnalyticsDataSource** ottiene un'origine dati di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="bd59b-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="bd59b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd59b-110">EXAMPLES</span></span>

### <span data-ttu-id="bd59b-111">Esempio 1: ottenere un'origine dati da un account</span><span class="sxs-lookup"><span data-stu-id="bd59b-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="bd59b-112">Questo comando consente di ottenere un'origine dati di data Lake Store denominata ContosoAdls da un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="bd59b-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="bd59b-113">Esempio 2: ottenere l'elenco degli account di data Lake Store in un account di analisi dei dati sul lago</span><span class="sxs-lookup"><span data-stu-id="bd59b-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="bd59b-114">Questo comando consente di ottenere tutti gli account dello Store Data Lake da un account di analisi dei dati del lago.</span><span class="sxs-lookup"><span data-stu-id="bd59b-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="bd59b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd59b-115">PARAMETERS</span></span>

### <span data-ttu-id="bd59b-116">-Account</span><span class="sxs-lookup"><span data-stu-id="bd59b-116">-Account</span></span>
<span data-ttu-id="bd59b-117">Specifica l'account di analisi del lago dati che questo cmdlet ottiene le origini dati.</span><span class="sxs-lookup"><span data-stu-id="bd59b-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd59b-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="bd59b-118">-Blob</span></span>
<span data-ttu-id="bd59b-119">Specifica il nome dell'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="bd59b-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd59b-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bd59b-120">-DataLakeStore</span></span>
<span data-ttu-id="bd59b-121">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bd59b-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Data Lake Store account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd59b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd59b-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd59b-123">Specifica il nome del gruppo di risorse che contiene l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="bd59b-123">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="bd59b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd59b-124">-DefaultProfile</span></span>
<span data-ttu-id="bd59b-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd59b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd59b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd59b-126">CommonParameters</span></span>
<span data-ttu-id="bd59b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd59b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd59b-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd59b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd59b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd59b-129">INPUTS</span></span>

## <span data-ttu-id="bd59b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd59b-130">OUTPUTS</span></span>

### <span data-ttu-id="bd59b-131">PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="bd59b-131">PSStorageAccountInfo</span></span>
<span data-ttu-id="bd59b-132">Dettagli dell'account di archiviazione di Azure specificati.</span><span class="sxs-lookup"><span data-stu-id="bd59b-132">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="bd59b-133">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="bd59b-133">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="bd59b-134">Dettagli dell'account dell'archivio dati specificato del lago</span><span class="sxs-lookup"><span data-stu-id="bd59b-134">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="bd59b-135">Elenco<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="bd59b-135">List<AdlDataSource></span></span>
<span data-ttu-id="bd59b-136">Elenco di account di archiviazione di Azure e di data Lake Store nell'account di analisi dei dati del lago specificato.</span><span class="sxs-lookup"><span data-stu-id="bd59b-136">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="bd59b-137">Note</span><span class="sxs-lookup"><span data-stu-id="bd59b-137">NOTES</span></span>

## <span data-ttu-id="bd59b-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd59b-138">RELATED LINKS</span></span>

[<span data-ttu-id="bd59b-139">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bd59b-139">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="bd59b-140">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bd59b-140">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="bd59b-141">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bd59b-141">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


