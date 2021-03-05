---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: 754ac7657561ba52e28f90d951c0843a8c206484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002237"
---
# <span data-ttu-id="e0e4d-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e0e4d-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="e0e4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e4d-103">Inizia a copiare un BLOB.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="e0e4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0e4d-104">SYNTAX</span></span>

### <span data-ttu-id="e0e4d-105">ContainerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0e4d-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0e4d-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="e0e4d-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0e4d-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="e0e4d-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0e4d-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e0e4d-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0e4d-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="e0e4d-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e4d-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="e0e4d-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e4d-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="e0e4d-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e4d-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="e0e4d-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e4d-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="e0e4d-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0e4d-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="e0e4d-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0e4d-115">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e0e4d-115">DESCRIPTION</span></span>
<span data-ttu-id="e0e4d-116">Il cmdlet **Start-AzStorageBlobCopy inizia** a copiare un BLOB.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="e0e4d-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0e4d-117">EXAMPLES</span></span>

### <span data-ttu-id="e0e4d-118">Esempio 1: Copiare un BLOB denominato</span><span class="sxs-lookup"><span data-stu-id="e0e4d-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="e0e4d-119">Questo comando avvia l'operazione di copia del BLOB denominato ContosoPlanning2015 dal contenitore ContosoUploads al contenitore contosoArchives.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="e0e4d-120">Esempio 2: Ottenere un contenitore per specificare i BLOB da copiare</span><span class="sxs-lookup"><span data-stu-id="e0e4d-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="e0e4d-121">Questo comando recupera il contenitore denominato ContosoUploads usando il cmdlet **Get-AzStorageContainer** e quindi passa il contenitore al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e0e4d-122">Questo cmdlet avvia l'operazione di copia del BLOB denominato ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="e0e4d-123">Il cmdlet precedente fornisce il contenitore di origine.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="e0e4d-124">Il *parametro DestContainer* specifica ContosoArchives come contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="e0e4d-125">Esempio 3: Recuperare tutti i BLOB in un contenitore e copiarli</span><span class="sxs-lookup"><span data-stu-id="e0e4d-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="e0e4d-126">Questo comando recupera i BLOB nel contenitore denominato ContosoUploads, usando il cmdlet **Get-AzStorageBlob,** quindi passa i risultati al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e0e4d-127">Questo cmdlet avvia l'operazione di copia dei BLOB nel contenitore denominato ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="e0e4d-128">Esempio 4: Copiare un BLOB specificato come oggetto</span><span class="sxs-lookup"><span data-stu-id="e0e4d-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="e0e4d-129">Il primo comando recupera il BLOB denominato ContosoPlanning2015 nel contenitore ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="e0e4d-130">Il comando archivia l'oggetto nella $SrcBlob variabile.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="e0e4d-131">Il secondo comando recupera il BLOB denominato ContosoPlanning2015Archived nel contenitore denominato ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="e0e4d-132">Il comando archivia l'oggetto nella $DestBlob variabile.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="e0e4d-133">L'ultimo comando avvia l'operazione di copia dal contenitore di origine al contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="e0e4d-134">Il comando usa la notazione punto standard per specificare gli oggetti **ICloudBlob** per $SrcBlob e $DestBlob BLOB.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="e0e4d-135">Esempio 5: Copiare un BLOB da un URI</span><span class="sxs-lookup"><span data-stu-id="e0e4d-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="e0e4d-136">Questo comando crea un contesto per l'account contosoGeneral che usa la chiave specificata e quindi archivia tale chiave nella $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="e0e4d-137">Il secondo comando copia il file dall'URI specificato al BLOB denominato ContosoPlanning nel contenitore denominato ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="e0e4d-138">Il comando avvia l'operazione di copia nel contesto di destinazione archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="e0e4d-139">Non esiste alcun contesto di archiviazione di origine, quindi l'URI di origine deve avere accesso all'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="e0e4d-140">Ad esempio, se l'origine è un BLOB di Azure non pubblico, l'URI deve contenere un token di firma di accesso condiviso che ha accesso in lettura al BLOB.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="e0e4d-141">Esempio 6: Copiare un BLOB di blocco nel contenitore di destinazione con un nuovo nome BLOB e impostare il BLOB di destinazione StandardBlobTier su Hot, RehydratePriority come High</span><span class="sxs-lookup"><span data-stu-id="e0e4d-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="e0e4d-142">Questo comando avvia l'operazione di copia di un BLOB di blocco nel contenitore di destinazione con un nuovo nome BLOB e imposta il BLOB di destinazione StandardBlobTier su Hot, RehydratePriority come High</span><span class="sxs-lookup"><span data-stu-id="e0e4d-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="e0e4d-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0e4d-143">PARAMETERS</span></span>

### <span data-ttu-id="e0e4d-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="e0e4d-144">-AbsoluteUri</span></span>
<span data-ttu-id="e0e4d-145">Specifica l'URI assoluto di un file da copiare in un BLOB di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="e0e4d-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="e0e4d-146">-BlobBaseClient</span></span>
<span data-ttu-id="e0e4d-147">Oggetto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="e0e4d-147">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="e0e4d-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e0e4d-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e0e4d-149">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e0e4d-150">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e0e4d-151">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e0e4d-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e0e4d-152">-CloudBlob</span></span>
<span data-ttu-id="e0e4d-153">Specifica un **oggetto CloudBlob** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="e0e4d-154">Per ottenere un **oggetto CloudBlob,** usare il cmdlet Get-AzStorageBlob CloudBlob.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="e0e4d-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="e0e4d-155">-CloudBlobContainer</span></span>
<span data-ttu-id="e0e4d-156">Specifica un **oggetto CloudBlobContainer** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="e0e4d-157">Questo cmdlet copia un BLOB dal contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="e0e4d-158">Per ottenere un **oggetto CloudBlobContainer,** usare il cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="e0e4d-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e0e4d-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e0e4d-160">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e0e4d-161">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e0e4d-162">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e0e4d-163">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e0e4d-164">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-164">The default value is 10.</span></span>

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

