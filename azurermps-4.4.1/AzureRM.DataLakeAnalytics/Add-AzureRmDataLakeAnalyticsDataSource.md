---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: a3eff47b688f2f426c4f255d400ce1ef73c3c027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510684"
---
# <span data-ttu-id="7b2b9-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7b2b9-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="7b2b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b2b9-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2b9-103">Aggiunge un'origine dati a un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b2b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b2b9-104">SYNTAX</span></span>

### <span data-ttu-id="7b2b9-105">Aggiungere un account di archiviazione dati per i laghi</span><span class="sxs-lookup"><span data-stu-id="7b2b9-105">Add a Data Lake storage account</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b2b9-106">Aggiungere un account di archiviazione BLOB</span><span class="sxs-lookup"><span data-stu-id="7b2b9-106">Add a Blob storage account</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b2b9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b2b9-107">DESCRIPTION</span></span>
<span data-ttu-id="7b2b9-108">Il cmdlet **Add-AzureRmDataLakeAnalyticsDataSource** aggiunge un'origine dati a un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7b2b9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b2b9-109">EXAMPLES</span></span>

### <span data-ttu-id="7b2b9-110">Esempio 1: aggiungere un'origine dati a un account</span><span class="sxs-lookup"><span data-stu-id="7b2b9-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="7b2b9-111">Questo comando aggiunge un'origine dati di data Lake Store a un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="7b2b9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b2b9-112">PARAMETERS</span></span>

### <span data-ttu-id="7b2b9-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="7b2b9-113">-AccessKey</span></span>
<span data-ttu-id="7b2b9-114">Specifica il codice di accesso dell'account di archiviazione BLOB di Azure da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Blob storage account
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b2b9-115">-Account</span><span class="sxs-lookup"><span data-stu-id="7b2b9-115">-Account</span></span>
<span data-ttu-id="7b2b9-116">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="7b2b9-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="7b2b9-117">-Blob</span></span>
<span data-ttu-id="7b2b9-118">Specifica il nome dell'account di archiviazione BLOB di Azure da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b2b9-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7b2b9-119">-DataLakeStore</span></span>
<span data-ttu-id="7b2b9-120">Specifica il nome dell'account di Azure Data Lake Store da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Data Lake storage account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b2b9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b2b9-121">-ResourceGroupName</span></span>
<span data-ttu-id="7b2b9-122">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-122">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="7b2b9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2b9-123">-DefaultProfile</span></span>
<span data-ttu-id="7b2b9-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b2b9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2b9-125">CommonParameters</span></span>
<span data-ttu-id="7b2b9-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b2b9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2b9-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b2b9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2b9-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b2b9-128">INPUTS</span></span>

## <span data-ttu-id="7b2b9-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b2b9-129">OUTPUTS</span></span>

### <span data-ttu-id="7b2b9-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7b2b9-130">None</span></span>

## <span data-ttu-id="7b2b9-131">Note</span><span class="sxs-lookup"><span data-stu-id="7b2b9-131">NOTES</span></span>

## <span data-ttu-id="7b2b9-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b2b9-132">RELATED LINKS</span></span>

[<span data-ttu-id="7b2b9-133">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7b2b9-133">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="7b2b9-134">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7b2b9-134">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


