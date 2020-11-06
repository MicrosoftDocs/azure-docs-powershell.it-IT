---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: a04a035e0fedfa4bca00eceda1dcf8dba0680c0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519663"
---
# <span data-ttu-id="c550d-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c550d-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="c550d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c550d-102">SYNOPSIS</span></span>
<span data-ttu-id="c550d-103">Scarica il contenuto di un file.</span><span class="sxs-lookup"><span data-stu-id="c550d-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c550d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c550d-104">SYNTAX</span></span>

### <span data-ttu-id="c550d-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c550d-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c550d-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="c550d-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c550d-107">Directory</span><span class="sxs-lookup"><span data-stu-id="c550d-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c550d-108">File</span><span class="sxs-lookup"><span data-stu-id="c550d-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c550d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c550d-109">DESCRIPTION</span></span>
<span data-ttu-id="c550d-110">Il cmdlet **Get-AzureStorageFileContent** Scarica il contenuto di un file e lo salva in una destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="c550d-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="c550d-111">Questo cmdlet non restituisce il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="c550d-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="c550d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c550d-112">EXAMPLES</span></span>

### <span data-ttu-id="c550d-113">Esempio 1: scaricare un file da una cartella</span><span class="sxs-lookup"><span data-stu-id="c550d-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="c550d-114">Questo comando consente di scaricare un file denominato CurrentDataFile nella cartella ContosoWorkingFolder della condivisione file ContosoShare06 nella cartella corrente.</span><span class="sxs-lookup"><span data-stu-id="c550d-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="c550d-115">Esempio 2: Scarica i file in condivisione file di esempio</span><span class="sxs-lookup"><span data-stu-id="c550d-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="c550d-116">In questo esempio vengono scaricati i file in condivisione file di esempio</span><span class="sxs-lookup"><span data-stu-id="c550d-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="c550d-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c550d-117">PARAMETERS</span></span>

### <span data-ttu-id="c550d-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="c550d-118">-CheckMd5</span></span>
<span data-ttu-id="c550d-119">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="c550d-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c550d-120">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="c550d-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c550d-121">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="c550d-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="c550d-122">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c550d-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c550d-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c550d-124">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="c550d-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c550d-125">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="c550d-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c550d-126">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="c550d-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="c550d-127">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c550d-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c550d-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c550d-129">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="c550d-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c550d-130">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="c550d-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c550d-131">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="c550d-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="c550d-132">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c550d-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-133">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c550d-133">-Context</span></span>
<span data-ttu-id="c550d-134">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="c550d-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c550d-135">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="c550d-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c550d-136">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="c550d-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="c550d-137">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c550d-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-138">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="c550d-138">-Destination</span></span>
<span data-ttu-id="c550d-139">Specifica il percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c550d-139">Specifies the destination path.</span></span>
<span data-ttu-id="c550d-140">Questo cmdlet Scarica il contenuto del file nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c550d-140">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="c550d-141">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="c550d-141">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c550d-142">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="c550d-142">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c550d-143">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="c550d-143">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="c550d-144">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c550d-144">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-145">-Directory</span><span class="sxs-lookup"><span data-stu-id="c550d-145">-Directory</span></span>
<span data-ttu-id="c550d-146">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="c550d-146">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="c550d-147">Questo cmdlet consente di ottenere contenuto per un file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c550d-147">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="c550d-148">Per ottenere una directory, usare il cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="c550d-148">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="c550d-149">Puoi anche usare il cmdlet Get-AzureStorageFile per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="c550d-149">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-150">-File</span><span class="sxs-lookup"><span data-stu-id="c550d-150">-File</span></span>
<span data-ttu-id="c550d-151">Specifica un file come oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="c550d-151">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="c550d-152">Questo cmdlet ottiene il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c550d-152">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="c550d-153">Per ottenere un oggetto **CloudFile** , usa il cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="c550d-153">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-154">-Force</span><span class="sxs-lookup"><span data-stu-id="c550d-154">-Force</span></span>
<span data-ttu-id="c550d-155">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="c550d-155">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c550d-156">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="c550d-156">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c550d-157">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="c550d-157">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="c550d-158">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c550d-158">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-159">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c550d-159">-PassThru</span></span>
<span data-ttu-id="c550d-160">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="c550d-160">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c550d-161">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="c550d-161">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c550d-162">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="c550d-162">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="c550d-163">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c550d-163">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-164">-Path</span><span class="sxs-lookup"><span data-stu-id="c550d-164">-Path</span></span>
<span data-ttu-id="c550d-165">Specifica il percorso di un file.</span><span class="sxs-lookup"><span data-stu-id="c550d-165">Specifies the path of a file.</span></span>
<span data-ttu-id="c550d-166">Questo cmdlet consente di ottenere il contenuto del file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c550d-166">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="c550d-167">Se il file non esiste, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="c550d-167">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-168">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c550d-168">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c550d-169">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="c550d-169">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c550d-170">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="c550d-170">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c550d-171">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="c550d-171">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="c550d-172">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c550d-172">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-173">-Condividi</span><span class="sxs-lookup"><span data-stu-id="c550d-173">-Share</span></span>
<span data-ttu-id="c550d-174">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="c550d-174">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="c550d-175">Questo cmdlet Scarica il contenuto del file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="c550d-175">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="c550d-176">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="c550d-176">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="c550d-177">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c550d-177">This object contains the storage context.</span></span>
<span data-ttu-id="c550d-178">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="c550d-178">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-179">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c550d-179">-ShareName</span></span>
<span data-ttu-id="c550d-180">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="c550d-180">Specifies the name of the file share.</span></span>
<span data-ttu-id="c550d-181">Questo cmdlet Scarica il contenuto del file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="c550d-181">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-182">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c550d-182">-Confirm</span></span>
<span data-ttu-id="c550d-183">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c550d-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c550d-184">-WhatIf</span></span>
<span data-ttu-id="c550d-185">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c550d-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c550d-186">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c550d-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c550d-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c550d-187">CommonParameters</span></span>
<span data-ttu-id="c550d-188">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c550d-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c550d-189">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c550d-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c550d-190">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c550d-190">INPUTS</span></span>

### <span data-ttu-id="c550d-191">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c550d-191">IStorageContext</span></span>

<span data-ttu-id="c550d-192">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c550d-192">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c550d-193">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="c550d-193">CloudFileDirectory</span></span>

<span data-ttu-id="c550d-194">Il parametro ' directory ' accetta il valore di tipo ' CloudFileDirectory ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c550d-194">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="c550d-195">CloudFile</span><span class="sxs-lookup"><span data-stu-id="c550d-195">CloudFile</span></span>

<span data-ttu-id="c550d-196">Il parametro "file" accetta il valore di tipo "CloudFile" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c550d-196">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="c550d-197">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="c550d-197">CloudFileShare</span></span>

<span data-ttu-id="c550d-198">Il parametro "Share" accetta il valore di tipo "CloudFileShare" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c550d-198">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="c550d-199">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c550d-199">OUTPUTS</span></span>

## <span data-ttu-id="c550d-200">Note</span><span class="sxs-lookup"><span data-stu-id="c550d-200">NOTES</span></span>

## <span data-ttu-id="c550d-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c550d-201">RELATED LINKS</span></span>

[<span data-ttu-id="c550d-202">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="c550d-202">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="c550d-203">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c550d-203">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


