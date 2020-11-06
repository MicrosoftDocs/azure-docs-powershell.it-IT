---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: e873a7f4a825ed84172d098dfa0f8cb631cc3f7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514383"
---
# <span data-ttu-id="a21ef-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a21ef-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="a21ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a21ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a21ef-103">Modifica i dettagli di un'origine dati di un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="a21ef-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a21ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a21ef-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a21ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a21ef-105">DESCRIPTION</span></span>
<span data-ttu-id="a21ef-106">Il cmdlet **set-AzureRmDataLakeAnalyticsDataSource** modifica i dettagli di un'origine dati di un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a21ef-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a21ef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a21ef-107">EXAMPLES</span></span>

### <span data-ttu-id="a21ef-108">Esempio 1: cambiare il tasto di scelta per un'origine dati</span><span class="sxs-lookup"><span data-stu-id="a21ef-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="a21ef-109">Questo comando modifica il tasto di scelta archiviato per un'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="a21ef-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="a21ef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a21ef-110">PARAMETERS</span></span>

### <span data-ttu-id="a21ef-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="a21ef-111">-AccessKey</span></span>
<span data-ttu-id="a21ef-112">Specifica il nuovo codice di accesso dell'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="a21ef-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-113">-Account</span><span class="sxs-lookup"><span data-stu-id="a21ef-113">-Account</span></span>
<span data-ttu-id="a21ef-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="a21ef-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a21ef-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="a21ef-115">-Blob</span></span>
<span data-ttu-id="a21ef-116">Specifica il nome dell'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="a21ef-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a21ef-117">-DefaultProfile</span></span>
<span data-ttu-id="a21ef-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a21ef-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a21ef-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a21ef-119">-ResourceGroupName</span></span>
<span data-ttu-id="a21ef-120">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="a21ef-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a21ef-121">CommonParameters</span></span>
<span data-ttu-id="a21ef-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a21ef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a21ef-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a21ef-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a21ef-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a21ef-124">INPUTS</span></span>

### <span data-ttu-id="a21ef-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a21ef-125">None</span></span>
<span data-ttu-id="a21ef-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a21ef-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a21ef-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a21ef-127">OUTPUTS</span></span>

### <span data-ttu-id="a21ef-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a21ef-128">None</span></span>

## <span data-ttu-id="a21ef-129">Note</span><span class="sxs-lookup"><span data-stu-id="a21ef-129">NOTES</span></span>

## <span data-ttu-id="a21ef-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a21ef-130">RELATED LINKS</span></span>

[<span data-ttu-id="a21ef-131">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a21ef-131">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="a21ef-132">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a21ef-132">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


