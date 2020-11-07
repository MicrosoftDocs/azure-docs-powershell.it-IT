---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: aa1c7cebbcb6fe24b06638644d19b07c83c2ff04
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862234"
---
# <span data-ttu-id="f77da-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f77da-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="f77da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f77da-102">SYNOPSIS</span></span>
<span data-ttu-id="f77da-103">Scarica il contenuto di un file.</span><span class="sxs-lookup"><span data-stu-id="f77da-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="f77da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f77da-104">SYNTAX</span></span>

### <span data-ttu-id="f77da-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f77da-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f77da-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="f77da-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f77da-107">Directory</span><span class="sxs-lookup"><span data-stu-id="f77da-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f77da-108">File</span><span class="sxs-lookup"><span data-stu-id="f77da-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f77da-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f77da-109">DESCRIPTION</span></span>
<span data-ttu-id="f77da-110">Il cmdlet **Get-AzStorageFileContent** Scarica il contenuto di un file e lo salva in una destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="f77da-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="f77da-111">Questo cmdlet non restituisce il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="f77da-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="f77da-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f77da-112">EXAMPLES</span></span>

### <span data-ttu-id="f77da-113">Esempio 1: scaricare un file da una cartella</span><span class="sxs-lookup"><span data-stu-id="f77da-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="f77da-114">Questo comando consente di scaricare un file denominato CurrentDataFile nella cartella ContosoWorkingFolder della condivisione file ContosoShare06 nella cartella corrente.</span><span class="sxs-lookup"><span data-stu-id="f77da-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="f77da-115">Esempio 2: Scarica i file in condivisione file di esempio</span><span class="sxs-lookup"><span data-stu-id="f77da-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="f77da-116">In questo esempio vengono scaricati i file in condivisione file di esempio</span><span class="sxs-lookup"><span data-stu-id="f77da-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="f77da-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f77da-117">PARAMETERS</span></span>

### <span data-ttu-id="f77da-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="f77da-118">-CheckMd5</span></span>
<span data-ttu-id="f77da-119">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="f77da-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="f77da-120">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="f77da-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="f77da-121">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="f77da-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="f77da-122">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f77da-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="f77da-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f77da-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f77da-124">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="f77da-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="f77da-125">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="f77da-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="f77da-126">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="f77da-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="f77da-127">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f77da-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="f77da-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f77da-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f77da-129">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="f77da-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="f77da-130">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="f77da-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="f77da-131">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="f77da-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="f77da-132">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f77da-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="f77da-133">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f77da-133">-Context</span></span>
<span data-ttu-id="f77da-134">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="f77da-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="f77da-135">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="f77da-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="f77da-136">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="f77da-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="f77da-137">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f77da-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="f77da-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f77da-138">-DefaultProfile</span></span>
<span data-ttu-id="f77da-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f77da-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f77da-140">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="f77da-140">-Destination</span></span>
<span data-ttu-id="f77da-141">Specifica il percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f77da-141">Specifies the destination path.</span></span>
<span data-ttu-id="f77da-142">Questo cmdlet Scarica il contenuto del file nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f77da-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="f77da-143">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="f77da-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="f77da-144">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="f77da-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="f77da-145">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="f77da-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="f77da-146">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f77da-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="f77da-147">-Directory</span><span class="sxs-lookup"><span data-stu-id="f77da-147">-Directory</span></span>
<span data-ttu-id="f77da-148">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="f77da-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="f77da-149">Questo cmdlet consente di ottenere contenuto per un file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f77da-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="f77da-150">Per ottenere una directory, usare il cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="f77da-150">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="f77da-151">Puoi anche usare il cmdlet Get-AzStorageFile per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="f77da-151">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="f77da-152">-File</span><span class="sxs-lookup"><span data-stu-id="f77da-152">-File</span></span>
<span data-ttu-id="f77da-153">Specifica un file come oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="f77da-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="f77da-154">Questo cmdlet ottiene il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f77da-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="f77da-155">Per ottenere un oggetto **CloudFile** , usa il cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="f77da-155">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="f77da-156">-Force</span><span class="sxs-lookup"><span data-stu-id="f77da-156">-Force</span></span>
<span data-ttu-id="f77da-157">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="f77da-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="f77da-158">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="f77da-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="f77da-159">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="f77da-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="f77da-160">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f77da-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="f77da-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f77da-161">-PassThru</span></span>
<span data-ttu-id="f77da-162">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="f77da-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="f77da-163">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="f77da-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="f77da-164">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="f77da-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="f77da-165">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f77da-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="f77da-166">-Path</span><span class="sxs-lookup"><span data-stu-id="f77da-166">-Path</span></span>
<span data-ttu-id="f77da-167">Specifica il percorso di un file.</span><span class="sxs-lookup"><span data-stu-id="f77da-167">Specifies the path of a file.</span></span>
<span data-ttu-id="f77da-168">Questo cmdlet consente di ottenere il contenuto del file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f77da-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="f77da-169">Se il file non esiste, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="f77da-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f77da-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f77da-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f77da-171">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="f77da-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="f77da-172">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="f77da-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="f77da-173">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="f77da-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="f77da-174">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f77da-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="f77da-175">-Condividi</span><span class="sxs-lookup"><span data-stu-id="f77da-175">-Share</span></span>
<span data-ttu-id="f77da-176">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="f77da-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="f77da-177">Questo cmdlet Scarica il contenuto del file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="f77da-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="f77da-178">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="f77da-178">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="f77da-179">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f77da-179">This object contains the storage context.</span></span>
<span data-ttu-id="f77da-180">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="f77da-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="f77da-181">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f77da-181">-ShareName</span></span>
<span data-ttu-id="f77da-182">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="f77da-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="f77da-183">Questo cmdlet Scarica il contenuto del file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="f77da-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="f77da-184">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f77da-184">-Confirm</span></span>
<span data-ttu-id="f77da-185">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f77da-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f77da-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f77da-186">-WhatIf</span></span>
<span data-ttu-id="f77da-187">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f77da-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f77da-188">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f77da-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f77da-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f77da-189">CommonParameters</span></span>
<span data-ttu-id="f77da-190">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f77da-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f77da-191">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f77da-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f77da-192">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f77da-192">INPUTS</span></span>

### <span data-ttu-id="f77da-193">Microsoft. WindowsAz. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="f77da-193">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="f77da-194">Parametri: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f77da-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="f77da-195">Microsoft. WindowsAz. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="f77da-195">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="f77da-196">Parameters: directory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f77da-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="f77da-197">Microsoft. WindowsAz. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="f77da-197">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="f77da-198">Parameters: file (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f77da-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="f77da-199">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f77da-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f77da-200">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f77da-200">OUTPUTS</span></span>

### <span data-ttu-id="f77da-201">Microsoft. WindowsAz. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="f77da-201">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="f77da-202">Note</span><span class="sxs-lookup"><span data-stu-id="f77da-202">NOTES</span></span>

## <span data-ttu-id="f77da-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f77da-203">RELATED LINKS</span></span>

[<span data-ttu-id="f77da-204">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="f77da-204">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="f77da-205">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f77da-205">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


