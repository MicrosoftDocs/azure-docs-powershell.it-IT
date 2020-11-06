---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
ms.openlocfilehash: 5023643ae57ab73ea625254f7b2362c947209f8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510204"
---
# <span data-ttu-id="670ba-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="670ba-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="670ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="670ba-102">SYNOPSIS</span></span>
<span data-ttu-id="670ba-103">Scarica un BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="670ba-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="670ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="670ba-104">SYNTAX</span></span>

### <span data-ttu-id="670ba-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="670ba-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="670ba-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="670ba-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="670ba-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="670ba-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="670ba-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="670ba-108">DESCRIPTION</span></span>
<span data-ttu-id="670ba-109">Il cmdlet **Get-AzureStorageBlobContent** Scarica il BLOB di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="670ba-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="670ba-110">Se il nome del BLOB non è valido per il computer locale, questo cmdlet lo risolve automaticamente, se possibile.</span><span class="sxs-lookup"><span data-stu-id="670ba-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="670ba-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="670ba-111">EXAMPLES</span></span>

### <span data-ttu-id="670ba-112">Esempio 1: scaricare il contenuto BLOB per nome</span><span class="sxs-lookup"><span data-stu-id="670ba-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="670ba-113">Questo comando Scarica un BLOB per nome.</span><span class="sxs-lookup"><span data-stu-id="670ba-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="670ba-114">Esempio 2: scaricare il contenuto BLOB usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="670ba-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="670ba-115">Questo comando usa la pipeline per trovare e scaricare contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="670ba-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="670ba-116">Esempio 3: scaricare il contenuto BLOB usando la pipeline e un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="670ba-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="670ba-117">Questo esempio usa il carattere jolly asterisco e la pipeline per trovare e scaricare contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="670ba-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="670ba-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="670ba-118">PARAMETERS</span></span>

### <span data-ttu-id="670ba-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="670ba-119">-Blob</span></span>
<span data-ttu-id="670ba-120">Specifica il nome del BLOB da scaricare.</span><span class="sxs-lookup"><span data-stu-id="670ba-120">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670ba-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="670ba-121">-CheckMd5</span></span>
<span data-ttu-id="670ba-122">Specifica se controllare la somma MD5 per il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="670ba-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="670ba-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="670ba-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="670ba-124">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="670ba-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="670ba-125">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="670ba-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="670ba-126">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="670ba-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="670ba-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="670ba-127">-CloudBlob</span></span>
<span data-ttu-id="670ba-128">Specifica un BLOB cloud.</span><span class="sxs-lookup"><span data-stu-id="670ba-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="670ba-129">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="670ba-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="670ba-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="670ba-130">-CloudBlobContainer</span></span>
<span data-ttu-id="670ba-131">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="670ba-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="670ba-132">Puoi crearlo o usare il cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="670ba-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="670ba-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="670ba-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="670ba-134">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="670ba-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="670ba-135">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="670ba-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="670ba-136">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="670ba-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="670ba-137">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="670ba-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="670ba-138">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="670ba-138">The default value is 10.</span></span>

<span data-ttu-id="670ba-139">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="670ba-139">The default value is 10.</span></span>

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

### <span data-ttu-id="670ba-140">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="670ba-140">-Container</span></span>
<span data-ttu-id="670ba-141">Specifica il nome del contenitore con il BLOB che si vuole scaricare.</span><span class="sxs-lookup"><span data-stu-id="670ba-141">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670ba-142">-Contesto</span><span class="sxs-lookup"><span data-stu-id="670ba-142">-Context</span></span>
<span data-ttu-id="670ba-143">Specifica l'account di archiviazione di Azure da cui si vuole scaricare il contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="670ba-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="670ba-144">Puoi usare il cmdlet New-AzureStorageContext per creare un contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="670ba-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="670ba-145">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="670ba-145">-Destination</span></span>
<span data-ttu-id="670ba-146">Specifica il percorso in cui archiviare il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="670ba-146">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670ba-147">-Force</span><span class="sxs-lookup"><span data-stu-id="670ba-147">-Force</span></span>
<span data-ttu-id="670ba-148">Sovrascrive un file esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="670ba-148">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="670ba-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="670ba-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="670ba-150">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="670ba-150">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="670ba-151">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="670ba-151">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="670ba-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="670ba-152">-Confirm</span></span>
<span data-ttu-id="670ba-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="670ba-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="670ba-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="670ba-154">-WhatIf</span></span>
<span data-ttu-id="670ba-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="670ba-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="670ba-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="670ba-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="670ba-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670ba-157">CommonParameters</span></span>
<span data-ttu-id="670ba-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="670ba-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670ba-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="670ba-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670ba-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="670ba-160">INPUTS</span></span>

### <span data-ttu-id="670ba-161">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="670ba-161">IStorageContext</span></span>

<span data-ttu-id="670ba-162">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="670ba-162">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="670ba-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="670ba-163">OUTPUTS</span></span>

### <span data-ttu-id="670ba-164">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="670ba-164">AzureStorageContainer</span></span>

## <span data-ttu-id="670ba-165">Note</span><span class="sxs-lookup"><span data-stu-id="670ba-165">NOTES</span></span>
* <span data-ttu-id="670ba-166">Se il nome del BLOB non è valido per il computer locale, questo cmdlet la risolve in autonomia, se possibile.</span><span class="sxs-lookup"><span data-stu-id="670ba-166">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="670ba-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="670ba-167">RELATED LINKS</span></span>

[<span data-ttu-id="670ba-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="670ba-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="670ba-169">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="670ba-169">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="670ba-170">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="670ba-170">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)