### <span data-ttu-id="e0e4d-165">-Context</span><span class="sxs-lookup"><span data-stu-id="e0e4d-165">-Context</span></span>
<span data-ttu-id="e0e4d-166">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e0e4d-167">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e0e4d-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0e4d-168">-DefaultProfile</span></span>
<span data-ttu-id="e0e4d-169">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0e4d-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="e0e4d-170">-DestBlob</span></span>
<span data-ttu-id="e0e4d-171">Specifica il nome del BLOB di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-171">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="e0e4d-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="e0e4d-172">-DestCloudBlob</span></span>
<span data-ttu-id="e0e4d-173">Specifica un oggetto **CloudBlob di** destinazione</span><span class="sxs-lookup"><span data-stu-id="e0e4d-173">Specifies a destination **CloudBlob** object</span></span>

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

### <span data-ttu-id="e0e4d-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="e0e4d-174">-DestContainer</span></span>
<span data-ttu-id="e0e4d-175">Specifica il nome del contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-175">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="e0e4d-176">-DestContext</span><span class="sxs-lookup"><span data-stu-id="e0e4d-176">-DestContext</span></span>
<span data-ttu-id="e0e4d-177">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e0e4d-178">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e0e4d-179">-Force</span><span class="sxs-lookup"><span data-stu-id="e0e4d-179">-Force</span></span>
<span data-ttu-id="e0e4d-180">Indica che questo cmdlet sovrascrive il BLOB di destinazione senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e0e4d-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="e0e4d-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="e0e4d-182">Livello BLOB pagina Premium</span><span class="sxs-lookup"><span data-stu-id="e0e4d-182">Premium Page Blob Tier</span></span>

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

### <span data-ttu-id="e0e4d-183">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="e0e4d-183">-RehydratePriority</span></span>
<span data-ttu-id="e0e4d-184">Bloccare BLOB RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="e0e4d-185">Indica la priorità con cui rehydrate un BLOB archiviato.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="e0e4d-186">I valori validi sono High/Standard.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-186">Valid values are High/Standard.</span></span>

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

### <span data-ttu-id="e0e4d-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e0e4d-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e0e4d-188">Specifica l'intervallo di timeout del lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="e0e4d-189">Se prima dell'elaborazione della richiesta da parte del servizio è trascorso l'intervallo specificato, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="e0e4d-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="e0e4d-190">-SrcBlob</span></span>
<span data-ttu-id="e0e4d-191">Specifica il nome del BLOB di origine.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-191">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="e0e4d-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="e0e4d-192">-SrcContainer</span></span>
<span data-ttu-id="e0e4d-193">Specifica il nome del contenitore di origine.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-193">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="e0e4d-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="e0e4d-194">-SrcDir</span></span>
<span data-ttu-id="e0e4d-195">Specifica un **oggetto CloudFileDirectory** dalla libreria del client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

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

### <span data-ttu-id="e0e4d-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="e0e4d-196">-SrcFile</span></span>
<span data-ttu-id="e0e4d-197">Specifica un **oggetto CloudFile** dalla libreria del client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="e0e4d-198">È possibile crearlo o usare Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="e0e4d-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="e0e4d-199">-SrcFilePath</span></span>
<span data-ttu-id="e0e4d-200">Specifica il percorso relativo del file di origine della directory di origine o della condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-200">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="e0e4d-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="e0e4d-201">-SrcShare</span></span>
<span data-ttu-id="e0e4d-202">Specifica un **oggetto CloudFileShare** dalla libreria del client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="e0e4d-203">È possibile crearlo o usare Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="e0e4d-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="e0e4d-204">-SrcShareName</span></span>
<span data-ttu-id="e0e4d-205">Specifica il nome della condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-205">Specifies the source share name.</span></span>

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

### <span data-ttu-id="e0e4d-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="e0e4d-206">-StandardBlobTier</span></span>
<span data-ttu-id="e0e4d-207">Livello BLOB block, i valori validi sono Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="e0e4d-208">Vedi i dettagli in https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="e0e4d-208">See detail in https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="e0e4d-209">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0e4d-209">-Confirm</span></span>
<span data-ttu-id="e0e4d-210">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0e4d-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0e4d-211">-WhatIf</span></span>
<span data-ttu-id="e0e4d-212">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0e4d-213">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0e4d-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e4d-214">CommonParameters</span></span>
<span data-ttu-id="e0e4d-215">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0e4d-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e4d-216">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0e4d-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e4d-217">INPUT</span><span class="sxs-lookup"><span data-stu-id="e0e4d-217">INPUTS</span></span>

### <span data-ttu-id="e0e4d-218">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e0e4d-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="e0e4d-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="e0e4d-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="e0e4d-220">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="e0e4d-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="e0e4d-221">System.String</span><span class="sxs-lookup"><span data-stu-id="e0e4d-221">System.String</span></span>

### <span data-ttu-id="e0e4d-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e0e4d-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e0e4d-223">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0e4d-223">OUTPUTS</span></span>

### <span data-ttu-id="e0e4d-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e0e4d-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="e0e4d-225">NOTE</span><span class="sxs-lookup"><span data-stu-id="e0e4d-225">NOTES</span></span>

## <span data-ttu-id="e0e4d-226">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0e4d-226">RELATED LINKS</span></span>

[<span data-ttu-id="e0e4d-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="e0e4d-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="e0e4d-228">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e0e4d-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
