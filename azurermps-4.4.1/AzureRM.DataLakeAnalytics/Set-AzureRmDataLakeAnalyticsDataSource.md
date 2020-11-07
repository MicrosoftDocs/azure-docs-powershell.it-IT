---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 258db8a7dc1d771b73ea4c4fa373b1861847b820
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687230"
---
# <span data-ttu-id="cb58a-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cb58a-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="cb58a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb58a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb58a-103">Modifica i dettagli di un'origine dati di un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="cb58a-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb58a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb58a-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb58a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb58a-105">DESCRIPTION</span></span>
<span data-ttu-id="cb58a-106">Il cmdlet **set-AzureRmDataLakeAnalyticsDataSource** modifica i dettagli di un'origine dati di un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="cb58a-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="cb58a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb58a-107">EXAMPLES</span></span>

### <span data-ttu-id="cb58a-108">Esempio 1: cambiare il tasto di scelta per un'origine dati</span><span class="sxs-lookup"><span data-stu-id="cb58a-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="cb58a-109">Questo comando modifica il tasto di scelta archiviato per un'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="cb58a-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="cb58a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb58a-110">PARAMETERS</span></span>

### <span data-ttu-id="cb58a-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="cb58a-111">-AccessKey</span></span>
<span data-ttu-id="cb58a-112">Specifica il nuovo codice di accesso dell'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="cb58a-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="cb58a-113">-Account</span><span class="sxs-lookup"><span data-stu-id="cb58a-113">-Account</span></span>
<span data-ttu-id="cb58a-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="cb58a-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="cb58a-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="cb58a-115">-Blob</span></span>
<span data-ttu-id="cb58a-116">Specifica il nome dell'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="cb58a-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="cb58a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb58a-117">-ResourceGroupName</span></span>
<span data-ttu-id="cb58a-118">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="cb58a-118">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="cb58a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb58a-119">-DefaultProfile</span></span>
<span data-ttu-id="cb58a-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb58a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb58a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb58a-121">CommonParameters</span></span>
<span data-ttu-id="cb58a-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb58a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb58a-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb58a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb58a-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb58a-124">INPUTS</span></span>

## <span data-ttu-id="cb58a-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb58a-125">OUTPUTS</span></span>

### <span data-ttu-id="cb58a-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cb58a-126">None</span></span>

## <span data-ttu-id="cb58a-127">Note</span><span class="sxs-lookup"><span data-stu-id="cb58a-127">NOTES</span></span>

## <span data-ttu-id="cb58a-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb58a-128">RELATED LINKS</span></span>

[<span data-ttu-id="cb58a-129">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cb58a-129">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="cb58a-130">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cb58a-130">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


