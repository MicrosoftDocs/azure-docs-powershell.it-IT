---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 0777c24aa5cb9b505ffc3495c9a9220da912f055
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676617"
---
# <span data-ttu-id="cdf29-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cdf29-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="cdf29-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdf29-102">SYNOPSIS</span></span>
<span data-ttu-id="cdf29-103">Scarica il contenuto di un file.</span><span class="sxs-lookup"><span data-stu-id="cdf29-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="cdf29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdf29-104">SYNTAX</span></span>

### <span data-ttu-id="cdf29-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cdf29-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdf29-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="cdf29-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdf29-107">Directory</span><span class="sxs-lookup"><span data-stu-id="cdf29-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdf29-108">File</span><span class="sxs-lookup"><span data-stu-id="cdf29-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cdf29-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdf29-109">DESCRIPTION</span></span>
<span data-ttu-id="cdf29-110">Il cmdlet **Get-AzStorageFileContent** Scarica il contenuto di un file e lo salva in una destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="cdf29-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="cdf29-111">Questo cmdlet non restituisce il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="cdf29-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="cdf29-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdf29-112">EXAMPLES</span></span>

### <span data-ttu-id="cdf29-113">Esempio 1: scaricare un file da una cartella</span><span class="sxs-lookup"><span data-stu-id="cdf29-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="cdf29-114">Questo comando consente di scaricare un file denominato CurrentDataFile nella cartella ContosoWorkingFolder della condivisione file ContosoShare06 nella cartella corrente.</span><span class="sxs-lookup"><span data-stu-id="cdf29-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="cdf29-115">Esempio 2: Scarica i file in condivisione file di esempio</span><span class="sxs-lookup"><span data-stu-id="cdf29-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="cdf29-116">In questo esempio vengono scaricati i file in condivisione file di esempio</span><span class="sxs-lookup"><span data-stu-id="cdf29-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="cdf29-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdf29-117">PARAMETERS</span></span>

### <span data-ttu-id="cdf29-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdf29-118">-AsJob</span></span>
<span data-ttu-id="cdf29-119">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="cdf29-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="cdf29-120">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="cdf29-120">-CheckMd5</span></span>
<span data-ttu-id="cdf29-121">Specifica se controllare la somma MD5 per il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="cdf29-121">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="cdf29-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cdf29-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cdf29-123">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="cdf29-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="cdf29-124">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="cdf29-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="cdf29-125">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="cdf29-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cdf29-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cdf29-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cdf29-127">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="cdf29-127">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="cdf29-128">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="cdf29-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="cdf29-129">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="cdf29-129">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="cdf29-130">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="cdf29-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="cdf29-131">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="cdf29-131">The default value is 10.</span></span>

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

