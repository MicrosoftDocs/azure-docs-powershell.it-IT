---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376137"
---
# <span data-ttu-id="4c0b5-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4c0b5-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="4c0b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0b5-103">Carica il contenuto di un file.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="4c0b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c0b5-104">SYNTAX</span></span>

### <span data-ttu-id="4c0b5-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c0b5-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="4c0b5-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="4c0b5-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="4c0b5-107">Directory</span><span class="sxs-lookup"><span data-stu-id="4c0b5-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="4c0b5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c0b5-108">DESCRIPTION</span></span>
<span data-ttu-id="4c0b5-109">Il cmdlet **set-AzStorageFileContent** carica il contenuto di un file in un file in una condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="4c0b5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c0b5-110">EXAMPLES</span></span>

### <span data-ttu-id="4c0b5-111">Esempio 1: caricare un file nella cartella corrente</span><span class="sxs-lookup"><span data-stu-id="4c0b5-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="4c0b5-112">Questo comando carica un file denominato DataFile37 nella cartella corrente come un file denominato CurrentDataFile nella cartella denominata ContosoWorkingFolder.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="4c0b5-113">Esempio 2: caricare tutti i file nella cartella corrente</span><span class="sxs-lookup"><span data-stu-id="4c0b5-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="4c0b5-114">Questo esempio usa diversi cmdlet di Windows PowerShell comuni e il cmdlet corrente per caricare tutti i file dalla cartella corrente nella cartella radice di container ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="4c0b5-115">Il primo comando ottiene il nome della cartella corrente e lo archivia nella variabile $CurrentFolder.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="4c0b5-116">Il secondo comando usa il cmdlet **Get-AzStorageShare** per ottenere la condivisione di file denominata ContosoShare06 e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="4c0b5-117">Il comando finale Recupera il contenuto della cartella corrente e passa ognuno al cmdlet Where-Object usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4c0b5-118">Questo cmdlet filtra gli oggetti che non sono file e quindi passa i file al cmdlet ForEach-Object.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="4c0b5-119">Questo cmdlet esegue un blocco di script per ogni file che crea il percorso appropriato e quindi usa il cmdlet Current per caricare il file.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="4c0b5-120">Il risultato ha lo stesso nome e la stessa posizione relativa rispetto agli altri file caricati in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="4c0b5-121">Per altre informazioni sui blocchi di script, digitare `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="4c0b5-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="4c0b5-122">Esempio 3: caricare un file locale in un file di Azure e Perserve le proprietà SMB del file locale (file Attributtes, ora di creazione del file, ultima ora di scrittura) nel file Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="4c0b5-123">Questo esempio carica un file locale in un file di Azure e perserves le proprietà SMB del file locale (file Attributtes, ora di creazione del file, ultima ora di scrittura) nel file Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="4c0b5-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c0b5-124">PARAMETERS</span></span>

### <span data-ttu-id="4c0b5-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c0b5-125">-AsJob</span></span>
<span data-ttu-id="4c0b5-126">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="4c0b5-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4c0b5-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4c0b5-128">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4c0b5-129">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4c0b5-130">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4c0b5-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4c0b5-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4c0b5-132">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4c0b5-133">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4c0b5-134">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4c0b5-135">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4c0b5-136">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-136">The default value is 10.</span></span>

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

