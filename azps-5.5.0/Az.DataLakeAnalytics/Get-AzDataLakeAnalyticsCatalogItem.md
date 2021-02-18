---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180974"
---
# <span data-ttu-id="e27a9-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="e27a9-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="e27a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e27a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e27a9-103">Ottiene un elemento del catalogo Data Lake Analytics o tipi di elementi.</span><span class="sxs-lookup"><span data-stu-id="e27a9-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="e27a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e27a9-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e27a9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e27a9-105">DESCRIPTION</span></span>
<span data-ttu-id="e27a9-106">**Get-AzDataLakeAnalyticsCatalogItem** ottiene un elemento del catalogo Azure Data Lake Analytics specificato o elementi del catalogo di un tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="e27a9-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="e27a9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e27a9-107">EXAMPLES</span></span>

### <span data-ttu-id="e27a9-108">Esempio 1: Ottenere un database specificato</span><span class="sxs-lookup"><span data-stu-id="e27a9-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="e27a9-109">Questo comando recupera il database specificato.</span><span class="sxs-lookup"><span data-stu-id="e27a9-109">This command gets the specified database.</span></span>

### <span data-ttu-id="e27a9-110">Esempio 2: Recuperare tabelle in un database e uno schema specificati</span><span class="sxs-lookup"><span data-stu-id="e27a9-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="e27a9-111">Questo comando ottiene un elenco di tabelle nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="e27a9-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="e27a9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e27a9-112">PARAMETERS</span></span>

### <span data-ttu-id="e27a9-113">-Account</span><span class="sxs-lookup"><span data-stu-id="e27a9-113">-Account</span></span>
<span data-ttu-id="e27a9-114">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e27a9-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e27a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27a9-115">-DefaultProfile</span></span>
<span data-ttu-id="e27a9-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e27a9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e27a9-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="e27a9-117">-ItemType</span></span>
<span data-ttu-id="e27a9-118">Specifica il tipo di elemento di catalogo degli elementi in fase di recupero o di elenco.</span><span class="sxs-lookup"><span data-stu-id="e27a9-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="e27a9-119">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="e27a9-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e27a9-120">Database</span><span class="sxs-lookup"><span data-stu-id="e27a9-120">Database</span></span>
- <span data-ttu-id="e27a9-121">Schema</span><span class="sxs-lookup"><span data-stu-id="e27a9-121">Schema</span></span>
- <span data-ttu-id="e27a9-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="e27a9-122">Assembly</span></span>
- <span data-ttu-id="e27a9-123">tavolo</span><span class="sxs-lookup"><span data-stu-id="e27a9-123">Table</span></span>
- <span data-ttu-id="e27a9-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="e27a9-124">TableValuedFunction</span></span>
- <span data-ttu-id="e27a9-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="e27a9-125">TableStatistics</span></span>
- <span data-ttu-id="e27a9-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="e27a9-126">ExternalDataSource</span></span>
- <span data-ttu-id="e27a9-127">Visualizza</span><span class="sxs-lookup"><span data-stu-id="e27a9-127">View</span></span>
- <span data-ttu-id="e27a9-128">Procedura</span><span class="sxs-lookup"><span data-stu-id="e27a9-128">Procedure</span></span>
- <span data-ttu-id="e27a9-129">Segreto</span><span class="sxs-lookup"><span data-stu-id="e27a9-129">Secret</span></span>
- <span data-ttu-id="e27a9-130">Credenziali</span><span class="sxs-lookup"><span data-stu-id="e27a9-130">Credential</span></span>
- <span data-ttu-id="e27a9-131">Tipi</span><span class="sxs-lookup"><span data-stu-id="e27a9-131">Types</span></span>
- <span data-ttu-id="e27a9-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="e27a9-132">TablePartition</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e27a9-133">-Path</span><span class="sxs-lookup"><span data-stu-id="e27a9-133">-Path</span></span>
<span data-ttu-id="e27a9-134">Specifica il percorso multi part dell'elemento da recuperare o dell'elemento padre degli elementi da elencare.</span><span class="sxs-lookup"><span data-stu-id="e27a9-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="e27a9-135">Le parti del percorso devono essere separate da un punto (.).</span><span class="sxs-lookup"><span data-stu-id="e27a9-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e27a9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e27a9-136">CommonParameters</span></span>
<span data-ttu-id="e27a9-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e27a9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e27a9-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e27a9-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e27a9-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="e27a9-139">INPUTS</span></span>

### <span data-ttu-id="e27a9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e27a9-140">System.String</span></span>

### <span data-ttu-id="e27a9-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="e27a9-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="e27a9-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="e27a9-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="e27a9-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e27a9-143">OUTPUTS</span></span>

### <span data-ttu-id="e27a9-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span><span class="sxs-lookup"><span data-stu-id="e27a9-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="e27a9-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="e27a9-145">NOTES</span></span>

## <span data-ttu-id="e27a9-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e27a9-146">RELATED LINKS</span></span>

[<span data-ttu-id="e27a9-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="e27a9-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