### <span data-ttu-id="cdf29-132">-Contesto</span><span class="sxs-lookup"><span data-stu-id="cdf29-132">-Context</span></span>
<span data-ttu-id="cdf29-133">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cdf29-133">Specifies an Azure Storage context.</span></span> <span data-ttu-id="cdf29-134">Per ottenere un contesto, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="cdf29-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cdf29-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdf29-135">-DefaultProfile</span></span>
<span data-ttu-id="cdf29-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cdf29-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdf29-137">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="cdf29-137">-Destination</span></span>
<span data-ttu-id="cdf29-138">Specifica il percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cdf29-138">Specifies the destination path.</span></span>
<span data-ttu-id="cdf29-139">Questo cmdlet Scarica il contenuto del file nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cdf29-139">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="cdf29-140">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="cdf29-140">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="cdf29-141">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="cdf29-141">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="cdf29-142">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="cdf29-142">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="cdf29-143">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cdf29-143">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="cdf29-144">-Directory</span><span class="sxs-lookup"><span data-stu-id="cdf29-144">-Directory</span></span>
<span data-ttu-id="cdf29-145">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="cdf29-145">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="cdf29-146">Questo cmdlet consente di ottenere contenuto per un file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cdf29-146">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="cdf29-147">Per ottenere una directory, usare il cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="cdf29-147">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="cdf29-148">Puoi anche usare il cmdlet Get-AzStorageFile per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="cdf29-148">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="cdf29-149">-File</span><span class="sxs-lookup"><span data-stu-id="cdf29-149">-File</span></span>
<span data-ttu-id="cdf29-150">Specifica un file come oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="cdf29-150">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="cdf29-151">Questo cmdlet ottiene il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cdf29-151">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="cdf29-152">Per ottenere un oggetto **CloudFile** , usa il cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="cdf29-152">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="cdf29-153">-Force</span><span class="sxs-lookup"><span data-stu-id="cdf29-153">-Force</span></span>
<span data-ttu-id="cdf29-154">Se specifichi il percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="cdf29-154">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="cdf29-155">Se si specifica un percorso di un file già esistente e si specifica il parametro *Force* , il cmdlet sovrascriverà il file.</span><span class="sxs-lookup"><span data-stu-id="cdf29-155">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="cdf29-156">Se si specifica un percorso di un file esistente e non si specifica la *forza* , il cmdlet richiede prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="cdf29-156">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="cdf29-157">Se si specifica il percorso di una cartella, questo cmdlet tenterà di creare un file con il nome del file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cdf29-157">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="cdf29-158">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdf29-158">-PassThru</span></span>
<span data-ttu-id="cdf29-159">Indica che questo cmdlet restituisce l'oggetto **AzureStorageFile** che esegue il download.</span><span class="sxs-lookup"><span data-stu-id="cdf29-159">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="cdf29-160">-Path</span><span class="sxs-lookup"><span data-stu-id="cdf29-160">-Path</span></span>
<span data-ttu-id="cdf29-161">Specifica il percorso di un file.</span><span class="sxs-lookup"><span data-stu-id="cdf29-161">Specifies the path of a file.</span></span>
<span data-ttu-id="cdf29-162">Questo cmdlet consente di ottenere il contenuto del file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cdf29-162">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="cdf29-163">Se il file non esiste, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="cdf29-163">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cdf29-164">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cdf29-164">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cdf29-165">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="cdf29-165">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="cdf29-166">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="cdf29-166">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="cdf29-167">-Condividi</span><span class="sxs-lookup"><span data-stu-id="cdf29-167">-Share</span></span>
<span data-ttu-id="cdf29-168">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="cdf29-168">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="cdf29-169">Questo cmdlet Scarica il contenuto del file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="cdf29-169">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="cdf29-170">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="cdf29-170">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="cdf29-171">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cdf29-171">This object contains the storage context.</span></span>
<span data-ttu-id="cdf29-172">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="cdf29-172">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="cdf29-173">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cdf29-173">-ShareName</span></span>
<span data-ttu-id="cdf29-174">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="cdf29-174">Specifies the name of the file share.</span></span>
<span data-ttu-id="cdf29-175">Questo cmdlet Scarica il contenuto del file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="cdf29-175">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="cdf29-176">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cdf29-176">-Confirm</span></span>
<span data-ttu-id="cdf29-177">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdf29-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdf29-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdf29-178">-WhatIf</span></span>
<span data-ttu-id="cdf29-179">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdf29-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdf29-180">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdf29-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdf29-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdf29-181">CommonParameters</span></span>
<span data-ttu-id="cdf29-182">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdf29-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdf29-183">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdf29-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdf29-184">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdf29-184">INPUTS</span></span>

### <span data-ttu-id="cdf29-185">Microsoft. WindowsAzure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="cdf29-185">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="cdf29-186">Microsoft. WindowsAzure. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="cdf29-186">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="cdf29-187">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="cdf29-187">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="cdf29-188">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cdf29-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cdf29-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdf29-189">OUTPUTS</span></span>

### <span data-ttu-id="cdf29-190">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="cdf29-190">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="cdf29-191">Note</span><span class="sxs-lookup"><span data-stu-id="cdf29-191">NOTES</span></span>

## <span data-ttu-id="cdf29-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdf29-192">RELATED LINKS</span></span>

[<span data-ttu-id="cdf29-193">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cdf29-193">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="cdf29-194">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cdf29-194">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)

