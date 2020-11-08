---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189100"
---
# <span data-ttu-id="94e2f-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="94e2f-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="94e2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="94e2f-103">Controlla l'esistenza di un elemento del catalogo.</span><span class="sxs-lookup"><span data-stu-id="94e2f-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="94e2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94e2f-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94e2f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94e2f-105">DESCRIPTION</span></span>
<span data-ttu-id="94e2f-106">Il cmdlet **test-AzDataLakeAnalyticsCatalogItem** controlla l'esistenza di un elemento del catalogo di dati di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="94e2f-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="94e2f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94e2f-107">EXAMPLES</span></span>

### <span data-ttu-id="94e2f-108">Esempio 1: verificare se un elemento del catalogo esiste</span><span class="sxs-lookup"><span data-stu-id="94e2f-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="94e2f-109">Questo comando verifica se esiste un elemento schema specificato.</span><span class="sxs-lookup"><span data-stu-id="94e2f-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="94e2f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94e2f-110">PARAMETERS</span></span>

### <span data-ttu-id="94e2f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="94e2f-111">-Account</span></span>
<span data-ttu-id="94e2f-112">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="94e2f-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="94e2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e2f-113">-DefaultProfile</span></span>
<span data-ttu-id="94e2f-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="94e2f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94e2f-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="94e2f-115">-ItemType</span></span>
<span data-ttu-id="94e2f-116">Specifica il tipo di elemento catalogo dell'elemento da controllare.</span><span class="sxs-lookup"><span data-stu-id="94e2f-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="94e2f-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="94e2f-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94e2f-118">Database</span><span class="sxs-lookup"><span data-stu-id="94e2f-118">Database</span></span>
- <span data-ttu-id="94e2f-119">Schema</span><span class="sxs-lookup"><span data-stu-id="94e2f-119">Schema</span></span>
- <span data-ttu-id="94e2f-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="94e2f-120">Assembly</span></span>
- <span data-ttu-id="94e2f-121">tavolo</span><span class="sxs-lookup"><span data-stu-id="94e2f-121">Table</span></span>
- <span data-ttu-id="94e2f-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="94e2f-122">TablePartition</span></span>
- <span data-ttu-id="94e2f-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="94e2f-123">TableValuedFunction</span></span>
- <span data-ttu-id="94e2f-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="94e2f-124">TableStatistics</span></span>
- <span data-ttu-id="94e2f-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="94e2f-125">ExternalDataSource</span></span>
- <span data-ttu-id="94e2f-126">Visualizzazione</span><span class="sxs-lookup"><span data-stu-id="94e2f-126">View</span></span>
- <span data-ttu-id="94e2f-127">Procedura</span><span class="sxs-lookup"><span data-stu-id="94e2f-127">Procedure</span></span>
- <span data-ttu-id="94e2f-128">Segreto</span><span class="sxs-lookup"><span data-stu-id="94e2f-128">Secret</span></span>
- <span data-ttu-id="94e2f-129">Credenziali</span><span class="sxs-lookup"><span data-stu-id="94e2f-129">Credential</span></span>
- <span data-ttu-id="94e2f-130">Tipi</span><span class="sxs-lookup"><span data-stu-id="94e2f-130">Types</span></span>

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

### <span data-ttu-id="94e2f-131">-Path</span><span class="sxs-lookup"><span data-stu-id="94e2f-131">-Path</span></span>
<span data-ttu-id="94e2f-132">Specifica il percorso dell'elemento da recuperare oppure il percorso dell'elemento padre degli elementi da elencare.</span><span class="sxs-lookup"><span data-stu-id="94e2f-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="94e2f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e2f-133">CommonParameters</span></span>
<span data-ttu-id="94e2f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94e2f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e2f-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94e2f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e2f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94e2f-136">INPUTS</span></span>

### <span data-ttu-id="94e2f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="94e2f-137">System.String</span></span>

### <span data-ttu-id="94e2f-138">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="94e2f-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="94e2f-139">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="94e2f-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="94e2f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94e2f-140">OUTPUTS</span></span>

### <span data-ttu-id="94e2f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94e2f-141">System.Boolean</span></span>

## <span data-ttu-id="94e2f-142">Note</span><span class="sxs-lookup"><span data-stu-id="94e2f-142">NOTES</span></span>

## <span data-ttu-id="94e2f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94e2f-143">RELATED LINKS</span></span>

[<span data-ttu-id="94e2f-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="94e2f-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


