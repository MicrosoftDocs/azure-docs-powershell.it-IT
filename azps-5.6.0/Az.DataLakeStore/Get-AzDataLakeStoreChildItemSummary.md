---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: d83e07e207c2b0e3a03c745abc874814378e5ee4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957293"
---
# <span data-ttu-id="517c5-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="517c5-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="517c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="517c5-102">SYNOPSIS</span></span>
<span data-ttu-id="517c5-103">Ottiene il riepilogo delle dimensioni totali, dei file e delle directory contenuti nel percorso specificato</span><span class="sxs-lookup"><span data-stu-id="517c5-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="517c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="517c5-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="517c5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="517c5-105">DESCRIPTION</span></span>
<span data-ttu-id="517c5-106">**Get-AzDataLakeStoreItemSummary** recupera il riepilogo del contenuto per un determinato percorso.</span><span class="sxs-lookup"><span data-stu-id="517c5-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="517c5-107">Calcola in modo ricorsivo il numero totale di file, le directory e le dimensioni totali di tutti i file nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="517c5-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="517c5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="517c5-108">EXAMPLES</span></span>

### <span data-ttu-id="517c5-109">Esempio 1: Ottenere il riepilogo del contenuto di una cartella</span><span class="sxs-lookup"><span data-stu-id="517c5-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="517c5-110">Elenca il numero totale di directory, file e relative dimensioni contenuti in /a.</span><span class="sxs-lookup"><span data-stu-id="517c5-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="517c5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="517c5-111">PARAMETERS</span></span>

### <span data-ttu-id="517c5-112">-Account</span><span class="sxs-lookup"><span data-stu-id="517c5-112">-Account</span></span>
<span data-ttu-id="517c5-113">Account Data Lake Store in cui eseguire l'operazione filesystem in</span><span class="sxs-lookup"><span data-stu-id="517c5-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="517c5-114">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="517c5-114">-Concurrency</span></span>
<span data-ttu-id="517c5-115">Indica il numero di file/directory elaborati in parallelo.</span><span class="sxs-lookup"><span data-stu-id="517c5-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="517c5-116">L'impostazione predefinita verrà calcolata come soluzione ottimale in base alle specifiche del sistema.</span><span class="sxs-lookup"><span data-stu-id="517c5-116">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="517c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="517c5-117">-DefaultProfile</span></span>
<span data-ttu-id="517c5-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="517c5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="517c5-119">-Path</span><span class="sxs-lookup"><span data-stu-id="517c5-119">-Path</span></span>
<span data-ttu-id="517c5-120">Percorso nell'account Data Lake specificato che deve essere recuperato.</span><span class="sxs-lookup"><span data-stu-id="517c5-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="517c5-121">Può essere un file o una cartella nel formato '/cartella/file.txt', dove il primo '/' dopo il DNS indica la radice del file system.</span><span class="sxs-lookup"><span data-stu-id="517c5-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="517c5-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="517c5-122">-Confirm</span></span>
<span data-ttu-id="517c5-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="517c5-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517c5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="517c5-124">-WhatIf</span></span>
<span data-ttu-id="517c5-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="517c5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="517c5-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="517c5-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517c5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517c5-127">CommonParameters</span></span>
<span data-ttu-id="517c5-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="517c5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517c5-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="517c5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517c5-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="517c5-130">INPUTS</span></span>

### <span data-ttu-id="517c5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="517c5-131">System.String</span></span>

### <span data-ttu-id="517c5-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="517c5-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="517c5-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="517c5-133">System.Int32</span></span>

## <span data-ttu-id="517c5-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="517c5-134">OUTPUTS</span></span>

### <span data-ttu-id="517c5-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemSummary</span><span class="sxs-lookup"><span data-stu-id="517c5-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="517c5-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="517c5-136">NOTES</span></span>

## <span data-ttu-id="517c5-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="517c5-137">RELATED LINKS</span></span>
