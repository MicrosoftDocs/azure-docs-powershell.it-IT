---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b7a608e4bed6e68f06660f10f2ef72effb6ad18b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686002"
---
# <span data-ttu-id="5585a-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="5585a-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="5585a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5585a-102">SYNOPSIS</span></span>
<span data-ttu-id="5585a-103">Ottiene un elemento o tipi di elementi del catalogo data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5585a-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5585a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5585a-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5585a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5585a-105">DESCRIPTION</span></span>
<span data-ttu-id="5585a-106">**Get-AzureRmDataLakeAnalyticsCatalogItem** ottiene un elemento del catalogo di analisi di dati di Azure Data Lake specificato o ottiene elementi del catalogo di un tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="5585a-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="5585a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5585a-107">EXAMPLES</span></span>

### <span data-ttu-id="5585a-108">Esempio 1: ottenere un database specificato</span><span class="sxs-lookup"><span data-stu-id="5585a-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="5585a-109">Questo comando ottiene il database specificato.</span><span class="sxs-lookup"><span data-stu-id="5585a-109">This command gets the specified database.</span></span>

### <span data-ttu-id="5585a-110">Esempio 2: ottenere tabelle in un database e uno schema specificati</span><span class="sxs-lookup"><span data-stu-id="5585a-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="5585a-111">Questo comando consente di ottenere un elenco di tabelle nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="5585a-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="5585a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5585a-112">PARAMETERS</span></span>

### <span data-ttu-id="5585a-113">-Account</span><span class="sxs-lookup"><span data-stu-id="5585a-113">-Account</span></span>
<span data-ttu-id="5585a-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="5585a-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5585a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5585a-115">-DefaultProfile</span></span>
<span data-ttu-id="5585a-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5585a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5585a-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="5585a-117">-ItemType</span></span>
<span data-ttu-id="5585a-118">Specifica il tipo di elemento catalogo degli elementi che vengono recuperati o elencati.</span><span class="sxs-lookup"><span data-stu-id="5585a-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="5585a-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5585a-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5585a-120">Database</span><span class="sxs-lookup"><span data-stu-id="5585a-120">Database</span></span>
- <span data-ttu-id="5585a-121">Schema</span><span class="sxs-lookup"><span data-stu-id="5585a-121">Schema</span></span>
- <span data-ttu-id="5585a-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="5585a-122">Assembly</span></span>
- <span data-ttu-id="5585a-123">tavolo</span><span class="sxs-lookup"><span data-stu-id="5585a-123">Table</span></span>
- <span data-ttu-id="5585a-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="5585a-124">TableValuedFunction</span></span>
- <span data-ttu-id="5585a-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="5585a-125">TableStatistics</span></span>
- <span data-ttu-id="5585a-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="5585a-126">ExternalDataSource</span></span>
- <span data-ttu-id="5585a-127">Visualizzazione</span><span class="sxs-lookup"><span data-stu-id="5585a-127">View</span></span>
- <span data-ttu-id="5585a-128">Procedura</span><span class="sxs-lookup"><span data-stu-id="5585a-128">Procedure</span></span>
- <span data-ttu-id="5585a-129">Segreto</span><span class="sxs-lookup"><span data-stu-id="5585a-129">Secret</span></span>
- <span data-ttu-id="5585a-130">Credenziali</span><span class="sxs-lookup"><span data-stu-id="5585a-130">Credential</span></span>
- <span data-ttu-id="5585a-131">Tipi</span><span class="sxs-lookup"><span data-stu-id="5585a-131">Types</span></span>
- <span data-ttu-id="5585a-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="5585a-132">TablePartition</span></span>

```yaml
Type: CatalogItemType
Parameter Sets: (All)
Aliases: 
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5585a-133">-Path</span><span class="sxs-lookup"><span data-stu-id="5585a-133">-Path</span></span>
<span data-ttu-id="5585a-134">Specifica il percorso multiparte dell'elemento da recuperare oppure l'elemento padre dell'elenco elementi da elencare.</span><span class="sxs-lookup"><span data-stu-id="5585a-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="5585a-135">Le parti del percorso devono essere separate da un punto (.).</span><span class="sxs-lookup"><span data-stu-id="5585a-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5585a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5585a-136">CommonParameters</span></span>
<span data-ttu-id="5585a-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5585a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5585a-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5585a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5585a-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5585a-139">INPUTS</span></span>

### <span data-ttu-id="5585a-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5585a-140">None</span></span>
<span data-ttu-id="5585a-141">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5585a-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5585a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5585a-142">OUTPUTS</span></span>

### <span data-ttu-id="5585a-143">CatalogItem</span><span class="sxs-lookup"><span data-stu-id="5585a-143">CatalogItem</span></span>
<span data-ttu-id="5585a-144">Elemento del catalogo specificato.</span><span class="sxs-lookup"><span data-stu-id="5585a-144">The specified catalog item.</span></span>

### <span data-ttu-id="5585a-145">Elenco<CatalogItem></span><span class="sxs-lookup"><span data-stu-id="5585a-145">List<CatalogItem></span></span>
<span data-ttu-id="5585a-146">Elenco degli elementi del catalogo specificati sotto il relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="5585a-146">The list of the specified catalog items underneath their corresponding container.</span></span>

## <span data-ttu-id="5585a-147">Note</span><span class="sxs-lookup"><span data-stu-id="5585a-147">NOTES</span></span>

## <span data-ttu-id="5585a-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5585a-148">RELATED LINKS</span></span>

[<span data-ttu-id="5585a-149">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="5585a-149">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


