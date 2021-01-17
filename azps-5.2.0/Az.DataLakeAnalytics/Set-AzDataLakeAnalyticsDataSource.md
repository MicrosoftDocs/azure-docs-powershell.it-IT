---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 0dd0dfb25959ed3a5753ae6bd19b0500d4742634
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345367"
---
# <span data-ttu-id="e52ea-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="e52ea-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="e52ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e52ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e52ea-103">Modifica i dettagli di un'origine dati di un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="e52ea-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="e52ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e52ea-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e52ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e52ea-105">DESCRIPTION</span></span>
<span data-ttu-id="e52ea-106">Il cmdlet **set-AzDataLakeAnalyticsDataSource** modifica i dettagli di un'origine dati di un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="e52ea-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e52ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e52ea-107">EXAMPLES</span></span>

### <span data-ttu-id="e52ea-108">Esempio 1: cambiare il tasto di scelta per un'origine dati</span><span class="sxs-lookup"><span data-stu-id="e52ea-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="e52ea-109">Questo comando modifica il tasto di scelta archiviato per un'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="e52ea-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="e52ea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e52ea-110">PARAMETERS</span></span>

### <span data-ttu-id="e52ea-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="e52ea-111">-AccessKey</span></span>
<span data-ttu-id="e52ea-112">Specifica il nuovo codice di accesso dell'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="e52ea-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="e52ea-113">-Account</span><span class="sxs-lookup"><span data-stu-id="e52ea-113">-Account</span></span>
<span data-ttu-id="e52ea-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="e52ea-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e52ea-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="e52ea-115">-Blob</span></span>
<span data-ttu-id="e52ea-116">Specifica il nome dell'origine dati di archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="e52ea-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="e52ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e52ea-117">-DefaultProfile</span></span>
<span data-ttu-id="e52ea-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e52ea-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e52ea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e52ea-119">-ResourceGroupName</span></span>
<span data-ttu-id="e52ea-120">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="e52ea-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="e52ea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e52ea-121">CommonParameters</span></span>
<span data-ttu-id="e52ea-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e52ea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e52ea-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e52ea-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e52ea-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e52ea-124">INPUTS</span></span>

### <span data-ttu-id="e52ea-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e52ea-125">System.String</span></span>

## <span data-ttu-id="e52ea-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e52ea-126">OUTPUTS</span></span>

### <span data-ttu-id="e52ea-127">System. void</span><span class="sxs-lookup"><span data-stu-id="e52ea-127">System.Void</span></span>

## <span data-ttu-id="e52ea-128">Note</span><span class="sxs-lookup"><span data-stu-id="e52ea-128">NOTES</span></span>

## <span data-ttu-id="e52ea-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e52ea-129">RELATED LINKS</span></span>

[<span data-ttu-id="e52ea-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="e52ea-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="e52ea-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="e52ea-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


