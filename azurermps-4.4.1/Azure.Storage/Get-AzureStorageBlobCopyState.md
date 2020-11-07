---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 6a61e076bf91d1ed994f9745d18a6f4832925250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686884"
---
# <span data-ttu-id="84b2d-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="84b2d-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="84b2d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="84b2d-103">Ottiene lo stato di copia di un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="84b2d-103">Gets the copy status of an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84b2d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84b2d-104">SYNTAX</span></span>

### <span data-ttu-id="84b2d-105">NamePipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84b2d-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="84b2d-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="84b2d-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="84b2d-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="84b2d-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="84b2d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84b2d-108">DESCRIPTION</span></span>
<span data-ttu-id="84b2d-109">Il cmdlet **Get-AzureStorageBlobCopyState** ottiene lo stato di copia di un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="84b2d-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="84b2d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84b2d-110">EXAMPLES</span></span>

### <span data-ttu-id="84b2d-111">Esempio 1: ottenere lo stato di copia di un BLOB</span><span class="sxs-lookup"><span data-stu-id="84b2d-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="84b2d-112">Questo comando ottiene lo stato di copia del BLOB denominato ContosoPlanning2015 nel contenitore ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="84b2d-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="84b2d-113">Esempio 2: ottenere lo stato di copia di un BLOB usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="84b2d-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="84b2d-114">Questo comando ottiene il BLOB denominato ContosoPlanning2015 nel contenitore denominato ContosoUploads usando il cmdlet **Get-AzureStorageBlob** e quindi passa il risultato al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="84b2d-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="84b2d-115">Il cmdlet **Get-AzureStorageBlobCopyState** ottiene lo stato di copia per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="84b2d-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="84b2d-116">Esempio 3: ottenere lo stato di copia di un BLOB in un contenitore usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="84b2d-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="84b2d-117">Questo comando ottiene il contenitore denominato usando il cmdlet **Get-AzureStorageBlob** e quindi passa il risultato al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="84b2d-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="84b2d-118">Il cmdlet **Get-AzureStorageContainer** ottiene lo stato di copia per il BLOB denominato ContosoPlanning2015 in tale contenitore.</span><span class="sxs-lookup"><span data-stu-id="84b2d-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="84b2d-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84b2d-119">PARAMETERS</span></span>

### <span data-ttu-id="84b2d-120">-BLOB</span><span class="sxs-lookup"><span data-stu-id="84b2d-120">-Blob</span></span>
<span data-ttu-id="84b2d-121">Specifica il nome di un BLOB.</span><span class="sxs-lookup"><span data-stu-id="84b2d-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="84b2d-122">Questo cmdlet ottiene lo stato dell'operazione di copia BLOB per il BLOB di archiviazione di Azure specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="84b2d-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="84b2d-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="84b2d-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="84b2d-124">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="84b2d-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="84b2d-125">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="84b2d-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="84b2d-126">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="84b2d-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="84b2d-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="84b2d-127">-CloudBlob</span></span>
<span data-ttu-id="84b2d-128">Specifica un oggetto **CloudBlob** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="84b2d-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="84b2d-129">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="84b2d-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="84b2d-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="84b2d-130">-CloudBlobContainer</span></span>
<span data-ttu-id="84b2d-131">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="84b2d-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="84b2d-132">Questo cmdlet ottiene lo stato di copia di un BLOB nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="84b2d-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="84b2d-133">Per ottenere un oggetto **CloudBlobContainer** , usa il cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="84b2d-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="84b2d-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="84b2d-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="84b2d-135">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="84b2d-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="84b2d-136">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="84b2d-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="84b2d-137">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="84b2d-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="84b2d-138">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="84b2d-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="84b2d-139">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="84b2d-139">The default value is 10.</span></span>

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

### <span data-ttu-id="84b2d-140">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="84b2d-140">-Container</span></span>
<span data-ttu-id="84b2d-141">Specifica il nome di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="84b2d-141">Specifies the name of a container.</span></span>
<span data-ttu-id="84b2d-142">Questo cmdlet ottiene lo stato di copia di un BLOB nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="84b2d-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="84b2d-143">-Contesto</span><span class="sxs-lookup"><span data-stu-id="84b2d-143">-Context</span></span>
<span data-ttu-id="84b2d-144">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="84b2d-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="84b2d-145">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="84b2d-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="84b2d-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="84b2d-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="84b2d-147">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="84b2d-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="84b2d-148">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="84b2d-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="84b2d-149">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="84b2d-149">-WaitForComplete</span></span>
<span data-ttu-id="84b2d-150">Indica che questo cmdlet attende che la copia finisca.</span><span class="sxs-lookup"><span data-stu-id="84b2d-150">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="84b2d-151">Se non specifichi questo parametro, questo cmdlet restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="84b2d-151">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="84b2d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b2d-152">CommonParameters</span></span>
<span data-ttu-id="84b2d-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b2d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b2d-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b2d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b2d-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84b2d-155">INPUTS</span></span>

### <span data-ttu-id="84b2d-156">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="84b2d-156">IStorageContext</span></span>

<span data-ttu-id="84b2d-157">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="84b2d-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="84b2d-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84b2d-158">OUTPUTS</span></span>

### <span data-ttu-id="84b2d-159">CopyState</span><span class="sxs-lookup"><span data-stu-id="84b2d-159">CopyState</span></span>

## <span data-ttu-id="84b2d-160">Note</span><span class="sxs-lookup"><span data-stu-id="84b2d-160">NOTES</span></span>

## <span data-ttu-id="84b2d-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84b2d-161">RELATED LINKS</span></span>

[<span data-ttu-id="84b2d-162">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="84b2d-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="84b2d-163">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="84b2d-163">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)


