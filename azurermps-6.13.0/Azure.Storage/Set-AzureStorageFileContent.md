---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
ms.openlocfilehash: 84192a4715087d5ae896067e02ab07ef27574410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507803"
---
# <span data-ttu-id="2621d-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2621d-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="2621d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2621d-102">SYNOPSIS</span></span>
<span data-ttu-id="2621d-103">Carica il contenuto di un file.</span><span class="sxs-lookup"><span data-stu-id="2621d-103">Uploads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2621d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2621d-104">SYNTAX</span></span>

### <span data-ttu-id="2621d-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2621d-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2621d-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="2621d-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2621d-107">Directory</span><span class="sxs-lookup"><span data-stu-id="2621d-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2621d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2621d-108">DESCRIPTION</span></span>
<span data-ttu-id="2621d-109">Il cmdlet **set-AzureStorageFileContent** carica il contenuto di un file in un file in una condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="2621d-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="2621d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2621d-110">EXAMPLES</span></span>

### <span data-ttu-id="2621d-111">Esempio 1: caricare un file nella cartella corrente</span><span class="sxs-lookup"><span data-stu-id="2621d-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="2621d-112">Questo comando carica un file denominato DataFile37 nella cartella corrente come un file denominato CurrentDataFile nella cartella denominata ContosoWorkingFolder.</span><span class="sxs-lookup"><span data-stu-id="2621d-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="2621d-113">Esempio 2: caricare tutti i file nella cartella corrente</span><span class="sxs-lookup"><span data-stu-id="2621d-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="2621d-114">Questo esempio usa diversi cmdlet di Windows PowerShell comuni e il cmdlet corrente per caricare tutti i file dalla cartella corrente nella cartella radice di container ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="2621d-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="2621d-115">Il primo comando ottiene il nome della cartella corrente e lo archivia nella variabile $CurrentFolder.</span><span class="sxs-lookup"><span data-stu-id="2621d-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="2621d-116">Il secondo comando usa il cmdlet **Get-AzureStorageShare** per ottenere la condivisione di file denominata ContosoShare06 e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="2621d-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2621d-117">Il comando finale Recupera il contenuto della cartella corrente e passa ognuno al cmdlet Where-Object usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="2621d-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2621d-118">Questo cmdlet filtra gli oggetti che non sono file e quindi passa i file al cmdlet ForEach-Object.</span><span class="sxs-lookup"><span data-stu-id="2621d-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="2621d-119">Questo cmdlet esegue un blocco di script per ogni file che crea il percorso appropriato e quindi usa il cmdlet Current per caricare il file.</span><span class="sxs-lookup"><span data-stu-id="2621d-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="2621d-120">Il risultato ha lo stesso nome e la stessa posizione relativa rispetto agli altri file caricati in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="2621d-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="2621d-121">Per altre informazioni sui blocchi di script, digitare `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="2621d-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="2621d-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2621d-122">PARAMETERS</span></span>

### <span data-ttu-id="2621d-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2621d-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2621d-124">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="2621d-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2621d-125">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="2621d-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2621d-126">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="2621d-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2621d-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2621d-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2621d-128">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="2621d-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2621d-129">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="2621d-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2621d-130">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="2621d-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2621d-131">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="2621d-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2621d-132">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="2621d-132">The default value is 10.</span></span>

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

