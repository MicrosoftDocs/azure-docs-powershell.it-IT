---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 0ac029d4fbe0ab632671f024ff90ebeca9717d50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188886"
---
# <span data-ttu-id="78600-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="78600-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="78600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78600-102">SYNOPSIS</span></span>
<span data-ttu-id="78600-103">Chiude gli handle di file di una condivisione file, di una directory o di un file.</span><span class="sxs-lookup"><span data-stu-id="78600-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="78600-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78600-104">SYNTAX</span></span>

### <span data-ttu-id="78600-105">ShareNameCloseAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78600-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78600-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="78600-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78600-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="78600-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78600-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="78600-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78600-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="78600-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78600-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="78600-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78600-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="78600-111">DESCRIPTION</span></span>
<span data-ttu-id="78600-112">Il cmdlet **Close-AzStorageFileHandle** chiude gli handle di file di una condivisione file, di una directory o di un file.</span><span class="sxs-lookup"><span data-stu-id="78600-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="78600-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78600-113">EXAMPLES</span></span>

### <span data-ttu-id="78600-114">Esempio 1: elenca tutte le condivisioni file dell'account di archiviazione corrente e chiude tutti gli handle di file delle condivisioni file in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="78600-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="78600-115">Questo comando elenca tutte le condivisioni file dell'account di archiviazione corrente e chiude tutti gli handle di file delle condivisioni file in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="78600-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="78600-116">Esempio 2: Chiudere tutti gli handle di file in una directory di file in modo ricorsivo e visualizzare il numero di handle di file chiusi</span><span class="sxs-lookup"><span data-stu-id="78600-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="78600-117">Questo comando chiude tutti i punti di controllo file in una directory di file e mostra il numero di handle di file chiusi.</span><span class="sxs-lookup"><span data-stu-id="78600-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="78600-118">Esempio 3: Chiudere tutti gli handle di file aperti 1 giorno prima in una directory di file</span><span class="sxs-lookup"><span data-stu-id="78600-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="78600-119">Questo comando elenca tutti gli handle di file in una directory di file in modo ricorsivo, filtra i quadratini di ridimensionamento aperti un giorno fa e quindi li chiude.</span><span class="sxs-lookup"><span data-stu-id="78600-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="78600-120">Esempio 4: Chiudere tutti gli handle di file su un file</span><span class="sxs-lookup"><span data-stu-id="78600-120">Example 4: Close all file handles on a file</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="78600-121">Questo comando chiude tutti i quadratini di ridimensionamento per un file.</span><span class="sxs-lookup"><span data-stu-id="78600-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="78600-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78600-122">PARAMETERS</span></span>

### <span data-ttu-id="78600-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78600-123">-AsJob</span></span>
<span data-ttu-id="78600-124">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="78600-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78600-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="78600-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="78600-126">Il tempo massimo di esecuzione sul lato client per ogni richiesta in secondi.</span><span class="sxs-lookup"><span data-stu-id="78600-126">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78600-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="78600-127">-CloseAll</span></span>
<span data-ttu-id="78600-128">Forzare la chiusura di tutti i punti di controllo del file.</span><span class="sxs-lookup"><span data-stu-id="78600-128">Force close all File handles.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll, FileCloseAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78600-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="78600-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="78600-130">La quantità totale di attività sincronizzate simultanee.</span><span class="sxs-lookup"><span data-stu-id="78600-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="78600-131">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="78600-131">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78600-132">-Context</span><span class="sxs-lookup"><span data-stu-id="78600-132">-Context</span></span>
<span data-ttu-id="78600-133">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="78600-133">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78600-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78600-134">-DefaultProfile</span></span>
<span data-ttu-id="78600-135">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78600-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78600-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="78600-136">-Directory</span></span>
<span data-ttu-id="78600-137">L'oggetto CloudFileDirectory indica la cartella di base in cui verranno elencati i file/directory.</span><span class="sxs-lookup"><span data-stu-id="78600-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78600-138">-File</span><span class="sxs-lookup"><span data-stu-id="78600-138">-File</span></span>
<span data-ttu-id="78600-139">L'oggetto CloudFile ha indicato il punto di controllo di chiusura del file.</span><span class="sxs-lookup"><span data-stu-id="78600-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78600-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="78600-140">-FileHandle</span></span>
<span data-ttu-id="78600-141">L'handle di file da chiudere.</span><span class="sxs-lookup"><span data-stu-id="78600-141">The File Handle to close.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSFileHandle
Parameter Sets: ShareNameCloseSingle, ShareCloseSingle
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78600-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78600-142">-PassThru</span></span>
<span data-ttu-id="78600-143">Restituire il conteggio dei punti di controllo file chiusi.</span><span class="sxs-lookup"><span data-stu-id="78600-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="78600-144">-Path</span><span class="sxs-lookup"><span data-stu-id="78600-144">-Path</span></span>
<span data-ttu-id="78600-145">Percorso di un file/directory esistente.</span><span class="sxs-lookup"><span data-stu-id="78600-145">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78600-146">-Ricorsivo</span><span class="sxs-lookup"><span data-stu-id="78600-146">-Recursive</span></span>
<span data-ttu-id="78600-147">I punti di controllo dell'elenco vengono visualizzati in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="78600-147">List handles Recursively.</span></span>
<span data-ttu-id="78600-148">Funziona solo in Directory file.</span><span class="sxs-lookup"><span data-stu-id="78600-148">Only works on File Directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78600-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="78600-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="78600-150">Timeout del server in ogni richiesta in secondi.</span><span class="sxs-lookup"><span data-stu-id="78600-150">The server time out for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78600-151">-Condividi</span><span class="sxs-lookup"><span data-stu-id="78600-151">-Share</span></span>
<span data-ttu-id="78600-152">L'oggetto CloudFileShare indica la condivisione in cui verranno elencati i file/directory.</span><span class="sxs-lookup"><span data-stu-id="78600-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78600-153">-ShareName</span><span class="sxs-lookup"><span data-stu-id="78600-153">-ShareName</span></span>
<span data-ttu-id="78600-154">Nome della condivisione file in cui verranno elencati i file/directory.</span><span class="sxs-lookup"><span data-stu-id="78600-154">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78600-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78600-155">-Confirm</span></span>
<span data-ttu-id="78600-156">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78600-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78600-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78600-157">-WhatIf</span></span>
<span data-ttu-id="78600-158">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78600-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78600-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78600-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78600-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78600-160">CommonParameters</span></span>
<span data-ttu-id="78600-161">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78600-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78600-162">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78600-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78600-163">INPUT</span><span class="sxs-lookup"><span data-stu-id="78600-163">INPUTS</span></span>

### <span data-ttu-id="78600-164">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="78600-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="78600-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="78600-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="78600-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="78600-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="78600-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78600-167">OUTPUTS</span></span>

### <span data-ttu-id="78600-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="78600-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="78600-169">NOTE</span><span class="sxs-lookup"><span data-stu-id="78600-169">NOTES</span></span>

## <span data-ttu-id="78600-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78600-170">RELATED LINKS</span></span>
