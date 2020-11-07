---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: fa80c434523b51e76884b0735eb178504d8a1a4d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676498"
---
# <span data-ttu-id="9e142-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9e142-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="9e142-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e142-102">SYNOPSIS</span></span>
<span data-ttu-id="9e142-103">Carica il contenuto di un file.</span><span class="sxs-lookup"><span data-stu-id="9e142-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="9e142-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e142-104">SYNTAX</span></span>

### <span data-ttu-id="9e142-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e142-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e142-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="9e142-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e142-107">Directory</span><span class="sxs-lookup"><span data-stu-id="9e142-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e142-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e142-108">DESCRIPTION</span></span>
<span data-ttu-id="9e142-109">Il cmdlet **set-AzStorageFileContent** carica il contenuto di un file in un file in una condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="9e142-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="9e142-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e142-110">EXAMPLES</span></span>

### <span data-ttu-id="9e142-111">Esempio 1: caricare un file nella cartella corrente</span><span class="sxs-lookup"><span data-stu-id="9e142-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="9e142-112">Questo comando carica un file denominato DataFile37 nella cartella corrente come un file denominato CurrentDataFile nella cartella denominata ContosoWorkingFolder.</span><span class="sxs-lookup"><span data-stu-id="9e142-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="9e142-113">Esempio 2: caricare tutti i file nella cartella corrente</span><span class="sxs-lookup"><span data-stu-id="9e142-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="9e142-114">Questo esempio usa diversi cmdlet di Windows PowerShell comuni e il cmdlet corrente per caricare tutti i file dalla cartella corrente nella cartella radice di container ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="9e142-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="9e142-115">Il primo comando ottiene il nome della cartella corrente e lo archivia nella variabile $CurrentFolder.</span><span class="sxs-lookup"><span data-stu-id="9e142-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="9e142-116">Il secondo comando usa il cmdlet **Get-AzStorageShare** per ottenere la condivisione di file denominata ContosoShare06 e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="9e142-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="9e142-117">Il comando finale Recupera il contenuto della cartella corrente e passa ognuno al cmdlet Where-Object usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e142-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9e142-118">Questo cmdlet filtra gli oggetti che non sono file e quindi passa i file al cmdlet ForEach-Object.</span><span class="sxs-lookup"><span data-stu-id="9e142-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="9e142-119">Questo cmdlet esegue un blocco di script per ogni file che crea il percorso appropriato e quindi usa il cmdlet Current per caricare il file.</span><span class="sxs-lookup"><span data-stu-id="9e142-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="9e142-120">Il risultato ha lo stesso nome e la stessa posizione relativa rispetto agli altri file caricati in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="9e142-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="9e142-121">Per altre informazioni sui blocchi di script, digitare `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="9e142-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="9e142-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e142-122">PARAMETERS</span></span>

### <span data-ttu-id="9e142-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e142-123">-AsJob</span></span>
<span data-ttu-id="9e142-124">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="9e142-124">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9e142-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9e142-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9e142-126">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="9e142-126">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9e142-127">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="9e142-127">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9e142-128">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9e142-128">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9e142-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9e142-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9e142-130">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="9e142-130">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9e142-131">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="9e142-131">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9e142-132">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="9e142-132">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9e142-133">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="9e142-133">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9e142-134">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="9e142-134">The default value is 10.</span></span>

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

