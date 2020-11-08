---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: ddb291a72d3c35c79321ddefa0832d46c489998f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020761"
---
# <span data-ttu-id="59181-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="59181-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="59181-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59181-102">SYNOPSIS</span></span>
<span data-ttu-id="59181-103">Aggiunge un'origine dati a un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="59181-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="59181-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59181-104">SYNTAX</span></span>

### <span data-ttu-id="59181-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59181-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59181-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59181-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59181-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59181-107">DESCRIPTION</span></span>
<span data-ttu-id="59181-108">Il cmdlet **Add-AzDataLakeAnalyticsDataSource** aggiunge un'origine dati a un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="59181-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="59181-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59181-109">EXAMPLES</span></span>

### <span data-ttu-id="59181-110">Esempio 1: aggiungere un'origine dati a un account</span><span class="sxs-lookup"><span data-stu-id="59181-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="59181-111">Questo comando aggiunge un'origine dati di data Lake Store a un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="59181-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="59181-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59181-112">PARAMETERS</span></span>

### <span data-ttu-id="59181-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="59181-113">-AccessKey</span></span>
<span data-ttu-id="59181-114">Specifica il codice di accesso dell'account di archiviazione BLOB di Azure da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="59181-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59181-115">-Account</span><span class="sxs-lookup"><span data-stu-id="59181-115">-Account</span></span>
<span data-ttu-id="59181-116">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="59181-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="59181-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="59181-117">-Blob</span></span>
<span data-ttu-id="59181-118">Specifica il nome dell'account di archiviazione BLOB di Azure da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="59181-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59181-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59181-119">-DataLakeStore</span></span>
<span data-ttu-id="59181-120">Specifica il nome dell'account di Azure Data Lake Store da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="59181-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59181-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59181-121">-DefaultProfile</span></span>
<span data-ttu-id="59181-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="59181-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59181-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59181-123">-ResourceGroupName</span></span>
<span data-ttu-id="59181-124">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="59181-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59181-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59181-125">CommonParameters</span></span>
<span data-ttu-id="59181-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59181-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59181-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59181-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59181-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59181-128">INPUTS</span></span>

### <span data-ttu-id="59181-129">System. String</span><span class="sxs-lookup"><span data-stu-id="59181-129">System.String</span></span>

## <span data-ttu-id="59181-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59181-130">OUTPUTS</span></span>

### <span data-ttu-id="59181-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="59181-131">System.Object</span></span>
## <span data-ttu-id="59181-132">Note</span><span class="sxs-lookup"><span data-stu-id="59181-132">NOTES</span></span>

## <span data-ttu-id="59181-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59181-133">RELATED LINKS</span></span>

[<span data-ttu-id="59181-134">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="59181-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="59181-135">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="59181-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


