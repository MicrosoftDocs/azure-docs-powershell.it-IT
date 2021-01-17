---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: ba8131ba496d51ba5597995e24f873fe2e186435
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474631"
---
# <span data-ttu-id="53dd7-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="53dd7-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="53dd7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="53dd7-103">Inizia a copiare un BLOB.</span><span class="sxs-lookup"><span data-stu-id="53dd7-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="53dd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53dd7-104">SYNTAX</span></span>

### <span data-ttu-id="53dd7-105">ContainerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="53dd7-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53dd7-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="53dd7-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53dd7-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="53dd7-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53dd7-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="53dd7-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53dd7-109">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="53dd7-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53dd7-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="53dd7-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53dd7-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="53dd7-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53dd7-112">Istanza di fileinstance</span><span class="sxs-lookup"><span data-stu-id="53dd7-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53dd7-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="53dd7-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53dd7-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="53dd7-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53dd7-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53dd7-115">DESCRIPTION</span></span>
<span data-ttu-id="53dd7-116">Il cmdlet **Start-AzStorageBlobCopy** inizia a copiare un BLOB.</span><span class="sxs-lookup"><span data-stu-id="53dd7-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="53dd7-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53dd7-117">EXAMPLES</span></span>

### <span data-ttu-id="53dd7-118">Esempio 1: copiare un BLOB denominato</span><span class="sxs-lookup"><span data-stu-id="53dd7-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="53dd7-119">Questo comando avvia l'operazione di copia del BLOB denominato ContosoPlanning2015 dal contenitore denominato ContosoUploads al contenitore denominato ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="53dd7-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="53dd7-120">Esempio 2: ottenere un contenitore per specificare i BLOB da copiare</span><span class="sxs-lookup"><span data-stu-id="53dd7-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="53dd7-121">Questo comando ottiene il contenitore denominato ContosoUploads usando il cmdlet **Get-AzStorageContainer** e quindi passa il contenitore al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="53dd7-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="53dd7-122">Questo cmdlet avvia l'operazione di copia del BLOB denominato ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="53dd7-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="53dd7-123">Il cmdlet Previous fornisce il contenitore di origine.</span><span class="sxs-lookup"><span data-stu-id="53dd7-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="53dd7-124">Il parametro *DestContainer* specifica ContosoArchives come contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="53dd7-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="53dd7-125">Esempio 3: ottenere tutti i BLOB in un contenitore e copiarli</span><span class="sxs-lookup"><span data-stu-id="53dd7-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="53dd7-126">Questo comando ottiene i BLOB nel contenitore denominato ContosoUploads, usando il cmdlet **Get-AzStorageBlob** e quindi passa i risultati al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="53dd7-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="53dd7-127">Questo cmdlet avvia l'operazione di copia degli oggetti BLOB nel contenitore denominato ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="53dd7-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="53dd7-128">Esempio 4: copiare un blob specificato come oggetto</span><span class="sxs-lookup"><span data-stu-id="53dd7-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="53dd7-129">Il primo comando ottiene il BLOB denominato ContosoPlanning2015 nel contenitore denominato ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="53dd7-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="53dd7-130">Il comando Archivia l'oggetto nella variabile $SrcBlob.</span><span class="sxs-lookup"><span data-stu-id="53dd7-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="53dd7-131">Il secondo comando ottiene il BLOB denominato ContosoPlanning2015Archived nel contenitore denominato ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="53dd7-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="53dd7-132">Il comando Archivia l'oggetto nella variabile $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="53dd7-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="53dd7-133">L'ultimo comando avvia l'operazione di copia dal contenitore di origine al contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="53dd7-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="53dd7-134">Il comando usa la notazione standard del punto per specificare gli oggetti **ICloudBlob** per la $SrcBlob e $DestBlob BLOB.</span><span class="sxs-lookup"><span data-stu-id="53dd7-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="53dd7-135">Esempio 5: copiare un BLOB da un URI</span><span class="sxs-lookup"><span data-stu-id="53dd7-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="53dd7-136">Questo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata e quindi archivia tale chiave nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="53dd7-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="53dd7-137">Il secondo comando copia il file dall'URI specificato al BLOB denominato ContosoPlanning nel contenitore denominato ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="53dd7-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="53dd7-138">Il comando avvia l'operazione di copia nel contesto di destinazione archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="53dd7-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="53dd7-139">Non esistono contesto di archiviazione di origine, quindi l'URI di origine deve avere accesso all'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="53dd7-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="53dd7-140">Ad esempio: se l'origine è un BLOB pubblico nessuno, l'URI deve contenere il token SAS che ha accesso in lettura al BLOB.</span><span class="sxs-lookup"><span data-stu-id="53dd7-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="53dd7-141">Esempio 6: copiare un BLOB di blocco nel contenitore di destinazione con un nuovo nome BLOB e impostare BLOB di destinazione StandardBlobTier come caldo, RehydratePriority come alto</span><span class="sxs-lookup"><span data-stu-id="53dd7-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="53dd7-142">Questo comando avvia l'operazione di copia di un BLOB di blocco nel contenitore di destinazione con un nuovo nome BLOB e imposta BLOB di destinazione StandardBlobTier come caldo, RehydratePriority come alto</span><span class="sxs-lookup"><span data-stu-id="53dd7-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="53dd7-143">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53dd7-143">PARAMETERS</span></span>

