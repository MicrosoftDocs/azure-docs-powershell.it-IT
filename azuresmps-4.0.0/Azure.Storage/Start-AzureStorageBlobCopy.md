---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 01edb18c72487ada7c51408ce38502b6e87b2f56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685272"
---
# <span data-ttu-id="7b94d-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7b94d-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="7b94d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b94d-102">SYNOPSIS</span></span>
<span data-ttu-id="7b94d-103">Inizia a copiare un BLOB.</span><span class="sxs-lookup"><span data-stu-id="7b94d-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="7b94d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b94d-104">SYNTAX</span></span>

### <span data-ttu-id="7b94d-105">ContainerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b94d-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94d-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="7b94d-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94d-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="7b94d-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94d-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7b94d-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94d-109">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="7b94d-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94d-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="7b94d-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94d-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="7b94d-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94d-112">Istanza di fileinstance</span><span class="sxs-lookup"><span data-stu-id="7b94d-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94d-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="7b94d-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94d-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="7b94d-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b94d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b94d-115">DESCRIPTION</span></span>
<span data-ttu-id="7b94d-116">Il cmdlet **Start-AzureStorageBlobCopy** inizia a copiare un BLOB.</span><span class="sxs-lookup"><span data-stu-id="7b94d-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="7b94d-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b94d-117">EXAMPLES</span></span>

### <span data-ttu-id="7b94d-118">Esempio 1: copiare un BLOB denominato</span><span class="sxs-lookup"><span data-stu-id="7b94d-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="7b94d-119">Questo comando avvia l'operazione di copia del BLOB denominato ContosoPlanning2015 dal contenitore denominato ContosoUploads al contenitore denominato ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="7b94d-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="7b94d-120">Esempio 2: ottenere un contenitore per specificare i BLOB da copiare</span><span class="sxs-lookup"><span data-stu-id="7b94d-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="7b94d-121">Questo comando ottiene il contenitore denominato ContosoUploads usando il cmdlet **Get-AzureStorageContainer** e quindi passa il contenitore al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="7b94d-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7b94d-122">Questo cmdlet avvia l'operazione di copia del BLOB denominato ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="7b94d-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="7b94d-123">Il cmdlet Previous fornisce il contenitore di origine.</span><span class="sxs-lookup"><span data-stu-id="7b94d-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="7b94d-124">Il parametro *DestContainer* specifica ContosoArchives come contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b94d-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="7b94d-125">Esempio 3: ottenere un BLOB da copiare</span><span class="sxs-lookup"><span data-stu-id="7b94d-125">Example 3: Get a blob to copy</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="7b94d-126">Questo comando ottiene i BLOB nel contenitore denominato ContosoUploads, usando il cmdlet **Get-AzureStorageBlob** e quindi passa i risultati al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="7b94d-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7b94d-127">Questo cmdlet avvia l'operazione di copia degli oggetti BLOB nel contenitore denominato ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="7b94d-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="7b94d-128">Esempio 4: copiare un blob specificato come oggetto</span><span class="sxs-lookup"><span data-stu-id="7b94d-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="7b94d-129">Il primo comando ottiene il BLOB denominato ContosoPlanning2015 nel contenitore denominato ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="7b94d-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="7b94d-130">Il comando Archivia l'oggetto nella variabile $SrcBlob.</span><span class="sxs-lookup"><span data-stu-id="7b94d-130">The command stores that object in the $SrcBlob variable.</span></span>

<span data-ttu-id="7b94d-131">Il secondo comando ottiene il BLOB denominato ContosoPlanning2015Archived nel contenitore denominato ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="7b94d-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="7b94d-132">Il comando Archivia l'oggetto nella variabile $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="7b94d-132">The command stores that object in the $DestBlob variable.</span></span>

<span data-ttu-id="7b94d-133">L'ultimo comando avvia l'operazione di copia dal contenitore di origine al contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b94d-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="7b94d-134">Il comando usa la notazione standard del punto per specificare gli oggetti **ICloudBlob** per la $SrcBlob e $DestBlob BLOB.</span><span class="sxs-lookup"><span data-stu-id="7b94d-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="7b94d-135">Esempio 5: copiare un BLOB da un URI</span><span class="sxs-lookup"><span data-stu-id="7b94d-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="7b94d-136">Questo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata e quindi archivia tale chiave nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="7b94d-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>

<span data-ttu-id="7b94d-137">Il secondo comando copia il file dall'URI specificato al BLOB denominato ContosoPlanning nel contenitore denominato ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="7b94d-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="7b94d-138">Il comando avvia l'operazione di copia nel contesto archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="7b94d-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="7b94d-139">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b94d-139">PARAMETERS</span></span>

