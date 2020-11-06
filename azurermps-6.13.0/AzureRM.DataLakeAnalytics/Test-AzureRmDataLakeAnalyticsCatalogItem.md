---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 1cada55b8db886d85f88d34254c8814cdfc44665
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518751"
---
# <span data-ttu-id="b76c2-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="b76c2-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="b76c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b76c2-102">SYNOPSIS</span></span>
<span data-ttu-id="b76c2-103">Controlla l'esistenza di un elemento del catalogo.</span><span class="sxs-lookup"><span data-stu-id="b76c2-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b76c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b76c2-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b76c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b76c2-105">DESCRIPTION</span></span>
<span data-ttu-id="b76c2-106">Il cmdlet **test-AzureRmDataLakeAnalyticsCatalogItem** controlla l'esistenza di un elemento del catalogo di dati di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="b76c2-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="b76c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b76c2-107">EXAMPLES</span></span>

### <span data-ttu-id="b76c2-108">Esempio 1: verificare se un elemento del catalogo esiste</span><span class="sxs-lookup"><span data-stu-id="b76c2-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="b76c2-109">Questo comando verifica se esiste un elemento schema specificato.</span><span class="sxs-lookup"><span data-stu-id="b76c2-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="b76c2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b76c2-110">PARAMETERS</span></span>

### <span data-ttu-id="b76c2-111">-Account</span><span class="sxs-lookup"><span data-stu-id="b76c2-111">-Account</span></span>
<span data-ttu-id="b76c2-112">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="b76c2-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="b76c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76c2-113">-DefaultProfile</span></span>
<span data-ttu-id="b76c2-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b76c2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b76c2-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="b76c2-115">-ItemType</span></span>
<span data-ttu-id="b76c2-116">Specifica il tipo di elemento catalogo dell'elemento da controllare.</span><span class="sxs-lookup"><span data-stu-id="b76c2-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="b76c2-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b76c2-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b76c2-118">Database</span><span class="sxs-lookup"><span data-stu-id="b76c2-118">Database</span></span>
- <span data-ttu-id="b76c2-119">Schema</span><span class="sxs-lookup"><span data-stu-id="b76c2-119">Schema</span></span>
- <span data-ttu-id="b76c2-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="b76c2-120">Assembly</span></span>
- <span data-ttu-id="b76c2-121">tavolo</span><span class="sxs-lookup"><span data-stu-id="b76c2-121">Table</span></span>
- <span data-ttu-id="b76c2-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="b76c2-122">TablePartition</span></span>
- <span data-ttu-id="b76c2-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="b76c2-123">TableValuedFunction</span></span>
- <span data-ttu-id="b76c2-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="b76c2-124">TableStatistics</span></span>
- <span data-ttu-id="b76c2-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="b76c2-125">ExternalDataSource</span></span>
- <span data-ttu-id="b76c2-126">Visualizzazione</span><span class="sxs-lookup"><span data-stu-id="b76c2-126">View</span></span>
- <span data-ttu-id="b76c2-127">Procedura</span><span class="sxs-lookup"><span data-stu-id="b76c2-127">Procedure</span></span>
- <span data-ttu-id="b76c2-128">Segreto</span><span class="sxs-lookup"><span data-stu-id="b76c2-128">Secret</span></span>
- <span data-ttu-id="b76c2-129">Credenziali</span><span class="sxs-lookup"><span data-stu-id="b76c2-129">Credential</span></span>
- <span data-ttu-id="b76c2-130">Tipi</span><span class="sxs-lookup"><span data-stu-id="b76c2-130">Types</span></span>

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

### <span data-ttu-id="b76c2-131">-Path</span><span class="sxs-lookup"><span data-stu-id="b76c2-131">-Path</span></span>
<span data-ttu-id="b76c2-132">Specifica il percorso dell'elemento da recuperare oppure il percorso dell'elemento padre degli elementi da elencare.</span><span class="sxs-lookup"><span data-stu-id="b76c2-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b76c2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76c2-133">CommonParameters</span></span>
<span data-ttu-id="b76c2-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76c2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76c2-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b76c2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76c2-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b76c2-136">INPUTS</span></span>

### <span data-ttu-id="b76c2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b76c2-137">System.String</span></span>

### <span data-ttu-id="b76c2-138">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="b76c2-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="b76c2-139">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="b76c2-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="b76c2-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b76c2-140">OUTPUTS</span></span>

### <span data-ttu-id="b76c2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b76c2-141">System.Boolean</span></span>

## <span data-ttu-id="b76c2-142">Note</span><span class="sxs-lookup"><span data-stu-id="b76c2-142">NOTES</span></span>

## <span data-ttu-id="b76c2-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b76c2-143">RELATED LINKS</span></span>

[<span data-ttu-id="b76c2-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="b76c2-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


