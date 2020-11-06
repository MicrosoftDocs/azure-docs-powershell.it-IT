---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
ms.openlocfilehash: 83fb8b3ea5fdf9ad63983d2a3a3d23d402fbb5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520642"
---
# <span data-ttu-id="b054a-101">Get-AzureRmDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="b054a-101">Get-AzureRmDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="b054a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b054a-102">SYNOPSIS</span></span>
<span data-ttu-id="b054a-103">Ottiene il riepilogo delle dimensioni totali, dei file e delle directory contenuti nel percorso specificato</span><span class="sxs-lookup"><span data-stu-id="b054a-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b054a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b054a-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b054a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b054a-105">DESCRIPTION</span></span>
<span data-ttu-id="b054a-106">Il **Get-AzureRmDataLakeStoreChildItemSummary** Recupera il riepilogo del contenuto per un percorso specifico.</span><span class="sxs-lookup"><span data-stu-id="b054a-106">The **Get-AzureRmDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="b054a-107">Calcola ricorsivamente il numero totale di file, directory e dimensioni totali di tutti i file nel percorso indicato.</span><span class="sxs-lookup"><span data-stu-id="b054a-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="b054a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b054a-108">EXAMPLES</span></span>

### <span data-ttu-id="b054a-109">Esempio 1: ottenere il riepilogo del contenuto di una cartella</span><span class="sxs-lookup"><span data-stu-id="b054a-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="b054a-110">Elenca il numero totale di directory, file e le relative dimensioni contenute in/a.</span><span class="sxs-lookup"><span data-stu-id="b054a-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="b054a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b054a-111">PARAMETERS</span></span>

### <span data-ttu-id="b054a-112">-Account</span><span class="sxs-lookup"><span data-stu-id="b054a-112">-Account</span></span>
<span data-ttu-id="b054a-113">L'account di data Lake Store per eseguire l'operazione filesystem in</span><span class="sxs-lookup"><span data-stu-id="b054a-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="b054a-114">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="b054a-114">-Concurrency</span></span>
<span data-ttu-id="b054a-115">Indica il numero di file/directory elaborati in parallelo.</span><span class="sxs-lookup"><span data-stu-id="b054a-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="b054a-116">L'impostazione predefinita verrà calcolata come uno sforzo ottimale in base alle specifiche di sistema.</span><span class="sxs-lookup"><span data-stu-id="b054a-116">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="b054a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b054a-117">-DefaultProfile</span></span>
<span data-ttu-id="b054a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b054a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b054a-119">-Path</span><span class="sxs-lookup"><span data-stu-id="b054a-119">-Path</span></span>
<span data-ttu-id="b054a-120">Il percorso nell'account del lago dati specificato che deve essere recuperato.</span><span class="sxs-lookup"><span data-stu-id="b054a-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="b054a-121">Può essere un file o una cartella nel formato "/folder/file.txt", in cui il primo "/" dopo il DNS indica la radice del file System.</span><span class="sxs-lookup"><span data-stu-id="b054a-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="b054a-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b054a-122">-Confirm</span></span>
<span data-ttu-id="b054a-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b054a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b054a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b054a-124">-WhatIf</span></span>
<span data-ttu-id="b054a-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b054a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b054a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b054a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b054a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b054a-127">CommonParameters</span></span>
<span data-ttu-id="b054a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b054a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b054a-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b054a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b054a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b054a-130">INPUTS</span></span>

### <span data-ttu-id="b054a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b054a-131">System.String</span></span>

### <span data-ttu-id="b054a-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b054a-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b054a-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b054a-133">System.Int32</span></span>

## <span data-ttu-id="b054a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b054a-134">OUTPUTS</span></span>

### <span data-ttu-id="b054a-135">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="b054a-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="b054a-136">Note</span><span class="sxs-lookup"><span data-stu-id="b054a-136">NOTES</span></span>

## <span data-ttu-id="b054a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b054a-137">RELATED LINKS</span></span>
