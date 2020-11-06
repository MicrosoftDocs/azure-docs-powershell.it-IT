---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 2f6dfae3d13a6de57a7dc04367ec2886be78f5f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520235"
---
# <span data-ttu-id="1d173-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1d173-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="1d173-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d173-102">SYNOPSIS</span></span>
<span data-ttu-id="1d173-103">Ottiene un'origine dati di data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1d173-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d173-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d173-104">SYNTAX</span></span>

### <span data-ttu-id="1d173-105">GetAllDataSources (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d173-105">GetAllDataSources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d173-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1d173-106">GetDataLakeStoreAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d173-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d173-107">GetBlobStorageAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d173-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d173-108">DESCRIPTION</span></span>
<span data-ttu-id="1d173-109">Il cmdlet **Get-AzureRmDataLakeAnalyticsDataSource** ottiene un'origine dati di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="1d173-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="1d173-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d173-110">EXAMPLES</span></span>

### <span data-ttu-id="1d173-111">Esempio 1: ottenere un'origine dati da un account</span><span class="sxs-lookup"><span data-stu-id="1d173-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="1d173-112">Questo comando consente di ottenere un'origine dati di data Lake Store denominata ContosoAdls da un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="1d173-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="1d173-113">Esempio 2: ottenere l'elenco degli account di data Lake Store in un account di analisi dei dati sul lago</span><span class="sxs-lookup"><span data-stu-id="1d173-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="1d173-114">Questo comando consente di ottenere tutti gli account dello Store Data Lake da un account di analisi dei dati del lago.</span><span class="sxs-lookup"><span data-stu-id="1d173-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="1d173-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d173-115">PARAMETERS</span></span>

### <span data-ttu-id="1d173-116">-Account</span><span class="sxs-lookup"><span data-stu-id="1d173-116">-Account</span></span>
<span data-ttu-id="1d173-117">Specifica l'account di analisi del lago dati che questo cmdlet ottiene le origini dati.</span><span class="sxs-lookup"><span data-stu-id="1d173-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="1d173-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="1d173-118">-Blob</span></span>
<span data-ttu-id="1d173-119">Specifica il nome dell'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d173-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d173-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d173-120">-DataLakeStore</span></span>
<span data-ttu-id="1d173-121">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1d173-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDataLakeStoreAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d173-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d173-122">-DefaultProfile</span></span>
<span data-ttu-id="1d173-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1d173-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d173-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d173-124">-ResourceGroupName</span></span>
<span data-ttu-id="1d173-125">Specifica il nome del gruppo di risorse che contiene l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="1d173-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="1d173-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d173-126">CommonParameters</span></span>
<span data-ttu-id="1d173-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d173-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d173-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d173-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d173-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d173-129">INPUTS</span></span>

### <span data-ttu-id="1d173-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1d173-130">System.String</span></span>

## <span data-ttu-id="1d173-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d173-131">OUTPUTS</span></span>

### <span data-ttu-id="1d173-132">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="1d173-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="1d173-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="1d173-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="1d173-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="1d173-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="1d173-135">Note</span><span class="sxs-lookup"><span data-stu-id="1d173-135">NOTES</span></span>

## <span data-ttu-id="1d173-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d173-136">RELATED LINKS</span></span>

[<span data-ttu-id="1d173-137">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1d173-137">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="1d173-138">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1d173-138">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="1d173-139">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1d173-139">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


