---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 0641fdf635bce2bbb545e50ecc99a39329fabc9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514020"
---
# <span data-ttu-id="3475a-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3475a-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="3475a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3475a-102">SYNOPSIS</span></span>
<span data-ttu-id="3475a-103">Scarica il contenuto di un file.</span><span class="sxs-lookup"><span data-stu-id="3475a-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3475a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3475a-104">SYNTAX</span></span>

### <span data-ttu-id="3475a-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3475a-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3475a-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="3475a-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3475a-107">Directory</span><span class="sxs-lookup"><span data-stu-id="3475a-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3475a-108">File</span><span class="sxs-lookup"><span data-stu-id="3475a-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3475a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3475a-109">DESCRIPTION</span></span>
<span data-ttu-id="3475a-110">Il cmdlet **Get-AzureStorageFileContent** Scarica il contenuto di un file e lo salva in una destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="3475a-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="3475a-111">Questo cmdlet non restituisce il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="3475a-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="3475a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3475a-112">EXAMPLES</span></span>

### <span data-ttu-id="3475a-113">Esempio 1: scaricare un file da una cartella</span><span class="sxs-lookup"><span data-stu-id="3475a-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="3475a-114">Questo comando consente di scaricare un file denominato CurrentDataFile nella cartella ContosoWorkingFolder della condivisione file ContosoShare06 nella cartella corrente.</span><span class="sxs-lookup"><span data-stu-id="3475a-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="3475a-115">Esempio 2: Scarica i file in condivisione file di esempio</span><span class="sxs-lookup"><span data-stu-id="3475a-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="3475a-116">In questo esempio vengono scaricati i file in condivisione file di esempio</span><span class="sxs-lookup"><span data-stu-id="3475a-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="3475a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3475a-117">PARAMETERS</span></span>

### <span data-ttu-id="3475a-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="3475a-118">-CheckMd5</span></span>
<span data-ttu-id="3475a-119">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="3475a-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3475a-120">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="3475a-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3475a-121">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="3475a-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="3475a-122">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3475a-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="3475a-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3475a-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3475a-124">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="3475a-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3475a-125">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="3475a-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3475a-126">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="3475a-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="3475a-127">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3475a-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="3475a-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3475a-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3475a-129">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="3475a-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3475a-130">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="3475a-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3475a-131">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="3475a-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="3475a-132">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3475a-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="3475a-133">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3475a-133">-Context</span></span>
<span data-ttu-id="3475a-134">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="3475a-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3475a-135">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="3475a-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3475a-136">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="3475a-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="3475a-137">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3475a-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3475a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3475a-138">-DefaultProfile</span></span>
<span data-ttu-id="3475a-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3475a-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3475a-140">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="3475a-140">-Destination</span></span>
<span data-ttu-id="3475a-141">Specifica il percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3475a-141">Specifies the destination path.</span></span>
<span data-ttu-id="3475a-142">Questo cmdlet Scarica il contenuto del file nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3475a-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="3475a-143">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="3475a-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3475a-144">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="3475a-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3475a-145">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="3475a-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="3475a-146">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3475a-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3475a-147">-Directory</span><span class="sxs-lookup"><span data-stu-id="3475a-147">-Directory</span></span>
<span data-ttu-id="3475a-148">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="3475a-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="3475a-149">Questo cmdlet consente di ottenere contenuto per un file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3475a-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="3475a-150">Per ottenere una directory, usare il cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="3475a-150">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="3475a-151">Puoi anche usare il cmdlet Get-AzureStorageFile per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="3475a-151">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3475a-152">-File</span><span class="sxs-lookup"><span data-stu-id="3475a-152">-File</span></span>
<span data-ttu-id="3475a-153">Specifica un file come oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="3475a-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="3475a-154">Questo cmdlet ottiene il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3475a-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="3475a-155">Per ottenere un oggetto **CloudFile** , usa il cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="3475a-155">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3475a-156">-Force</span><span class="sxs-lookup"><span data-stu-id="3475a-156">-Force</span></span>
<span data-ttu-id="3475a-157">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="3475a-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3475a-158">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="3475a-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3475a-159">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="3475a-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="3475a-160">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3475a-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="3475a-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3475a-161">-PassThru</span></span>
<span data-ttu-id="3475a-162">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="3475a-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3475a-163">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="3475a-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3475a-164">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="3475a-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="3475a-165">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3475a-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="3475a-166">-Path</span><span class="sxs-lookup"><span data-stu-id="3475a-166">-Path</span></span>
<span data-ttu-id="3475a-167">Specifica il percorso di un file.</span><span class="sxs-lookup"><span data-stu-id="3475a-167">Specifies the path of a file.</span></span>
<span data-ttu-id="3475a-168">Questo cmdlet consente di ottenere il contenuto del file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3475a-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="3475a-169">Se il file non esiste, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="3475a-169">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3475a-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3475a-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3475a-171">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="3475a-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3475a-172">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="3475a-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3475a-173">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="3475a-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="3475a-174">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3475a-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="3475a-175">-Condividi</span><span class="sxs-lookup"><span data-stu-id="3475a-175">-Share</span></span>
<span data-ttu-id="3475a-176">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="3475a-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="3475a-177">Questo cmdlet Scarica il contenuto del file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="3475a-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="3475a-178">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="3475a-178">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="3475a-179">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3475a-179">This object contains the storage context.</span></span>
<span data-ttu-id="3475a-180">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="3475a-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3475a-181">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3475a-181">-ShareName</span></span>
<span data-ttu-id="3475a-182">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3475a-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="3475a-183">Questo cmdlet Scarica il contenuto del file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="3475a-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3475a-184">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3475a-184">-Confirm</span></span>
<span data-ttu-id="3475a-185">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3475a-185">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3475a-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3475a-186">-WhatIf</span></span>
<span data-ttu-id="3475a-187">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3475a-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3475a-188">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3475a-188">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3475a-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3475a-189">CommonParameters</span></span>
<span data-ttu-id="3475a-190">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3475a-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3475a-191">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3475a-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3475a-192">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3475a-192">INPUTS</span></span>

### <span data-ttu-id="3475a-193">Microsoft. WindowsAzure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3475a-193">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="3475a-194">Parametri: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3475a-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="3475a-195">Microsoft. WindowsAzure. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3475a-195">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="3475a-196">Parameters: directory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3475a-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="3475a-197">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="3475a-197">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="3475a-198">Parameters: file (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3475a-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="3475a-199">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3475a-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3475a-200">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3475a-200">OUTPUTS</span></span>

### <span data-ttu-id="3475a-201">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="3475a-201">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="3475a-202">Note</span><span class="sxs-lookup"><span data-stu-id="3475a-202">NOTES</span></span>

## <span data-ttu-id="3475a-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3475a-203">RELATED LINKS</span></span>

[<span data-ttu-id="3475a-204">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="3475a-204">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="3475a-205">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3475a-205">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)