### <span data-ttu-id="4c0b5-137">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4c0b5-137">-Context</span></span>
<span data-ttu-id="4c0b5-138">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4c0b5-139">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="4c0b5-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4c0b5-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0b5-140">-DefaultProfile</span></span>
<span data-ttu-id="4c0b5-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c0b5-142">-Directory</span><span class="sxs-lookup"><span data-stu-id="4c0b5-142">-Directory</span></span>
<span data-ttu-id="4c0b5-143">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="4c0b5-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="4c0b5-144">Questo cmdlet carica il file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="4c0b5-145">Per ottenere una directory, usare il cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="4c0b5-146">Puoi anche usare il cmdlet Get-AzStorageFile per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0b5-147">-Force</span><span class="sxs-lookup"><span data-stu-id="4c0b5-147">-Force</span></span>
<span data-ttu-id="4c0b5-148">Indica che questo cmdlet sovrascrive un file di archiviazione di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="4c0b5-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c0b5-149">-PassThru</span></span>
<span data-ttu-id="4c0b5-150">Indica che questo cmdlet restituisce l'oggetto **AzureStorageFile** che crea o carica.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="4c0b5-151">-Path</span><span class="sxs-lookup"><span data-stu-id="4c0b5-151">-Path</span></span>
<span data-ttu-id="4c0b5-152">Specifica il percorso di un file o di una cartella.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="4c0b5-153">Questo cmdlet carica il contenuto nel file specificato da questo parametro o in un file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="4c0b5-154">Se specifichi una cartella, questo cmdlet crea un file con lo stesso nome del file di origine.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="4c0b5-155">Se specifichi un percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto in tale file.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="4c0b5-156">Se si specifica un file già esistente e si specifica il parametro _Force_ , questo cmdlet sovrascrive il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="4c0b5-157">Se si specifica un file già esistente e non si specifica _Force_, questo cmdlet non apporta alcuna modifica e restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-157">If you specify a file that already exists and you do not specify _Force_, this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="4c0b5-158">Se si specifica un percorso di una cartella che non esiste, questo cmdlet non apporta alcuna modifica e restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="4c0b5-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="4c0b5-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="4c0b5-160">Mantieni le proprietà SMB del file di origine (file Attributtes, ora di creazione del file, ultima ora di scrittura) nel file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="4c0b5-161">Questo parametro è disponibile solo in Windows.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="4c0b5-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4c0b5-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4c0b5-163">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4c0b5-164">-Condividi</span><span class="sxs-lookup"><span data-stu-id="4c0b5-164">-Share</span></span>
<span data-ttu-id="4c0b5-165">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="4c0b5-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="4c0b5-166">Questo cmdlet viene caricato in un file nella condivisione file specificata dal parametro.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="4c0b5-167">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="4c0b5-168">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-168">This object contains the storage context.</span></span>
<span data-ttu-id="4c0b5-169">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="4c0b5-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0b5-170">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4c0b5-170">-ShareName</span></span>
<span data-ttu-id="4c0b5-171">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="4c0b5-172">Questo cmdlet viene caricato in un file nella condivisione file specificata dal parametro.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="4c0b5-173">-Origine</span><span class="sxs-lookup"><span data-stu-id="4c0b5-173">-Source</span></span>
<span data-ttu-id="4c0b5-174">Specifica il file di origine caricato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="4c0b5-175">Se specifichi un file che non esiste, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0b5-176">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c0b5-176">-Confirm</span></span>
<span data-ttu-id="4c0b5-177">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c0b5-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c0b5-178">-WhatIf</span></span>
<span data-ttu-id="4c0b5-179">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c0b5-180">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c0b5-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0b5-181">CommonParameters</span></span>
<span data-ttu-id="4c0b5-182">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c0b5-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0b5-183">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c0b5-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0b5-184">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c0b5-184">INPUTS</span></span>

### <span data-ttu-id="4c0b5-185">Microsoft. Azure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4c0b5-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="4c0b5-186">Microsoft. Azure. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="4c0b5-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="4c0b5-187">System. String</span><span class="sxs-lookup"><span data-stu-id="4c0b5-187">System.String</span></span>

### <span data-ttu-id="4c0b5-188">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4c0b5-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4c0b5-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c0b5-189">OUTPUTS</span></span>

### <span data-ttu-id="4c0b5-190">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="4c0b5-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="4c0b5-191">Note</span><span class="sxs-lookup"><span data-stu-id="4c0b5-191">NOTES</span></span>

## <span data-ttu-id="4c0b5-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c0b5-192">RELATED LINKS</span></span>

[<span data-ttu-id="4c0b5-193">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4c0b5-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="4c0b5-194">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4c0b5-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="4c0b5-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4c0b5-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
