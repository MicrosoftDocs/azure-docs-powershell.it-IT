---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 249ef7ae66436d4bf82b3b038aa8b1201f68110e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686585"
---
# <span data-ttu-id="342d9-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="342d9-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="342d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="342d9-102">SYNOPSIS</span></span>
<span data-ttu-id="342d9-103">Controlla l'esistenza di un elemento del catalogo.</span><span class="sxs-lookup"><span data-stu-id="342d9-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="342d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="342d9-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="342d9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="342d9-105">DESCRIPTION</span></span>
<span data-ttu-id="342d9-106">Il cmdlet **test-AzureRmDataLakeAnalyticsCatalogItem** controlla l'esistenza di un elemento del catalogo di dati di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="342d9-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="342d9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="342d9-107">EXAMPLES</span></span>

### <span data-ttu-id="342d9-108">Esempio 1: verificare se un elemento del catalogo esiste</span><span class="sxs-lookup"><span data-stu-id="342d9-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="342d9-109">Questo comando verifica se esiste un elemento schema specificato.</span><span class="sxs-lookup"><span data-stu-id="342d9-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="342d9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="342d9-110">PARAMETERS</span></span>

### <span data-ttu-id="342d9-111">-Account</span><span class="sxs-lookup"><span data-stu-id="342d9-111">-Account</span></span>
<span data-ttu-id="342d9-112">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="342d9-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="342d9-113">-ItemType</span><span class="sxs-lookup"><span data-stu-id="342d9-113">-ItemType</span></span>
<span data-ttu-id="342d9-114">Specifica il tipo di elemento catalogo dell'elemento da controllare.</span><span class="sxs-lookup"><span data-stu-id="342d9-114">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="342d9-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="342d9-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="342d9-116">Database</span><span class="sxs-lookup"><span data-stu-id="342d9-116">Database</span></span>
- <span data-ttu-id="342d9-117">Schema</span><span class="sxs-lookup"><span data-stu-id="342d9-117">Schema</span></span>
- <span data-ttu-id="342d9-118">Assembly</span><span class="sxs-lookup"><span data-stu-id="342d9-118">Assembly</span></span>
- <span data-ttu-id="342d9-119">tavolo</span><span class="sxs-lookup"><span data-stu-id="342d9-119">Table</span></span>
- <span data-ttu-id="342d9-120">TablePartition</span><span class="sxs-lookup"><span data-stu-id="342d9-120">TablePartition</span></span>
- <span data-ttu-id="342d9-121">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="342d9-121">TableValuedFunction</span></span>
- <span data-ttu-id="342d9-122">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="342d9-122">TableStatistics</span></span>
- <span data-ttu-id="342d9-123">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="342d9-123">ExternalDataSource</span></span>
- <span data-ttu-id="342d9-124">Visualizzazione</span><span class="sxs-lookup"><span data-stu-id="342d9-124">View</span></span>
- <span data-ttu-id="342d9-125">Procedura</span><span class="sxs-lookup"><span data-stu-id="342d9-125">Procedure</span></span>
- <span data-ttu-id="342d9-126">Segreto</span><span class="sxs-lookup"><span data-stu-id="342d9-126">Secret</span></span>
- <span data-ttu-id="342d9-127">Credenziali</span><span class="sxs-lookup"><span data-stu-id="342d9-127">Credential</span></span>
- <span data-ttu-id="342d9-128">Tipi</span><span class="sxs-lookup"><span data-stu-id="342d9-128">Types</span></span>

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

### <span data-ttu-id="342d9-129">-Path</span><span class="sxs-lookup"><span data-stu-id="342d9-129">-Path</span></span>
<span data-ttu-id="342d9-130">Specifica il percorso dell'elemento da recuperare oppure il percorso dell'elemento padre degli elementi da elencare.</span><span class="sxs-lookup"><span data-stu-id="342d9-130">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="342d9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342d9-131">-DefaultProfile</span></span>
<span data-ttu-id="342d9-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="342d9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="342d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342d9-133">CommonParameters</span></span>
<span data-ttu-id="342d9-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="342d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342d9-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="342d9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342d9-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="342d9-136">INPUTS</span></span>

## <span data-ttu-id="342d9-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="342d9-137">OUTPUTS</span></span>

### <span data-ttu-id="342d9-138">bool</span><span class="sxs-lookup"><span data-stu-id="342d9-138">bool</span></span>
<span data-ttu-id="342d9-139">Vero o falso che indica se l'elemento di catalogo specificato esiste o meno.</span><span class="sxs-lookup"><span data-stu-id="342d9-139">True or false indicating if the specified catalog item exists or not.</span></span>

## <span data-ttu-id="342d9-140">Note</span><span class="sxs-lookup"><span data-stu-id="342d9-140">NOTES</span></span>

## <span data-ttu-id="342d9-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="342d9-141">RELATED LINKS</span></span>

[<span data-ttu-id="342d9-142">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="342d9-142">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


