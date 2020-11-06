---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1caded810569225bfa269e7c0d29c60be87d4fb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93506948"
---
# <span data-ttu-id="f9ce4-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f9ce4-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="f9ce4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ce4-103">Carica un file locale in un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="f9ce4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9ce4-104">SYNTAX</span></span>

### <span data-ttu-id="f9ce4-105">SendManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9ce4-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ce4-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="f9ce4-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ce4-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="f9ce4-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9ce4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9ce4-108">DESCRIPTION</span></span>
<span data-ttu-id="f9ce4-109">Il cmdlet **set-AzureStorageBlobContent** carica un file locale in un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="f9ce4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9ce4-110">EXAMPLES</span></span>

### <span data-ttu-id="f9ce4-111">Esempio 1: caricare un file denominato</span><span class="sxs-lookup"><span data-stu-id="f9ce4-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="f9ce4-112">Questo comando carica il file denominato PlanningData in un BLOB denominato Planning2015.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="f9ce4-113">Esempio 2: caricare tutti i file nella cartella corrente</span><span class="sxs-lookup"><span data-stu-id="f9ce4-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="f9ce4-114">Questo comando usa il cmdlet di Windows PowerShell di base Get-ChildItem per ottenere tutti i file nella cartella corrente e nelle sottocartelle e quindi li passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f9ce4-115">Il cmdlet **set-AzureStorageBlobContent** carica i file nel contenitore denominato ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="f9ce4-116">Esempio 3: sovrascrivere un BLOB esistente</span><span class="sxs-lookup"><span data-stu-id="f9ce4-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="f9ce4-117">Questo comando ottiene il BLOB denominato Planning2015 nel contenitore ContosoUploads usando il cmdlet Get-AzureStorageBlob e quindi passa tale BLOB al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="f9ce4-118">Il comando carica il file denominato ContosoPlanning come Planning2015.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="f9ce4-119">Questo comando non specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="f9ce4-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="f9ce4-120">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="f9ce4-121">Se si conferma il comando, il cmdlet sovrascrive il BLOB esistente.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="f9ce4-122">Esempio 4: caricare un file in un contenitore tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="f9ce4-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="f9ce4-123">Questo comando ottiene il contenitore che inizia con la stringa ContosoUpload usando il cmdlet **Get-AzureStorageContainer** e quindi passa tale BLOB al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="f9ce4-124">Il comando carica il file denominato ContosoPlanning come Planning2015.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="f9ce4-125">Esempio 5: caricare un file e i metadati</span><span class="sxs-lookup"><span data-stu-id="f9ce4-125">Example 5: Upload a file and metadata</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata
```

<span data-ttu-id="f9ce4-126">Il primo comando crea una tabella hash che contiene metadati per un BLOB e archivia la tabella hash nella variabile $Metadata.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="f9ce4-127">Il secondo comando carica il file denominato ContosoPlanning nel contenitore denominato ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="f9ce4-128">Il BLOB include i metadati archiviati in $Metadata.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-128">The blob includes the metadata stored in $Metadata.</span></span>

## <span data-ttu-id="f9ce4-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9ce4-129">PARAMETERS</span></span>

### <span data-ttu-id="f9ce4-130">-BLOB</span><span class="sxs-lookup"><span data-stu-id="f9ce4-130">-Blob</span></span>
<span data-ttu-id="f9ce4-131">Specifica il nome di un BLOB.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-131">Specifies the name of a blob.</span></span>
<span data-ttu-id="f9ce4-132">Questo cmdlet carica un file nel BLOB di archiviazione di Azure specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-132">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual, ContainerPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ce4-133">-BlobType</span><span class="sxs-lookup"><span data-stu-id="f9ce4-133">-BlobType</span></span>
<span data-ttu-id="f9ce4-134">Specifica il tipo per il BLOB caricato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-134">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="f9ce4-135">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9ce4-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9ce4-136">Blocco</span><span class="sxs-lookup"><span data-stu-id="f9ce4-136">Block</span></span>
- <span data-ttu-id="f9ce4-137">Pagina</span><span class="sxs-lookup"><span data-stu-id="f9ce4-137">Page</span></span>

<span data-ttu-id="f9ce4-138">Il valore predefinito è Block.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-138">The default value is Block.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ce4-139">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f9ce4-139">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f9ce4-140">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f9ce4-141">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f9ce4-142">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f9ce4-143">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="f9ce4-143">-CloudBlob</span></span>
<span data-ttu-id="f9ce4-144">Specifica un oggetto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="f9ce4-144">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="f9ce4-145">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-145">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ce4-146">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="f9ce4-146">-CloudBlobContainer</span></span>
<span data-ttu-id="f9ce4-147">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-147">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="f9ce4-148">Questo cmdlet carica il contenuto in un BLOB nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-148">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="f9ce4-149">Per ottenere un oggetto **CloudBlobContainer** , usa il cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-149">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ce4-150">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f9ce4-150">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f9ce4-151">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-151">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f9ce4-152">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-152">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f9ce4-153">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-153">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f9ce4-154">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-154">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f9ce4-155">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-155">The default value is 10.</span></span>

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

### <span data-ttu-id="f9ce4-156">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="f9ce4-156">-Container</span></span>
<span data-ttu-id="f9ce4-157">Specifica il nome di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-157">Specifies the name of a container.</span></span>
<span data-ttu-id="f9ce4-158">Questo cmdlet carica un file in un BLOB nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-158">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ce4-159">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f9ce4-159">-Context</span></span>
<span data-ttu-id="f9ce4-160">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f9ce4-161">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ce4-162">-File</span><span class="sxs-lookup"><span data-stu-id="f9ce4-162">-File</span></span>
<span data-ttu-id="f9ce4-163">Specifica un percorso di file locale per un file da caricare come contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-163">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ce4-164">-Force</span><span class="sxs-lookup"><span data-stu-id="f9ce4-164">-Force</span></span>
<span data-ttu-id="f9ce4-165">Indica che questo cmdlet sovrascrive un BLOB esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-165">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f9ce4-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f9ce4-166">-Metadata</span></span>
<span data-ttu-id="f9ce4-167">Specifica i metadati per il BLOB caricato.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-167">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ce4-168">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="f9ce4-168">-Properties</span></span>
<span data-ttu-id="f9ce4-169">Specifica le proprietà per il BLOB caricato.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-169">Specifies properties for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ce4-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f9ce4-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f9ce4-171">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-171">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="f9ce4-172">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-172">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="f9ce4-173">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f9ce4-173">-Confirm</span></span>
<span data-ttu-id="f9ce4-174">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9ce4-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ce4-175">-WhatIf</span></span>
<span data-ttu-id="f9ce4-176">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9ce4-177">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9ce4-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ce4-178">CommonParameters</span></span>
<span data-ttu-id="f9ce4-179">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9ce4-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ce4-180">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9ce4-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ce4-181">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9ce4-181">INPUTS</span></span>

## <span data-ttu-id="f9ce4-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9ce4-182">OUTPUTS</span></span>

## <span data-ttu-id="f9ce4-183">Note</span><span class="sxs-lookup"><span data-stu-id="f9ce4-183">NOTES</span></span>

## <span data-ttu-id="f9ce4-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9ce4-184">RELATED LINKS</span></span>

[<span data-ttu-id="f9ce4-185">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f9ce4-185">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="f9ce4-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f9ce4-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="f9ce4-187">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f9ce4-187">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