### <span data-ttu-id="53dd7-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="53dd7-144">-AbsoluteUri</span></span>
<span data-ttu-id="53dd7-145">Specifica l'URI assoluto di un file da copiare in un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="53dd7-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="53dd7-146">-BlobBaseClient</span></span>
<span data-ttu-id="53dd7-147">Oggetto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="53dd7-147">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="53dd7-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="53dd7-149">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="53dd7-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="53dd7-150">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="53dd7-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="53dd7-151">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="53dd7-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="53dd7-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="53dd7-152">-CloudBlob</span></span>
<span data-ttu-id="53dd7-153">Specifica un oggetto **CloudBlob** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="53dd7-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="53dd7-154">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="53dd7-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="53dd7-155">-CloudBlobContainer</span></span>
<span data-ttu-id="53dd7-156">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="53dd7-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="53dd7-157">Questo cmdlet copia un BLOB dal contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="53dd7-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="53dd7-158">Per ottenere un oggetto **CloudBlobContainer** , usa il cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="53dd7-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="53dd7-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="53dd7-160">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="53dd7-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="53dd7-161">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="53dd7-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="53dd7-162">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="53dd7-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="53dd7-163">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="53dd7-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="53dd7-164">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="53dd7-164">The default value is 10.</span></span>

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

