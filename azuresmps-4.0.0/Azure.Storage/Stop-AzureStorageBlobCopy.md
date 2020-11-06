---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bdb5a02f474f575f90406ad9026b4437194dffb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507151"
---
# <span data-ttu-id="10ee1-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10ee1-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="10ee1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="10ee1-103">Interrompe un'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="10ee1-103">Stops a copy operation.</span></span>

## <span data-ttu-id="10ee1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10ee1-104">SYNTAX</span></span>

### <span data-ttu-id="10ee1-105">NamePipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10ee1-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ee1-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="10ee1-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ee1-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="10ee1-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10ee1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10ee1-108">DESCRIPTION</span></span>
<span data-ttu-id="10ee1-109">Il cmdlet **Stop-AzureStorageBlobCopy** interrompe un'operazione di copia nel BLOB di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="10ee1-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="10ee1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10ee1-110">EXAMPLES</span></span>

### <span data-ttu-id="10ee1-111">Esempio 1: interrompere l'operazione di copia per nome</span><span class="sxs-lookup"><span data-stu-id="10ee1-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="10ee1-112">Questo comando interrompe l'operazione di copia per nome.</span><span class="sxs-lookup"><span data-stu-id="10ee1-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="10ee1-113">Esempio 2: interrompere l'operazione di copia usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="10ee1-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="10ee1-114">Questo comando interrompe l'operazione di copia passando il contenitore sulla pipeline da **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="10ee1-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="10ee1-115">Esempio 3: interrompere l'operazione di copia usando la pipeline e Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="10ee1-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="10ee1-116">Questo esempio interrompe l'operazione di copia passando il contenitore sulla pipeline dal cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="10ee1-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="10ee1-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10ee1-117">PARAMETERS</span></span>

### <span data-ttu-id="10ee1-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="10ee1-118">-Blob</span></span>
<span data-ttu-id="10ee1-119">Specifica il nome del BLOB.</span><span class="sxs-lookup"><span data-stu-id="10ee1-119">Specifies the name of the blob.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ee1-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="10ee1-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="10ee1-121">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="10ee1-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="10ee1-122">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="10ee1-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="10ee1-123">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="10ee1-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="10ee1-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="10ee1-124">-CloudBlob</span></span>
<span data-ttu-id="10ee1-125">Specifica un oggetto **CloudBlob** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="10ee1-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="10ee1-126">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="10ee1-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="10ee1-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="10ee1-127">-CloudBlobContainer</span></span>
<span data-ttu-id="10ee1-128">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="10ee1-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="10ee1-129">Puoi creare l'oggetto o usare il cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="10ee1-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="10ee1-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="10ee1-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="10ee1-131">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="10ee1-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="10ee1-132">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="10ee1-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="10ee1-133">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="10ee1-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="10ee1-134">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="10ee1-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="10ee1-135">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="10ee1-135">The default value is 10.</span></span>

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

### <span data-ttu-id="10ee1-136">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="10ee1-136">-Container</span></span>
<span data-ttu-id="10ee1-137">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="10ee1-137">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ee1-138">-Contesto</span><span class="sxs-lookup"><span data-stu-id="10ee1-138">-Context</span></span>
<span data-ttu-id="10ee1-139">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="10ee1-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="10ee1-140">Puoi creare il contesto usando il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="10ee1-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="10ee1-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="10ee1-141">-CopyId</span></span>
<span data-ttu-id="10ee1-142">Specifica l'ID copia.</span><span class="sxs-lookup"><span data-stu-id="10ee1-142">Specifies the copy ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ee1-143">-Force</span><span class="sxs-lookup"><span data-stu-id="10ee1-143">-Force</span></span>
<span data-ttu-id="10ee1-144">Interrompe l'attività di copia corrente nel BLOB specificato senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="10ee1-144">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="10ee1-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="10ee1-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="10ee1-146">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="10ee1-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="10ee1-147">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="10ee1-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="10ee1-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="10ee1-148">-Confirm</span></span>
<span data-ttu-id="10ee1-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10ee1-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10ee1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10ee1-150">-WhatIf</span></span>
<span data-ttu-id="10ee1-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10ee1-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10ee1-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10ee1-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10ee1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ee1-153">CommonParameters</span></span>
<span data-ttu-id="10ee1-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10ee1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ee1-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10ee1-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ee1-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10ee1-156">INPUTS</span></span>

## <span data-ttu-id="10ee1-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10ee1-157">OUTPUTS</span></span>

## <span data-ttu-id="10ee1-158">Note</span><span class="sxs-lookup"><span data-stu-id="10ee1-158">NOTES</span></span>

## <span data-ttu-id="10ee1-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10ee1-159">RELATED LINKS</span></span>

[<span data-ttu-id="10ee1-160">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="10ee1-160">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="10ee1-161">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="10ee1-161">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="10ee1-162">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10ee1-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="10ee1-163">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="10ee1-163">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
