---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 0dd0dfb25959ed3a5753ae6bd19b0500d4742634
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194750"
---
# <span data-ttu-id="95ad9-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="95ad9-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="95ad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95ad9-102">SYNOPSIS</span></span>
<span data-ttu-id="95ad9-103">Modifica i dettagli di un'origine dati di un account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="95ad9-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="95ad9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95ad9-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95ad9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="95ad9-105">DESCRIPTION</span></span>
<span data-ttu-id="95ad9-106">Il cmdlet **Set-AzDataLakeAnalyticsDataSource** modifica i dettagli di un'origine dati di un account Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="95ad9-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="95ad9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95ad9-107">EXAMPLES</span></span>

### <span data-ttu-id="95ad9-108">Esempio 1: Cambiare la chiave di accesso per un'origine dati</span><span class="sxs-lookup"><span data-stu-id="95ad9-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="95ad9-109">Questo comando modifica la chiave di accesso archiviata per un'origine dati di Archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="95ad9-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="95ad9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95ad9-110">PARAMETERS</span></span>

### <span data-ttu-id="95ad9-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="95ad9-111">-AccessKey</span></span>
<span data-ttu-id="95ad9-112">Specifica la nuova chiave di accesso dell'origine dati Archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="95ad9-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="95ad9-113">-Account</span><span class="sxs-lookup"><span data-stu-id="95ad9-113">-Account</span></span>
<span data-ttu-id="95ad9-114">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="95ad9-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="95ad9-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="95ad9-115">-Blob</span></span>
<span data-ttu-id="95ad9-116">Specifica il nome dell'origine dati Archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="95ad9-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="95ad9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ad9-117">-DefaultProfile</span></span>
<span data-ttu-id="95ad9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="95ad9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95ad9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ad9-119">-ResourceGroupName</span></span>
<span data-ttu-id="95ad9-120">Specifica il nome del gruppo di risorse dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="95ad9-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="95ad9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ad9-121">CommonParameters</span></span>
<span data-ttu-id="95ad9-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ad9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ad9-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95ad9-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ad9-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="95ad9-124">INPUTS</span></span>

### <span data-ttu-id="95ad9-125">System.String</span><span class="sxs-lookup"><span data-stu-id="95ad9-125">System.String</span></span>

## <span data-ttu-id="95ad9-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95ad9-126">OUTPUTS</span></span>

### <span data-ttu-id="95ad9-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="95ad9-127">System.Void</span></span>

## <span data-ttu-id="95ad9-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="95ad9-128">NOTES</span></span>

## <span data-ttu-id="95ad9-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95ad9-129">RELATED LINKS</span></span>

[<span data-ttu-id="95ad9-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="95ad9-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="95ad9-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="95ad9-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


