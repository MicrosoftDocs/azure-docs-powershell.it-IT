---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 8aae62ccbf79f2b3c59f6009aa5233daf00853fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518755"
---
# <span data-ttu-id="d324f-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="d324f-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="d324f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d324f-102">SYNOPSIS</span></span>
<span data-ttu-id="d324f-103">Modifica i dettagli di un'origine dati di un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="d324f-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d324f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d324f-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d324f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d324f-105">DESCRIPTION</span></span>
<span data-ttu-id="d324f-106">Il cmdlet **set-AzureRmDataLakeAnalyticsDataSource** modifica i dettagli di un'origine dati di un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="d324f-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d324f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d324f-107">EXAMPLES</span></span>

### <span data-ttu-id="d324f-108">Esempio 1: cambiare il tasto di scelta per un'origine dati</span><span class="sxs-lookup"><span data-stu-id="d324f-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="d324f-109">Questo comando modifica il tasto di scelta archiviato per un'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="d324f-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="d324f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d324f-110">PARAMETERS</span></span>

### <span data-ttu-id="d324f-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="d324f-111">-AccessKey</span></span>
<span data-ttu-id="d324f-112">Specifica il nuovo codice di accesso dell'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="d324f-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d324f-113">-Account</span><span class="sxs-lookup"><span data-stu-id="d324f-113">-Account</span></span>
<span data-ttu-id="d324f-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="d324f-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d324f-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="d324f-115">-Blob</span></span>
<span data-ttu-id="d324f-116">Specifica il nome dell'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="d324f-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d324f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d324f-117">-DefaultProfile</span></span>
<span data-ttu-id="d324f-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d324f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d324f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d324f-119">-ResourceGroupName</span></span>
<span data-ttu-id="d324f-120">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="d324f-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="d324f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d324f-121">CommonParameters</span></span>
<span data-ttu-id="d324f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d324f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d324f-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d324f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d324f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d324f-124">INPUTS</span></span>

### <span data-ttu-id="d324f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d324f-125">System.String</span></span>

## <span data-ttu-id="d324f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d324f-126">OUTPUTS</span></span>

### <span data-ttu-id="d324f-127">System. void</span><span class="sxs-lookup"><span data-stu-id="d324f-127">System.Void</span></span>

## <span data-ttu-id="d324f-128">Note</span><span class="sxs-lookup"><span data-stu-id="d324f-128">NOTES</span></span>

## <span data-ttu-id="d324f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d324f-129">RELATED LINKS</span></span>

[<span data-ttu-id="d324f-130">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="d324f-130">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="d324f-131">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="d324f-131">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


