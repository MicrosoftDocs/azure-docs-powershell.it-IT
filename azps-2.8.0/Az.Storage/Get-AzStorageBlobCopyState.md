---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 14a6a7932d82d240522d524604a8337e1804c72b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857902"
---
# <span data-ttu-id="77568-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="77568-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="77568-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77568-102">SYNOPSIS</span></span>
<span data-ttu-id="77568-103">Ottiene lo stato di copia di un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="77568-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="77568-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77568-104">SYNTAX</span></span>

### <span data-ttu-id="77568-105">NamePipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="77568-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="77568-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="77568-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="77568-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="77568-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="77568-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77568-108">DESCRIPTION</span></span>
<span data-ttu-id="77568-109">Il cmdlet **Get-AzStorageBlobCopyState** ottiene lo stato di copia di un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="77568-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="77568-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77568-110">EXAMPLES</span></span>

### <span data-ttu-id="77568-111">Esempio 1: ottenere lo stato di copia di un BLOB</span><span class="sxs-lookup"><span data-stu-id="77568-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="77568-112">Questo comando ottiene lo stato di copia del BLOB denominato ContosoPlanning2015 nel contenitore ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="77568-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="77568-113">Esempio 2: ottenere lo stato di copia di un BLOB usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="77568-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="77568-114">Questo comando ottiene il BLOB denominato ContosoPlanning2015 nel contenitore denominato ContosoUploads usando il cmdlet **Get-AzStorageBlob** e quindi passa il risultato al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="77568-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="77568-115">Il cmdlet **Get-AzStorageBlobCopyState** ottiene lo stato di copia per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="77568-115">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="77568-116">Esempio 3: ottenere lo stato di copia di un BLOB in un contenitore usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="77568-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="77568-117">Questo comando ottiene il contenitore denominato usando il cmdlet **Get-AzStorageBlob** e quindi passa il risultato al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="77568-117">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="77568-118">Il cmdlet **Get-AzStorageContainer** ottiene lo stato di copia per il BLOB denominato ContosoPlanning2015 in tale contenitore.</span><span class="sxs-lookup"><span data-stu-id="77568-118">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="77568-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77568-119">PARAMETERS</span></span>

### <span data-ttu-id="77568-120">-BLOB</span><span class="sxs-lookup"><span data-stu-id="77568-120">-Blob</span></span>
<span data-ttu-id="77568-121">Specifica il nome di un BLOB.</span><span class="sxs-lookup"><span data-stu-id="77568-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="77568-122">Questo cmdlet ottiene lo stato dell'operazione di copia BLOB per il BLOB di archiviazione di Azure specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="77568-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="77568-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="77568-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="77568-124">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="77568-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="77568-125">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="77568-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="77568-126">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="77568-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="77568-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="77568-127">-CloudBlob</span></span>
<span data-ttu-id="77568-128">Specifica un oggetto **CloudBlob** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="77568-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="77568-129">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="77568-129">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="77568-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="77568-130">-CloudBlobContainer</span></span>
<span data-ttu-id="77568-131">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="77568-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="77568-132">Questo cmdlet ottiene lo stato di copia di un BLOB nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="77568-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="77568-133">Per ottenere un oggetto **CloudBlobContainer** , usa il cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="77568-133">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="77568-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="77568-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="77568-135">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="77568-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="77568-136">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="77568-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="77568-137">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="77568-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="77568-138">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="77568-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="77568-139">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="77568-139">The default value is 10.</span></span>

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

### <span data-ttu-id="77568-140">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="77568-140">-Container</span></span>
<span data-ttu-id="77568-141">Specifica il nome di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="77568-141">Specifies the name of a container.</span></span>
<span data-ttu-id="77568-142">Questo cmdlet ottiene lo stato di copia di un BLOB nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="77568-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="77568-143">-Contesto</span><span class="sxs-lookup"><span data-stu-id="77568-143">-Context</span></span>
<span data-ttu-id="77568-144">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="77568-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="77568-145">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="77568-145">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="77568-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77568-146">-DefaultProfile</span></span>
<span data-ttu-id="77568-147">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77568-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77568-148">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="77568-148">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="77568-149">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="77568-149">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="77568-150">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="77568-150">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="77568-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="77568-151">-WaitForComplete</span></span>
<span data-ttu-id="77568-152">Indica che questo cmdlet attende che la copia finisca.</span><span class="sxs-lookup"><span data-stu-id="77568-152">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="77568-153">Se non specifichi questo parametro, questo cmdlet restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="77568-153">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="77568-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77568-154">CommonParameters</span></span>
<span data-ttu-id="77568-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77568-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77568-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77568-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77568-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77568-157">INPUTS</span></span>

### <span data-ttu-id="77568-158">Microsoft. Azure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="77568-158">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="77568-159">Microsoft. Azure. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="77568-159">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="77568-160">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="77568-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="77568-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77568-161">OUTPUTS</span></span>

### <span data-ttu-id="77568-162">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="77568-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="77568-163">Note</span><span class="sxs-lookup"><span data-stu-id="77568-163">NOTES</span></span>

## <span data-ttu-id="77568-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77568-164">RELATED LINKS</span></span>

[<span data-ttu-id="77568-165">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="77568-165">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="77568-166">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="77568-166">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