### <span data-ttu-id="2621d-133">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2621d-133">-Context</span></span>
<span data-ttu-id="2621d-134">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2621d-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2621d-135">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="2621d-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="2621d-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2621d-136">-DefaultProfile</span></span>
<span data-ttu-id="2621d-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2621d-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2621d-138">-Directory</span><span class="sxs-lookup"><span data-stu-id="2621d-138">-Directory</span></span>
<span data-ttu-id="2621d-139">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="2621d-139">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="2621d-140">Questo cmdlet carica il file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2621d-140">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="2621d-141">Per ottenere una directory, usare il cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="2621d-141">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="2621d-142">Puoi anche usare il cmdlet Get-AzureStorageFile per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="2621d-142">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="2621d-143">-Force</span><span class="sxs-lookup"><span data-stu-id="2621d-143">-Force</span></span>
<span data-ttu-id="2621d-144">Indica che questo cmdlet sovrascrive un file di archiviazione di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="2621d-144">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="2621d-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2621d-145">-PassThru</span></span>
<span data-ttu-id="2621d-146">Indica che questo cmdlet restituisce l'oggetto **AzureStorageFile** che crea o carica.</span><span class="sxs-lookup"><span data-stu-id="2621d-146">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="2621d-147">-Path</span><span class="sxs-lookup"><span data-stu-id="2621d-147">-Path</span></span>
<span data-ttu-id="2621d-148">Specifica il percorso di un file o di una cartella.</span><span class="sxs-lookup"><span data-stu-id="2621d-148">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="2621d-149">Questo cmdlet carica il contenuto nel file specificato da questo parametro o in un file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2621d-149">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="2621d-150">Se specifichi una cartella, questo cmdlet crea un file con lo stesso nome del file di origine.</span><span class="sxs-lookup"><span data-stu-id="2621d-150">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="2621d-151">Se specifichi un percorso di un file che non esiste, questo cmdlet crea il file e salva il contenuto in tale file.</span><span class="sxs-lookup"><span data-stu-id="2621d-151">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="2621d-152">Se si specifica un file già esistente e si specifica il parametro _Force_ , questo cmdlet sovrascrive il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="2621d-152">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="2621d-153">Se si specifica un file già esistente e non si specifica _Force_ , questo cmdlet non apporta alcuna modifica e restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="2621d-153">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="2621d-154">Se si specifica un percorso di una cartella che non esiste, questo cmdlet non apporta alcuna modifica e restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="2621d-154">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="2621d-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2621d-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2621d-156">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="2621d-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="2621d-157">-Condividi</span><span class="sxs-lookup"><span data-stu-id="2621d-157">-Share</span></span>
<span data-ttu-id="2621d-158">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="2621d-158">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="2621d-159">Questo cmdlet viene caricato in un file nella condivisione file specificata dal parametro.</span><span class="sxs-lookup"><span data-stu-id="2621d-159">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="2621d-160">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="2621d-160">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="2621d-161">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2621d-161">This object contains the storage context.</span></span>
<span data-ttu-id="2621d-162">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="2621d-162">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="2621d-163">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2621d-163">-ShareName</span></span>
<span data-ttu-id="2621d-164">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="2621d-164">Specifies the name of the file share.</span></span>
<span data-ttu-id="2621d-165">Questo cmdlet viene caricato in un file nella condivisione file specificata dal parametro.</span><span class="sxs-lookup"><span data-stu-id="2621d-165">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="2621d-166">-Origine</span><span class="sxs-lookup"><span data-stu-id="2621d-166">-Source</span></span>
<span data-ttu-id="2621d-167">Specifica il file di origine caricato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2621d-167">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="2621d-168">Se specifichi un file che non esiste, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="2621d-168">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2621d-169">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2621d-169">-Confirm</span></span>
<span data-ttu-id="2621d-170">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2621d-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2621d-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2621d-171">-WhatIf</span></span>
<span data-ttu-id="2621d-172">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2621d-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2621d-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2621d-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2621d-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2621d-174">CommonParameters</span></span>
<span data-ttu-id="2621d-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2621d-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2621d-176">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2621d-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2621d-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2621d-177">INPUTS</span></span>

### <span data-ttu-id="2621d-178">Microsoft. WindowsAzure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2621d-178">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="2621d-179">Parametri: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2621d-179">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="2621d-180">Microsoft. WindowsAzure. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="2621d-180">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="2621d-181">Parameters: directory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2621d-181">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="2621d-182">System. String</span><span class="sxs-lookup"><span data-stu-id="2621d-182">System.String</span></span>

### <span data-ttu-id="2621d-183">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2621d-183">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2621d-184">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2621d-184">OUTPUTS</span></span>

### <span data-ttu-id="2621d-185">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="2621d-185">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="2621d-186">Note</span><span class="sxs-lookup"><span data-stu-id="2621d-186">NOTES</span></span>

## <span data-ttu-id="2621d-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2621d-187">RELATED LINKS</span></span>

[<span data-ttu-id="2621d-188">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="2621d-188">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="2621d-189">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="2621d-189">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="2621d-190">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2621d-190">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)