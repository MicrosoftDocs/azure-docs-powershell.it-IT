---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: dc825c5c79c3e314fc6b330c441f82543cc9fd23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857837"
---
# <span data-ttu-id="370b3-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="370b3-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="370b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="370b3-102">SYNOPSIS</span></span>
<span data-ttu-id="370b3-103">Elenca i BLOB in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="370b3-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="370b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="370b3-104">SYNTAX</span></span>

### <span data-ttu-id="370b3-105">Blobname (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="370b3-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="370b3-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="370b3-106">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="370b3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="370b3-107">DESCRIPTION</span></span>
<span data-ttu-id="370b3-108">Il cmdlet **Get-AzStorageBlob** elenca i BLOB nel contenitore specificato in un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="370b3-108">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="370b3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="370b3-109">EXAMPLES</span></span>

### <span data-ttu-id="370b3-110">Esempio 1: ottenere un BLOB per nome BLOB</span><span class="sxs-lookup"><span data-stu-id="370b3-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="370b3-111">Questo comando usa un nome BLOB e un carattere jolly per ottenere un BLOB.</span><span class="sxs-lookup"><span data-stu-id="370b3-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="370b3-112">Esempio 2: ottenere BLOB in un contenitore tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="370b3-112">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="370b3-113">Questo comando usa la pipeline per ottenere tutti i BLOB (Includi BLOB nello stato eliminato) in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="370b3-113">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="370b3-114">Esempio 3: ottenere i BLOB in base al prefisso del nome</span><span class="sxs-lookup"><span data-stu-id="370b3-114">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="370b3-115">Questo comando usa un prefisso di nome per ottenere i BLOB.</span><span class="sxs-lookup"><span data-stu-id="370b3-115">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="370b3-116">Esempio 4: elencare i BLOB in più batch</span><span class="sxs-lookup"><span data-stu-id="370b3-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="370b3-117">Questo esempio usa i parametri *maxCount* e *ContinuationToken* per elencare i BLOB di archiviazione di Azure in più batch.</span><span class="sxs-lookup"><span data-stu-id="370b3-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="370b3-118">I primi quattro comandi assegnano valori alle variabili da usare nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="370b3-118">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="370b3-119">Il quinto comando specifica un'istruzione **do-while** che usa il cmdlet **Get-AzStorageBlob** per ottenere i BLOB.</span><span class="sxs-lookup"><span data-stu-id="370b3-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="370b3-120">L'istruzione include il token di continuazione archiviato nella variabile $Token.</span><span class="sxs-lookup"><span data-stu-id="370b3-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="370b3-121">$Token cambia il valore durante l'esecuzione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="370b3-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="370b3-122">Per altre informazioni, digitare `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="370b3-122">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="370b3-123">Il comando finale usa il comando **echo** per visualizzare il totale.</span><span class="sxs-lookup"><span data-stu-id="370b3-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="370b3-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="370b3-124">PARAMETERS</span></span>

### <span data-ttu-id="370b3-125">-BLOB</span><span class="sxs-lookup"><span data-stu-id="370b3-125">-Blob</span></span>
<span data-ttu-id="370b3-126">Specifica un nome o un modello di nome, che può essere usato per una ricerca con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="370b3-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="370b3-127">Se non viene specificato alcun nome BLOB, il cmdlet elenca tutti i BLOB nel contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="370b3-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="370b3-128">Se viene specificato un valore per questo parametro, il cmdlet elenca tutti i BLOB con i nomi che corrispondono a questo parametro.</span><span class="sxs-lookup"><span data-stu-id="370b3-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370b3-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="370b3-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="370b3-130">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="370b3-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="370b3-131">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="370b3-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="370b3-132">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="370b3-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="370b3-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="370b3-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="370b3-134">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="370b3-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="370b3-135">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="370b3-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="370b3-136">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="370b3-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="370b3-137">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="370b3-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="370b3-138">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="370b3-138">The default value is 10.</span></span>

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

### <span data-ttu-id="370b3-139">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="370b3-139">-Container</span></span>
<span data-ttu-id="370b3-140">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="370b3-140">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370b3-141">-Contesto</span><span class="sxs-lookup"><span data-stu-id="370b3-141">-Context</span></span>
<span data-ttu-id="370b3-142">Specifica l'account di archiviazione di Azure da cui si vuole ottenere un elenco di BLOB.</span><span class="sxs-lookup"><span data-stu-id="370b3-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="370b3-143">Puoi usare il cmdlet New-AzStorageContext per creare un contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="370b3-143">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="370b3-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="370b3-144">-ContinuationToken</span></span>
<span data-ttu-id="370b3-145">Specifica un token di continuazione per l'elenco di BLOB.</span><span class="sxs-lookup"><span data-stu-id="370b3-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="370b3-146">Usa questo parametro e il parametro *maxCount* per elencare i BLOB in più batch.</span><span class="sxs-lookup"><span data-stu-id="370b3-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370b3-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="370b3-147">-DefaultProfile</span></span>
<span data-ttu-id="370b3-148">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="370b3-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="370b3-149">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="370b3-149">-IncludeDeleted</span></span>
<span data-ttu-id="370b3-150">Includi BLOB eliminati, per impostazione predefinita, Get BLOB non includerà BLOB eliminati.</span><span class="sxs-lookup"><span data-stu-id="370b3-150">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="370b3-151">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="370b3-151">-MaxCount</span></span>
<span data-ttu-id="370b3-152">Specifica il numero massimo di oggetti restituiti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="370b3-152">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="370b3-153">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="370b3-153">-Prefix</span></span>
<span data-ttu-id="370b3-154">Specifica un prefisso per i nomi di BLOB che si desidera ottenere.</span><span class="sxs-lookup"><span data-stu-id="370b3-154">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="370b3-155">Questo parametro non supporta l'uso di espressioni regolari o caratteri jolly per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="370b3-155">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="370b3-156">Questo significa che se il contenitore contiene solo oggetti BLOB denominati "My", "MyBlob1" e "MyBlob2" e specifichi "-prefix My \*", il cmdlet non restituisce alcun BLOB.</span><span class="sxs-lookup"><span data-stu-id="370b3-156">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="370b3-157">Se invece specifichi "-prefix My", il cmdlet restituirà "My", "MyBlob1" e "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="370b3-157">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370b3-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="370b3-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="370b3-159">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="370b3-159">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="370b3-160">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="370b3-160">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="370b3-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="370b3-161">CommonParameters</span></span>
<span data-ttu-id="370b3-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="370b3-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="370b3-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="370b3-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="370b3-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="370b3-164">INPUTS</span></span>

### <span data-ttu-id="370b3-165">System. String</span><span class="sxs-lookup"><span data-stu-id="370b3-165">System.String</span></span>

### <span data-ttu-id="370b3-166">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="370b3-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="370b3-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="370b3-167">OUTPUTS</span></span>

### <span data-ttu-id="370b3-168">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="370b3-168">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="370b3-169">Note</span><span class="sxs-lookup"><span data-stu-id="370b3-169">NOTES</span></span>

## <span data-ttu-id="370b3-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="370b3-170">RELATED LINKS</span></span>

[<span data-ttu-id="370b3-171">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="370b3-171">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="370b3-172">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="370b3-172">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="370b3-173">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="370b3-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


