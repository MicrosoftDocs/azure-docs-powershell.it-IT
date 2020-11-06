---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: ''
schema: 2.0.0
ms.openlocfilehash: f7b68be6981343d14f7d1d8530a0af3c3eee199c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507099"
---
# <span data-ttu-id="152dd-101">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="152dd-101">Get-AzureStorageBlob</span></span>

## <span data-ttu-id="152dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="152dd-102">SYNOPSIS</span></span>
<span data-ttu-id="152dd-103">Elenca i BLOB in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="152dd-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="152dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="152dd-104">SYNTAX</span></span>

### <span data-ttu-id="152dd-105">Blobname (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="152dd-105">BlobName (Default)</span></span>
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="152dd-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="152dd-106">BlobPrefix</span></span>
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="152dd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="152dd-107">DESCRIPTION</span></span>
<span data-ttu-id="152dd-108">Il cmdlet **Get-AzureStorageBlob** elenca i BLOB nel contenitore specificato in un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="152dd-108">The **Get-AzureStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="152dd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="152dd-109">EXAMPLES</span></span>

### <span data-ttu-id="152dd-110">Esempio 1: ottenere un BLOB per nome BLOB</span><span class="sxs-lookup"><span data-stu-id="152dd-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="152dd-111">Questo comando usa un nome BLOB e un carattere jolly per ottenere un BLOB.</span><span class="sxs-lookup"><span data-stu-id="152dd-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="152dd-112">Esempio 2: ottenere un BLOB usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="152dd-112">Example 2: Get a blob by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob
```

<span data-ttu-id="152dd-113">Questo comando usa la pipeline per ottenere un BLOB.</span><span class="sxs-lookup"><span data-stu-id="152dd-113">This command uses the pipeline to get a blob.</span></span>

### <span data-ttu-id="152dd-114">Esempio 3: ottenere un prefisso BLOB per nome</span><span class="sxs-lookup"><span data-stu-id="152dd-114">Example 3: Get a blob by name prefix</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="152dd-115">Questo comando usa un prefisso di nome per ottenere un BLOB.</span><span class="sxs-lookup"><span data-stu-id="152dd-115">This command uses a name prefix to get a blob.</span></span>

### <span data-ttu-id="152dd-116">Esempio 4: elencare i BLOB in più batch</span><span class="sxs-lookup"><span data-stu-id="152dd-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="152dd-117">Questo esempio usa i parametri *maxCount* e *ContinuationToken* per elencare i BLOB di archiviazione di Azure in più batch.</span><span class="sxs-lookup"><span data-stu-id="152dd-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="152dd-118">I primi quattro comandi assegnano valori alle variabili da usare nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="152dd-118">The first four commands assign values to variables to use in the example.</span></span>

<span data-ttu-id="152dd-119">Il quinto comando specifica un'istruzione **do-while** che usa il cmdlet **Get-AzureStorageBlob** per ottenere i BLOB.</span><span class="sxs-lookup"><span data-stu-id="152dd-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzureStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="152dd-120">L'istruzione include il token di continuazione archiviato nella variabile $Token.</span><span class="sxs-lookup"><span data-stu-id="152dd-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="152dd-121">$Token cambia il valore durante l'esecuzione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="152dd-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="152dd-122">Per altre informazioni, digitare `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="152dd-122">For more information, type `Get-Help About_Do`.</span></span>

<span data-ttu-id="152dd-123">Il comando finale usa il comando **echo** per visualizzare il totale.</span><span class="sxs-lookup"><span data-stu-id="152dd-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="152dd-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="152dd-124">PARAMETERS</span></span>

### <span data-ttu-id="152dd-125">-BLOB</span><span class="sxs-lookup"><span data-stu-id="152dd-125">-Blob</span></span>
<span data-ttu-id="152dd-126">Specifica un nome o un modello di nome, che può essere usato per una ricerca con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="152dd-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="152dd-127">Se non viene specificato alcun nome BLOB, il cmdlet elenca tutti i BLOB nel contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="152dd-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="152dd-128">Se viene specificato un valore per questo parametro, il cmdlet elenca tutti i BLOB con i nomi che corrispondono a questo parametro.</span><span class="sxs-lookup"><span data-stu-id="152dd-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152dd-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="152dd-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="152dd-130">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="152dd-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="152dd-131">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="152dd-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="152dd-132">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="152dd-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="152dd-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="152dd-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="152dd-134">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="152dd-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="152dd-135">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="152dd-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="152dd-136">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="152dd-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="152dd-137">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="152dd-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="152dd-138">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="152dd-138">The default value is 10.</span></span>

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

### <span data-ttu-id="152dd-139">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="152dd-139">-Container</span></span>
<span data-ttu-id="152dd-140">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="152dd-140">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="152dd-141">-Contesto</span><span class="sxs-lookup"><span data-stu-id="152dd-141">-Context</span></span>
<span data-ttu-id="152dd-142">Specifica l'account di archiviazione di Azure da cui si vuole ottenere un elenco di BLOB.</span><span class="sxs-lookup"><span data-stu-id="152dd-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="152dd-143">Puoi usare il cmdlet New-AzureStorageContext per creare un contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="152dd-143">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="152dd-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="152dd-144">-ContinuationToken</span></span>
<span data-ttu-id="152dd-145">Specifica un token di continuazione per l'elenco di BLOB.</span><span class="sxs-lookup"><span data-stu-id="152dd-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="152dd-146">Usa questo parametro e il parametro *maxCount* per elencare i BLOB in più batch.</span><span class="sxs-lookup"><span data-stu-id="152dd-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152dd-147">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="152dd-147">-MaxCount</span></span>
<span data-ttu-id="152dd-148">Specifica il numero massimo di oggetti restituiti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="152dd-148">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="152dd-149">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="152dd-149">-Prefix</span></span>
<span data-ttu-id="152dd-150">Specifica un prefisso per i nomi di BLOB che si desidera ottenere.</span><span class="sxs-lookup"><span data-stu-id="152dd-150">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="152dd-151">Questo parametro non supporta l'uso di espressioni regolari o caratteri jolly per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="152dd-151">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="152dd-152">Questo significa che se il contenitore contiene solo oggetti BLOB denominati "My", "MyBlob1" e "MyBlob2" e specifichi "-prefix My \*", il cmdlet non restituisce alcun BLOB.</span><span class="sxs-lookup"><span data-stu-id="152dd-152">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="152dd-153">Se invece specifichi "-prefix My", il cmdlet restituirà "My", "MyBlob1" e "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="152dd-153">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: String
Parameter Sets: BlobPrefix
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152dd-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="152dd-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="152dd-155">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="152dd-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="152dd-156">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="152dd-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="152dd-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152dd-157">CommonParameters</span></span>
<span data-ttu-id="152dd-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="152dd-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152dd-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="152dd-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152dd-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="152dd-160">INPUTS</span></span>

## <span data-ttu-id="152dd-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="152dd-161">OUTPUTS</span></span>

### <span data-ttu-id="152dd-162">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="152dd-162">AzureStorageBlob</span></span>

## <span data-ttu-id="152dd-163">Note</span><span class="sxs-lookup"><span data-stu-id="152dd-163">NOTES</span></span>
* <span data-ttu-id="152dd-164">Sinossi</span><span class="sxs-lookup"><span data-stu-id="152dd-164">SYNOPSIS</span></span>

## <span data-ttu-id="152dd-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="152dd-165">RELATED LINKS</span></span>

[<span data-ttu-id="152dd-166">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="152dd-166">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="152dd-167">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="152dd-167">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)

[<span data-ttu-id="152dd-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="152dd-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)