### <span data-ttu-id="7b94d-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="7b94d-140">-AbsoluteUri</span></span>
<span data-ttu-id="7b94d-141">Specifica l'URI assoluto di un file da copiare in un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b94d-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7b94d-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7b94d-143">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="7b94d-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7b94d-144">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="7b94d-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7b94d-145">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="7b94d-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7b94d-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="7b94d-146">-CloudBlob</span></span>
<span data-ttu-id="7b94d-147">Specifica un oggetto **CloudBlob** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b94d-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="7b94d-148">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="7b94d-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="7b94d-149">-CloudBlobContainer</span></span>
<span data-ttu-id="7b94d-150">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b94d-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="7b94d-151">Questo cmdlet copia un BLOB dal contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7b94d-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="7b94d-152">Per ottenere un oggetto **CloudBlobContainer** , usa il cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="7b94d-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7b94d-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7b94d-154">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="7b94d-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7b94d-155">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="7b94d-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7b94d-156">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="7b94d-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7b94d-157">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="7b94d-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7b94d-158">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="7b94d-158">The default value is 10.</span></span>

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

### <span data-ttu-id="7b94d-159">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7b94d-159">-Context</span></span>
<span data-ttu-id="7b94d-160">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b94d-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7b94d-161">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7b94d-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-162">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="7b94d-162">-DestBlob</span></span>
<span data-ttu-id="7b94d-163">Specifica il nome del BLOB di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b94d-163">Specifies the name of the destination blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-164">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="7b94d-164">-DestCloudBlob</span></span>
<span data-ttu-id="7b94d-165">Specifica un oggetto **CloudBlob** di destinazione</span><span class="sxs-lookup"><span data-stu-id="7b94d-165">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-166">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="7b94d-166">-DestContainer</span></span>
<span data-ttu-id="7b94d-167">Specifica il nome del contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b94d-167">Specifies the name of the destination container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-168">-DestContext</span><span class="sxs-lookup"><span data-stu-id="7b94d-168">-DestContext</span></span>
<span data-ttu-id="7b94d-169">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b94d-169">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7b94d-170">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7b94d-170">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-171">-Force</span><span class="sxs-lookup"><span data-stu-id="7b94d-171">-Force</span></span>
<span data-ttu-id="7b94d-172">Indica che questo cmdlet sovrascrive il BLOB di destinazione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7b94d-172">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7b94d-173">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7b94d-173">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7b94d-174">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="7b94d-174">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7b94d-175">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="7b94d-175">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="7b94d-176">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="7b94d-176">-SrcBlob</span></span>
<span data-ttu-id="7b94d-177">Specifica il nome del BLOB di origine.</span><span class="sxs-lookup"><span data-stu-id="7b94d-177">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-178">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="7b94d-178">-SrcContainer</span></span>
<span data-ttu-id="7b94d-179">Specifica il nome del contenitore di origine.</span><span class="sxs-lookup"><span data-stu-id="7b94d-179">Specifies the name of the source container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-180">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="7b94d-180">-SrcDir</span></span>
<span data-ttu-id="7b94d-181">Specifica un oggetto **CloudFileDirectory** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b94d-181">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-182">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="7b94d-182">-SrcFile</span></span>
<span data-ttu-id="7b94d-183">Specifica un oggetto **CloudFile** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b94d-183">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="7b94d-184">Puoi crearlo o usare Get-AzureStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b94d-184">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-185">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="7b94d-185">-SrcFilePath</span></span>
<span data-ttu-id="7b94d-186">Specifica il percorso relativo del file di origine della directory di origine o della condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="7b94d-186">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-187">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="7b94d-187">-SrcShare</span></span>
<span data-ttu-id="7b94d-188">Specifica un oggetto **CloudFileShare** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b94d-188">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="7b94d-189">Puoi crearlo o usare Get-AzureStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b94d-189">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-190">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="7b94d-190">-SrcShareName</span></span>
<span data-ttu-id="7b94d-191">Specifica il nome della condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="7b94d-191">Specifies the source share name.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b94d-192">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b94d-192">-Confirm</span></span>
<span data-ttu-id="7b94d-193">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b94d-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b94d-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b94d-194">-WhatIf</span></span>
<span data-ttu-id="7b94d-195">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b94d-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b94d-196">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b94d-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b94d-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b94d-197">CommonParameters</span></span>
<span data-ttu-id="7b94d-198">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b94d-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b94d-199">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b94d-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b94d-200">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b94d-200">INPUTS</span></span>

## <span data-ttu-id="7b94d-201">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b94d-201">OUTPUTS</span></span>

## <span data-ttu-id="7b94d-202">Note</span><span class="sxs-lookup"><span data-stu-id="7b94d-202">NOTES</span></span>

## <span data-ttu-id="7b94d-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b94d-203">RELATED LINKS</span></span>

[<span data-ttu-id="7b94d-204">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="7b94d-204">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="7b94d-205">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7b94d-205">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)