### <span data-ttu-id="9e142-135">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9e142-135">-Context</span></span>
<span data-ttu-id="9e142-136">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e142-136">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9e142-137">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="9e142-137">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9e142-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e142-138">-DefaultProfile</span></span>
<span data-ttu-id="9e142-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e142-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e142-140">-Directory</span><span class="sxs-lookup"><span data-stu-id="9e142-140">-Directory</span></span>
<span data-ttu-id="9e142-141">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="9e142-141">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="9e142-142">Questo cmdlet carica il file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9e142-142">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="9e142-143">Per ottenere una directory, usare il cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="9e142-143">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="9e142-144">Puoi anche usare il cmdlet Get-AzStorageFile per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="9e142-144">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="9e142-145">-Force</span><span class="sxs-lookup"><span data-stu-id="9e142-145">-Force</span></span>
<span data-ttu-id="9e142-146">Indica che questo cmdlet sovrascrive un file di archiviazione di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="9e142-146">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="9e142-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e142-147">-PassThru</span></span>
<span data-ttu-id="9e142-148">Indica che questo cmdlet restituisce l'oggetto **AzureStorageFile** che crea o carica.</span><span class="sxs-lookup"><span data-stu-id="9e142-148">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="9e142-149">-Path</span><span class="sxs-lookup"><span data-stu-id="9e142-149">-Path</span></span>
<span data-ttu-id="9e142-150">Specifica il percorso di un file o di una cartella.</span><span class="sxs-lookup"><span data-stu-id="9e142-150">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="9e142-151">Questo cmdlet carica il contenuto nel file specificato da questo parametro o in un file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9e142-151">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="9e142-152">Se specifichi una cartella, questo cmdlet crea un file con lo stesso nome del file di origine.</span><span class="sxs-lookup"><span data-stu-id="9e142-152">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="9e142-153">Se specifichi un percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto in tale file.</span><span class="sxs-lookup"><span data-stu-id="9e142-153">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="9e142-154">Se si specifica un file già esistente e si specifica il parametro _Force_ , questo cmdlet sovrascrive il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="9e142-154">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="9e142-155">Se si specifica un file già esistente e non si specifica _Force_ , questo cmdlet non apporta alcuna modifica e restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9e142-155">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="9e142-156">Se si specifica un percorso di una cartella che non esiste, questo cmdlet non apporta alcuna modifica e restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9e142-156">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="9e142-157">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9e142-157">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9e142-158">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="9e142-158">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9e142-159">-Condividi</span><span class="sxs-lookup"><span data-stu-id="9e142-159">-Share</span></span>
<span data-ttu-id="9e142-160">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="9e142-160">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="9e142-161">Questo cmdlet viene caricato in un file nella condivisione file specificata dal parametro.</span><span class="sxs-lookup"><span data-stu-id="9e142-161">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="9e142-162">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="9e142-162">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="9e142-163">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9e142-163">This object contains the storage context.</span></span>
<span data-ttu-id="9e142-164">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="9e142-164">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="9e142-165">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9e142-165">-ShareName</span></span>
<span data-ttu-id="9e142-166">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="9e142-166">Specifies the name of the file share.</span></span>
<span data-ttu-id="9e142-167">Questo cmdlet viene caricato in un file nella condivisione file specificata dal parametro.</span><span class="sxs-lookup"><span data-stu-id="9e142-167">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="9e142-168">-Origine</span><span class="sxs-lookup"><span data-stu-id="9e142-168">-Source</span></span>
<span data-ttu-id="9e142-169">Specifica il file di origine caricato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e142-169">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="9e142-170">Se specifichi un file che non esiste, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9e142-170">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9e142-171">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e142-171">-Confirm</span></span>
<span data-ttu-id="9e142-172">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e142-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e142-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e142-173">-WhatIf</span></span>
<span data-ttu-id="9e142-174">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e142-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e142-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e142-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e142-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e142-176">CommonParameters</span></span>
<span data-ttu-id="9e142-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e142-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e142-178">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e142-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e142-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e142-179">INPUTS</span></span>

### <span data-ttu-id="9e142-180">Microsoft. WindowsAzure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9e142-180">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="9e142-181">Microsoft. WindowsAzure. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="9e142-181">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="9e142-182">System. String</span><span class="sxs-lookup"><span data-stu-id="9e142-182">System.String</span></span>

### <span data-ttu-id="9e142-183">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9e142-183">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9e142-184">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e142-184">OUTPUTS</span></span>

### <span data-ttu-id="9e142-185">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="9e142-185">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="9e142-186">Note</span><span class="sxs-lookup"><span data-stu-id="9e142-186">NOTES</span></span>

## <span data-ttu-id="9e142-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e142-187">RELATED LINKS</span></span>

[<span data-ttu-id="9e142-188">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="9e142-188">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="9e142-189">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="9e142-189">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="9e142-190">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9e142-190">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
