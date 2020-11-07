---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 750203e954ef96619e32b63ffd6eae333bb852f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674813"
---
# <span data-ttu-id="c844d-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="c844d-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="c844d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c844d-102">SYNOPSIS</span></span>
<span data-ttu-id="c844d-103">Cerca le voci eliminate nel cestino che corrispondono al filtro.</span><span class="sxs-lookup"><span data-stu-id="c844d-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="c844d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c844d-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c844d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c844d-105">DESCRIPTION</span></span>
<span data-ttu-id="c844d-106">Il cmdlet **Get-AzDataLakeStoreDeletedItem** esegue la ricerca nei file o nelle cartelle eliminati in data Lake Store che corrispondono al filtro indicato.</span><span class="sxs-lookup"><span data-stu-id="c844d-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="c844d-107">Vengono visualizzati gli attributi seguenti degli elementi eliminati-OriginalPath, TrashDirPath, Type, CreationTime.</span><span class="sxs-lookup"><span data-stu-id="c844d-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="c844d-108">Potrebbe essere un'operazione a esecuzione prolungata perché potrebbe essere necessario eseguire ricerche in milioni di file nel cestino e può essere eseguito come processo.</span><span class="sxs-lookup"><span data-stu-id="c844d-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>

## <span data-ttu-id="c844d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c844d-109">EXAMPLES</span></span>

### <span data-ttu-id="c844d-110">Esempio: ottenere i dettagli di un file da data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c844d-110">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="c844d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c844d-111">PARAMETERS</span></span>

### <span data-ttu-id="c844d-112">-Account</span><span class="sxs-lookup"><span data-stu-id="c844d-112">-Account</span></span>
<span data-ttu-id="c844d-113">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c844d-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c844d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c844d-114">-AsJob</span></span>
<span data-ttu-id="c844d-115">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="c844d-115">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c844d-116">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="c844d-116">-Count</span></span>
<span data-ttu-id="c844d-117">Specifica il numero di risultati che l'utente vuole trovare.</span><span class="sxs-lookup"><span data-stu-id="c844d-117">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="c844d-118">La query viene eseguita fino a quando non trova i risultati del conteggio oppure esegue la ricerca in un intero cestino, a seconda del caso.</span><span class="sxs-lookup"><span data-stu-id="c844d-118">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c844d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c844d-119">-DefaultProfile</span></span>
<span data-ttu-id="c844d-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c844d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c844d-121">-Filtro</span><span class="sxs-lookup"><span data-stu-id="c844d-121">-Filter</span></span>
<span data-ttu-id="c844d-122">Specifica la query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c844d-122">Specifies the search query.</span></span> <span data-ttu-id="c844d-123">Un valore più specifico fornisce risultati più rilevanti.</span><span class="sxs-lookup"><span data-stu-id="c844d-123">A more specific value gives more relevant results.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c844d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c844d-124">CommonParameters</span></span>
<span data-ttu-id="c844d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c844d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c844d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c844d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c844d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c844d-127">INPUTS</span></span>

### <span data-ttu-id="c844d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c844d-128">System.String</span></span>

## <span data-ttu-id="c844d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c844d-129">OUTPUTS</span></span>

### <span data-ttu-id="c844d-130">System. Collections. Generic. list<Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="c844d-130">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="c844d-131">Note</span><span class="sxs-lookup"><span data-stu-id="c844d-131">NOTES</span></span>

## <span data-ttu-id="c844d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c844d-132">RELATED LINKS</span></span>

[<span data-ttu-id="c844d-133">Ripristinare-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="c844d-133">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)