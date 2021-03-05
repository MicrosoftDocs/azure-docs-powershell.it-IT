---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 016c2520ee97f03c19a68eefebdc0319bacdb6e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006845"
---
# <span data-ttu-id="0cd4a-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="0cd4a-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="0cd4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cd4a-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd4a-103">Ottiene un'origine dati Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0cd4a-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="0cd4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0cd4a-104">SYNTAX</span></span>

### <span data-ttu-id="0cd4a-105">GetAllDataSources (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0cd4a-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cd4a-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0cd4a-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cd4a-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0cd4a-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cd4a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0cd4a-108">DESCRIPTION</span></span>
<span data-ttu-id="0cd4a-109">Il cmdlet **Get-AzDataLakeAnalyticsDataSource** ottiene un'origine dati Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0cd4a-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="0cd4a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0cd4a-110">EXAMPLES</span></span>

### <span data-ttu-id="0cd4a-111">Esempio 1: Ottenere un'origine dati da un account</span><span class="sxs-lookup"><span data-stu-id="0cd4a-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="0cd4a-112">Questo comando recupera un'origine dati Data Lake Store denominata ContosoAdls da un account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0cd4a-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="0cd4a-113">Esempio 2: Ottenere l'elenco di account Data Lake Store in un account Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="0cd4a-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="0cd4a-114">Questo comando recupera tutti gli account di Data Lake Store da un account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0cd4a-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0cd4a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cd4a-115">PARAMETERS</span></span>

### <span data-ttu-id="0cd4a-116">-Account</span><span class="sxs-lookup"><span data-stu-id="0cd4a-116">-Account</span></span>
<span data-ttu-id="0cd4a-117">Specifica all'account Data Lake Analytics che questo cmdlet ottiene le origini dati.</span><span class="sxs-lookup"><span data-stu-id="0cd4a-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="0cd4a-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="0cd4a-118">-Blob</span></span>
<span data-ttu-id="0cd4a-119">Specifica il nome dell'origine dati Archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="0cd4a-119">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="0cd4a-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0cd4a-120">-DataLakeStore</span></span>
<span data-ttu-id="0cd4a-121">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0cd4a-121">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0cd4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd4a-122">-DefaultProfile</span></span>
<span data-ttu-id="0cd4a-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0cd4a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cd4a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cd4a-124">-ResourceGroupName</span></span>
<span data-ttu-id="0cd4a-125">Specifica il nome del gruppo di risorse che contiene l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="0cd4a-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="0cd4a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd4a-126">CommonParameters</span></span>
<span data-ttu-id="0cd4a-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd4a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd4a-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd4a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd4a-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="0cd4a-129">INPUTS</span></span>

### <span data-ttu-id="0cd4a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0cd4a-130">System.String</span></span>

## <span data-ttu-id="0cd4a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0cd4a-131">OUTPUTS</span></span>

### <span data-ttu-id="0cd4a-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="0cd4a-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="0cd4a-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="0cd4a-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="0cd4a-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="0cd4a-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="0cd4a-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="0cd4a-135">NOTES</span></span>

## <span data-ttu-id="0cd4a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0cd4a-136">RELATED LINKS</span></span>

[<span data-ttu-id="0cd4a-137">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="0cd4a-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="0cd4a-138">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="0cd4a-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="0cd4a-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="0cd4a-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