### <span data-ttu-id="53dd7-165">-Contesto</span><span class="sxs-lookup"><span data-stu-id="53dd7-165">-Context</span></span>
<span data-ttu-id="53dd7-166">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="53dd7-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="53dd7-167">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="53dd7-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53dd7-168">-DefaultProfile</span></span>
<span data-ttu-id="53dd7-169">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53dd7-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53dd7-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="53dd7-170">-DestBlob</span></span>
<span data-ttu-id="53dd7-171">Specifica il nome del BLOB di destinazione.</span><span class="sxs-lookup"><span data-stu-id="53dd7-171">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="53dd7-172">-DestCloudBlob</span></span>
<span data-ttu-id="53dd7-173">Specifica un oggetto **CloudBlob** di destinazione</span><span class="sxs-lookup"><span data-stu-id="53dd7-173">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="53dd7-174">-DestContainer</span></span>
<span data-ttu-id="53dd7-175">Specifica il nome del contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="53dd7-175">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-176">-DestContext</span><span class="sxs-lookup"><span data-stu-id="53dd7-176">-DestContext</span></span>
<span data-ttu-id="53dd7-177">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="53dd7-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="53dd7-178">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="53dd7-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-179">-Force</span><span class="sxs-lookup"><span data-stu-id="53dd7-179">-Force</span></span>
<span data-ttu-id="53dd7-180">Indica che questo cmdlet sovrascrive il BLOB di destinazione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="53dd7-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="53dd7-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="53dd7-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="53dd7-182">Livello di BLOB di pagine Premium</span><span class="sxs-lookup"><span data-stu-id="53dd7-182">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-183">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="53dd7-183">-RehydratePriority</span></span>
<span data-ttu-id="53dd7-184">Bloccare i BLOB RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="53dd7-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="53dd7-185">Indica la priorità con cui reidratare un BLOB archiviato.</span><span class="sxs-lookup"><span data-stu-id="53dd7-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="53dd7-186">I valori validi sono high/standard.</span><span class="sxs-lookup"><span data-stu-id="53dd7-186">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="53dd7-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="53dd7-188">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="53dd7-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="53dd7-189">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="53dd7-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="53dd7-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="53dd7-190">-SrcBlob</span></span>
<span data-ttu-id="53dd7-191">Specifica il nome del BLOB di origine.</span><span class="sxs-lookup"><span data-stu-id="53dd7-191">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="53dd7-192">-SrcContainer</span></span>
<span data-ttu-id="53dd7-193">Specifica il nome del contenitore di origine.</span><span class="sxs-lookup"><span data-stu-id="53dd7-193">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="53dd7-194">-SrcDir</span></span>
<span data-ttu-id="53dd7-195">Specifica un oggetto **CloudFileDirectory** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="53dd7-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="53dd7-196">-SrcFile</span></span>
<span data-ttu-id="53dd7-197">Specifica un oggetto **CloudFile** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="53dd7-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="53dd7-198">Puoi crearlo o usare Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53dd7-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="53dd7-199">-SrcFilePath</span></span>
<span data-ttu-id="53dd7-200">Specifica il percorso relativo del file di origine della directory di origine o della condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="53dd7-200">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="53dd7-201">-SrcShare</span></span>
<span data-ttu-id="53dd7-202">Specifica un oggetto **CloudFileShare** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="53dd7-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="53dd7-203">Puoi crearlo o usare Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53dd7-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="53dd7-204">-SrcShareName</span></span>
<span data-ttu-id="53dd7-205">Specifica il nome della condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="53dd7-205">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="53dd7-206">-StandardBlobTier</span></span>
<span data-ttu-id="53dd7-207">Blocca livello BLOB i valori validi sono hot/cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="53dd7-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="53dd7-208">Vedere dettagli in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="53dd7-208">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dd7-209">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53dd7-209">-Confirm</span></span>
<span data-ttu-id="53dd7-210">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53dd7-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53dd7-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53dd7-211">-WhatIf</span></span>
<span data-ttu-id="53dd7-212">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53dd7-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53dd7-213">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53dd7-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53dd7-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53dd7-214">CommonParameters</span></span>
<span data-ttu-id="53dd7-215">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53dd7-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53dd7-216">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53dd7-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53dd7-217">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53dd7-217">INPUTS</span></span>

### <span data-ttu-id="53dd7-218">Microsoft. Azure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="53dd7-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="53dd7-219">Microsoft. Azure. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="53dd7-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="53dd7-220">Microsoft. Azure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="53dd7-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="53dd7-221">System. String</span><span class="sxs-lookup"><span data-stu-id="53dd7-221">System.String</span></span>

### <span data-ttu-id="53dd7-222">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="53dd7-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="53dd7-223">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53dd7-223">OUTPUTS</span></span>

### <span data-ttu-id="53dd7-224">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="53dd7-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="53dd7-225">Note</span><span class="sxs-lookup"><span data-stu-id="53dd7-225">NOTES</span></span>

## <span data-ttu-id="53dd7-226">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53dd7-226">RELATED LINKS</span></span>

[<span data-ttu-id="53dd7-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="53dd7-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="53dd7-228">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="53dd7-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
