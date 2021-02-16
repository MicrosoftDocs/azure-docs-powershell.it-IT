---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204370"
---
# <span data-ttu-id="cac3c-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="cac3c-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="cac3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cac3c-102">SYNOPSIS</span></span>
<span data-ttu-id="cac3c-103">Cerca le voci eliminate nel Cestino che corrispondono al filtro.</span><span class="sxs-lookup"><span data-stu-id="cac3c-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="cac3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cac3c-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cac3c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cac3c-105">DESCRIPTION</span></span>
<span data-ttu-id="cac3c-106">Il **cmdlet Get-AzDataLakeStoreDeletedItem** cerca nei file o nelle cartelle eliminate in Data Lake Store che corrispondono al filtro specificato.</span><span class="sxs-lookup"><span data-stu-id="cac3c-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="cac3c-107">Vengono visualizzati gli attributi seguenti degli elementi eliminati: OriginalPath, TrashDirPath, Type, CreationTime.</span><span class="sxs-lookup"><span data-stu-id="cac3c-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="cac3c-108">Potrebbe trattarsi di un'operazione a esecuzione lunga, perché potrebbe essere necessario cercare milioni di file nel Cestino e potrebbe essere eseguita come processo.</span><span class="sxs-lookup"><span data-stu-id="cac3c-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="cac3c-109">Attenzione: l'annullamento dell'eliminazione dei file è un'operazione ottimale.</span><span class="sxs-lookup"><span data-stu-id="cac3c-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="cac3c-110">Non ci sono garanzie che un file possa essere ripristinato dopo l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="cac3c-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="cac3c-111">L'uso di questa API è abilitato tramite l'elenco degli elementi vuoti.</span><span class="sxs-lookup"><span data-stu-id="cac3c-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="cac3c-112">Se l'account ADL non è presente nell'elenco degli account, l'uso di questa API genererà un'eccezione Not implementata.</span><span class="sxs-lookup"><span data-stu-id="cac3c-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="cac3c-113">Per altre informazioni e assistenza, contattare il supporto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cac3c-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="cac3c-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cac3c-114">EXAMPLES</span></span>

### <span data-ttu-id="cac3c-115">Esempio: Ottenere i dettagli di un file da Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="cac3c-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="cac3c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cac3c-116">PARAMETERS</span></span>

### <span data-ttu-id="cac3c-117">-Account</span><span class="sxs-lookup"><span data-stu-id="cac3c-117">-Account</span></span>
<span data-ttu-id="cac3c-118">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cac3c-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="cac3c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cac3c-119">-AsJob</span></span>
<span data-ttu-id="cac3c-120">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="cac3c-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="cac3c-121">-Count</span><span class="sxs-lookup"><span data-stu-id="cac3c-121">-Count</span></span>
<span data-ttu-id="cac3c-122">Specifica il numero di risultati che l'utente vuole trovare.</span><span class="sxs-lookup"><span data-stu-id="cac3c-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="cac3c-123">La query viene eseguita finché non vengono trovati i risultati di Count o la ricerca viene eseguita nell'intero Cestino, a seconda dell'evento che si verifica per primo.</span><span class="sxs-lookup"><span data-stu-id="cac3c-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

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

### <span data-ttu-id="cac3c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac3c-124">-DefaultProfile</span></span>
<span data-ttu-id="cac3c-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cac3c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cac3c-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="cac3c-126">-Filter</span></span>
<span data-ttu-id="cac3c-127">Specifica la query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="cac3c-127">Specifies the search query.</span></span> <span data-ttu-id="cac3c-128">Un valore più specifico fornisce risultati più pertinenti.</span><span class="sxs-lookup"><span data-stu-id="cac3c-128">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="cac3c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac3c-129">CommonParameters</span></span>
<span data-ttu-id="cac3c-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cac3c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac3c-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cac3c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac3c-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="cac3c-132">INPUTS</span></span>

### <span data-ttu-id="cac3c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cac3c-133">System.String</span></span>

## <span data-ttu-id="cac3c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cac3c-134">OUTPUTS</span></span>

### <span data-ttu-id="cac3c-135">System.Collections.generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="cac3c-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="cac3c-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="cac3c-136">NOTES</span></span>

## <span data-ttu-id="cac3c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cac3c-137">RELATED LINKS</span></span>

[<span data-ttu-id="cac3c-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="cac3c-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)