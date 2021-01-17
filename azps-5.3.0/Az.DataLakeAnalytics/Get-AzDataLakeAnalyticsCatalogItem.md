---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487499"
---
# <span data-ttu-id="eb64f-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="eb64f-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="eb64f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb64f-102">SYNOPSIS</span></span>
<span data-ttu-id="eb64f-103">Ottiene un elemento o tipi di elementi del catalogo data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="eb64f-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="eb64f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb64f-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb64f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb64f-105">DESCRIPTION</span></span>
<span data-ttu-id="eb64f-106">**Get-AzDataLakeAnalyticsCatalogItem** ottiene un elemento del catalogo di analisi di dati di Azure Data Lake specificato o ottiene elementi del catalogo di un tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="eb64f-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="eb64f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb64f-107">EXAMPLES</span></span>

### <span data-ttu-id="eb64f-108">Esempio 1: ottenere un database specificato</span><span class="sxs-lookup"><span data-stu-id="eb64f-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="eb64f-109">Questo comando ottiene il database specificato.</span><span class="sxs-lookup"><span data-stu-id="eb64f-109">This command gets the specified database.</span></span>

### <span data-ttu-id="eb64f-110">Esempio 2: ottenere tabelle in un database e uno schema specificati</span><span class="sxs-lookup"><span data-stu-id="eb64f-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="eb64f-111">Questo comando consente di ottenere un elenco di tabelle nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="eb64f-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="eb64f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb64f-112">PARAMETERS</span></span>

### <span data-ttu-id="eb64f-113">-Account</span><span class="sxs-lookup"><span data-stu-id="eb64f-113">-Account</span></span>
<span data-ttu-id="eb64f-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="eb64f-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="eb64f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb64f-115">-DefaultProfile</span></span>
<span data-ttu-id="eb64f-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="eb64f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb64f-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="eb64f-117">-ItemType</span></span>
<span data-ttu-id="eb64f-118">Specifica il tipo di elemento catalogo degli elementi che vengono recuperati o elencati.</span><span class="sxs-lookup"><span data-stu-id="eb64f-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="eb64f-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="eb64f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb64f-120">Database</span><span class="sxs-lookup"><span data-stu-id="eb64f-120">Database</span></span>
- <span data-ttu-id="eb64f-121">Schema</span><span class="sxs-lookup"><span data-stu-id="eb64f-121">Schema</span></span>
- <span data-ttu-id="eb64f-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="eb64f-122">Assembly</span></span>
- <span data-ttu-id="eb64f-123">tavolo</span><span class="sxs-lookup"><span data-stu-id="eb64f-123">Table</span></span>
- <span data-ttu-id="eb64f-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="eb64f-124">TableValuedFunction</span></span>
- <span data-ttu-id="eb64f-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="eb64f-125">TableStatistics</span></span>
- <span data-ttu-id="eb64f-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="eb64f-126">ExternalDataSource</span></span>
- <span data-ttu-id="eb64f-127">Visualizzazione</span><span class="sxs-lookup"><span data-stu-id="eb64f-127">View</span></span>
- <span data-ttu-id="eb64f-128">Procedura</span><span class="sxs-lookup"><span data-stu-id="eb64f-128">Procedure</span></span>
- <span data-ttu-id="eb64f-129">Segreto</span><span class="sxs-lookup"><span data-stu-id="eb64f-129">Secret</span></span>
- <span data-ttu-id="eb64f-130">Credenziali</span><span class="sxs-lookup"><span data-stu-id="eb64f-130">Credential</span></span>
- <span data-ttu-id="eb64f-131">Tipi</span><span class="sxs-lookup"><span data-stu-id="eb64f-131">Types</span></span>
- <span data-ttu-id="eb64f-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="eb64f-132">TablePartition</span></span>

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

### <span data-ttu-id="eb64f-133">-Path</span><span class="sxs-lookup"><span data-stu-id="eb64f-133">-Path</span></span>
<span data-ttu-id="eb64f-134">Specifica il percorso multiparte dell'elemento da recuperare oppure l'elemento padre dell'elenco elementi da elencare.</span><span class="sxs-lookup"><span data-stu-id="eb64f-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="eb64f-135">Le parti del percorso devono essere separate da un punto (.).</span><span class="sxs-lookup"><span data-stu-id="eb64f-135">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="eb64f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb64f-136">CommonParameters</span></span>
<span data-ttu-id="eb64f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb64f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb64f-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb64f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb64f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb64f-139">INPUTS</span></span>

### <span data-ttu-id="eb64f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="eb64f-140">System.String</span></span>

### <span data-ttu-id="eb64f-141">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="eb64f-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="eb64f-142">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="eb64f-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="eb64f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb64f-143">OUTPUTS</span></span>

### <span data-ttu-id="eb64f-144">Microsoft. Azure. Management. datalake. Analytics. Models. CatalogItem</span><span class="sxs-lookup"><span data-stu-id="eb64f-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="eb64f-145">Note</span><span class="sxs-lookup"><span data-stu-id="eb64f-145">NOTES</span></span>

## <span data-ttu-id="eb64f-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb64f-146">RELATED LINKS</span></span>

[<span data-ttu-id="eb64f-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="eb64f-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


