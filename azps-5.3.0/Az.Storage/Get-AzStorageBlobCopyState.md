---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 319463dfb80cddbbffe5b7d1652a04f98e285768
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473664"
---
# <span data-ttu-id="93075-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="93075-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="93075-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93075-102">SYNOPSIS</span></span>
<span data-ttu-id="93075-103">Ottiene lo stato di copia di un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="93075-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="93075-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93075-104">SYNTAX</span></span>

### <span data-ttu-id="93075-105">NamePipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93075-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="93075-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="93075-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="93075-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="93075-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="93075-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93075-108">DESCRIPTION</span></span>
<span data-ttu-id="93075-109">Il cmdlet **Get-AzStorageBlobCopyState** ottiene lo stato di copia di un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="93075-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="93075-110">Dovrebbe essere eseguito nel BLOB di destinazione della copia.</span><span class="sxs-lookup"><span data-stu-id="93075-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="93075-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93075-111">EXAMPLES</span></span>

### <span data-ttu-id="93075-112">Esempio 1: ottenere lo stato di copia di un BLOB</span><span class="sxs-lookup"><span data-stu-id="93075-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="93075-113">Questo comando ottiene lo stato di copia del BLOB denominato ContosoPlanning2015 nel contenitore ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="93075-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="93075-114">Esempio 2: ottenere lo stato di copia di un BLOB usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="93075-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="93075-115">Questo comando ottiene il BLOB denominato ContosoPlanning2015 nel contenitore denominato ContosoUploads usando il cmdlet **Get-AzStorageBlob** e quindi passa il risultato al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="93075-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="93075-116">Il cmdlet **Get-AzStorageBlobCopyState** ottiene lo stato di copia per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="93075-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="93075-117">Esempio 3: ottenere lo stato di copia di un BLOB in un contenitore usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="93075-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="93075-118">Questo comando ottiene il contenitore denominato usando il cmdlet **Get-AzStorageBlob** e quindi passa il risultato al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="93075-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="93075-119">Il cmdlet **Get-AzStorageContainer** ottiene lo stato di copia per il BLOB denominato ContosoPlanning2015 in tale contenitore.</span><span class="sxs-lookup"><span data-stu-id="93075-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="93075-120">Esempio 4: avviare la copia e la pipeline per ottenere lo stato di copia</span><span class="sxs-lookup"><span data-stu-id="93075-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="93075-121">Il primo comando Avvia copia BLOB "ContosoPlanning2015" in "ContosoPlanning2015_copy", quindi emette l'oggetto BLOB destiantion.</span><span class="sxs-lookup"><span data-stu-id="93075-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="93075-122">Il secondo comando pipeline l'oggetto BLOB destiantion per Get-AzStorageBlobCopyState, per ottenere lo stato di copia BLOB.</span><span class="sxs-lookup"><span data-stu-id="93075-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="93075-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93075-123">PARAMETERS</span></span>

### <span data-ttu-id="93075-124">-BLOB</span><span class="sxs-lookup"><span data-stu-id="93075-124">-Blob</span></span>
<span data-ttu-id="93075-125">Specifica il nome di un BLOB.</span><span class="sxs-lookup"><span data-stu-id="93075-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="93075-126">Questo cmdlet ottiene lo stato dell'operazione di copia BLOB per il BLOB di archiviazione di Azure specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="93075-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93075-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="93075-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="93075-128">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="93075-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="93075-129">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="93075-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="93075-130">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="93075-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="93075-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="93075-131">-CloudBlob</span></span>
<span data-ttu-id="93075-132">Specifica un oggetto **CloudBlob** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="93075-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="93075-133">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="93075-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93075-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="93075-134">-CloudBlobContainer</span></span>
<span data-ttu-id="93075-135">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="93075-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="93075-136">Questo cmdlet ottiene lo stato di copia di un BLOB nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="93075-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="93075-137">Per ottenere un oggetto **CloudBlobContainer** , usa il cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="93075-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93075-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="93075-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="93075-139">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="93075-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="93075-140">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="93075-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="93075-141">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="93075-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="93075-142">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="93075-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="93075-143">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="93075-143">The default value is 10.</span></span>

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

### <span data-ttu-id="93075-144">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="93075-144">-Container</span></span>
<span data-ttu-id="93075-145">Specifica il nome di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="93075-145">Specifies the name of a container.</span></span>
<span data-ttu-id="93075-146">Questo cmdlet ottiene lo stato di copia di un BLOB nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="93075-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93075-147">-Contesto</span><span class="sxs-lookup"><span data-stu-id="93075-147">-Context</span></span>
<span data-ttu-id="93075-148">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="93075-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="93075-149">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="93075-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="93075-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93075-150">-DefaultProfile</span></span>
<span data-ttu-id="93075-151">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93075-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93075-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="93075-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="93075-153">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="93075-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="93075-154">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="93075-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="93075-155">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="93075-155">-WaitForComplete</span></span>
<span data-ttu-id="93075-156">Indica che questo cmdlet attende che la copia finisca.</span><span class="sxs-lookup"><span data-stu-id="93075-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="93075-157">Se non specifichi questo parametro, questo cmdlet restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="93075-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="93075-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93075-158">CommonParameters</span></span>
<span data-ttu-id="93075-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93075-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93075-160">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93075-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93075-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93075-161">INPUTS</span></span>

### <span data-ttu-id="93075-162">Microsoft. Azure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="93075-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="93075-163">Microsoft. Azure. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="93075-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="93075-164">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="93075-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="93075-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93075-165">OUTPUTS</span></span>

### <span data-ttu-id="93075-166">Microsoft. Azure. storage. blob. CopyState</span><span class="sxs-lookup"><span data-stu-id="93075-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="93075-167">Note</span><span class="sxs-lookup"><span data-stu-id="93075-167">NOTES</span></span>

## <span data-ttu-id="93075-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93075-168">RELATED LINKS</span></span>

[<span data-ttu-id="93075-169">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="93075-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="93075-170">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="93075-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


