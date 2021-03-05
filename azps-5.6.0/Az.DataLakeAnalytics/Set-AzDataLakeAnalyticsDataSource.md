---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: cb51b1c703d527a2888bd0e80d8cc7a50d044e36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962366"
---
# <span data-ttu-id="753cf-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="753cf-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="753cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="753cf-102">SYNOPSIS</span></span>
<span data-ttu-id="753cf-103">Modifica i dettagli di un'origine dati di un account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="753cf-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="753cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="753cf-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="753cf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="753cf-105">DESCRIPTION</span></span>
<span data-ttu-id="753cf-106">Il cmdlet **Set-AzDataLakeAnalyticsDataSource** modifica i dettagli di un'origine dati di un account Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="753cf-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="753cf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="753cf-107">EXAMPLES</span></span>

### <span data-ttu-id="753cf-108">Esempio 1: Cambiare la chiave di accesso per un'origine dati</span><span class="sxs-lookup"><span data-stu-id="753cf-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="753cf-109">Questo comando modifica la chiave di accesso archiviata per un'origine dati di Archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="753cf-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="753cf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="753cf-110">PARAMETERS</span></span>

### <span data-ttu-id="753cf-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="753cf-111">-AccessKey</span></span>
<span data-ttu-id="753cf-112">Specifica la nuova chiave di accesso dell'origine dati Archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="753cf-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="753cf-113">-Account</span><span class="sxs-lookup"><span data-stu-id="753cf-113">-Account</span></span>
<span data-ttu-id="753cf-114">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="753cf-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="753cf-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="753cf-115">-Blob</span></span>
<span data-ttu-id="753cf-116">Specifica il nome dell'origine dati Archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="753cf-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="753cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="753cf-117">-DefaultProfile</span></span>
<span data-ttu-id="753cf-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="753cf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="753cf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="753cf-119">-ResourceGroupName</span></span>
<span data-ttu-id="753cf-120">Specifica il nome del gruppo di risorse dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="753cf-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="753cf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="753cf-121">CommonParameters</span></span>
<span data-ttu-id="753cf-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="753cf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="753cf-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="753cf-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="753cf-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="753cf-124">INPUTS</span></span>

### <span data-ttu-id="753cf-125">System.String</span><span class="sxs-lookup"><span data-stu-id="753cf-125">System.String</span></span>

## <span data-ttu-id="753cf-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="753cf-126">OUTPUTS</span></span>

### <span data-ttu-id="753cf-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="753cf-127">System.Void</span></span>

## <span data-ttu-id="753cf-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="753cf-128">NOTES</span></span>

## <span data-ttu-id="753cf-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="753cf-129">RELATED LINKS</span></span>

[<span data-ttu-id="753cf-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="753cf-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="753cf-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="753cf-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


