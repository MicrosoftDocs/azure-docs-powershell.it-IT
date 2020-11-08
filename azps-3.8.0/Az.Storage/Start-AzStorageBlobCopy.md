---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: 36ae8a00237be287262de0cc9eac4022b9efc9d5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019462"
---
# <span data-ttu-id="80997-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="80997-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="80997-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80997-102">SYNOPSIS</span></span>
<span data-ttu-id="80997-103">Inizia a copiare un BLOB.</span><span class="sxs-lookup"><span data-stu-id="80997-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="80997-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80997-104">SYNTAX</span></span>

### <span data-ttu-id="80997-105">ContainerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80997-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80997-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="80997-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80997-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="80997-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80997-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="80997-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80997-109">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="80997-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80997-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="80997-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80997-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="80997-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80997-112">Istanza di fileinstance</span><span class="sxs-lookup"><span data-stu-id="80997-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80997-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="80997-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80997-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="80997-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80997-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80997-115">DESCRIPTION</span></span>
<span data-ttu-id="80997-116">Il cmdlet **Start-AzStorageBlobCopy** inizia a copiare un BLOB.</span><span class="sxs-lookup"><span data-stu-id="80997-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="80997-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80997-117">EXAMPLES</span></span>

### <span data-ttu-id="80997-118">Esempio 1: copiare un BLOB denominato</span><span class="sxs-lookup"><span data-stu-id="80997-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="80997-119">Questo comando avvia l'operazione di copia del BLOB denominato ContosoPlanning2015 dal contenitore denominato ContosoUploads al contenitore denominato ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="80997-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="80997-120">Esempio 2: ottenere un contenitore per specificare i BLOB da copiare</span><span class="sxs-lookup"><span data-stu-id="80997-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="80997-121">Questo comando ottiene il contenitore denominato ContosoUploads usando il cmdlet **Get-AzStorageContainer** e quindi passa il contenitore al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="80997-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="80997-122">Questo cmdlet avvia l'operazione di copia del BLOB denominato ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="80997-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="80997-123">Il cmdlet Previous fornisce il contenitore di origine.</span><span class="sxs-lookup"><span data-stu-id="80997-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="80997-124">Il parametro *DestContainer* specifica ContosoArchives come contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80997-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="80997-125">Esempio 3: ottenere tutti i BLOB in un contenitore e copiarli</span><span class="sxs-lookup"><span data-stu-id="80997-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="80997-126">Questo comando ottiene i BLOB nel contenitore denominato ContosoUploads, usando il cmdlet **Get-AzStorageBlob** e quindi passa i risultati al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="80997-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="80997-127">Questo cmdlet avvia l'operazione di copia degli oggetti BLOB nel contenitore denominato ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="80997-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="80997-128">Esempio 4: copiare un blob specificato come oggetto</span><span class="sxs-lookup"><span data-stu-id="80997-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="80997-129">Il primo comando ottiene il BLOB denominato ContosoPlanning2015 nel contenitore denominato ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="80997-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="80997-130">Il comando Archivia l'oggetto nella variabile $SrcBlob.</span><span class="sxs-lookup"><span data-stu-id="80997-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="80997-131">Il secondo comando ottiene il BLOB denominato ContosoPlanning2015Archived nel contenitore denominato ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="80997-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="80997-132">Il comando Archivia l'oggetto nella variabile $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="80997-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="80997-133">L'ultimo comando avvia l'operazione di copia dal contenitore di origine al contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80997-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="80997-134">Il comando usa la notazione standard del punto per specificare gli oggetti **ICloudBlob** per la $SrcBlob e $DestBlob BLOB.</span><span class="sxs-lookup"><span data-stu-id="80997-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="80997-135">Esempio 5: copiare un BLOB da un URI</span><span class="sxs-lookup"><span data-stu-id="80997-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="80997-136">Questo comando crea un contesto per l'account denominato ContosoGeneral che usa la chiave specificata e quindi archivia tale chiave nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="80997-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="80997-137">Il secondo comando copia il file dall'URI specificato al BLOB denominato ContosoPlanning nel contenitore denominato ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="80997-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="80997-138">Il comando avvia l'operazione di copia nel contesto archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="80997-138">The command starts the copy operation in the context stored in $Context.</span></span>

### <span data-ttu-id="80997-139">Esempio 6: copiare un BLOB di blocco nel contenitore di destinazione con un nuovo nome BLOB e impostare BLOB di destinazione StandardBlobTier come caldo, RehydratePriority come alto</span><span class="sxs-lookup"><span data-stu-id="80997-139">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="80997-140">Questo comando avvia l'operazione di copia di un BLOB di blocco nel contenitore di destinazione con un nuovo nome BLOB e imposta BLOB di destinazione StandardBlobTier come caldo, RehydratePriority come alto</span><span class="sxs-lookup"><span data-stu-id="80997-140">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="80997-141">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80997-141">PARAMETERS</span></span>

### <span data-ttu-id="80997-142">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="80997-142">-AbsoluteUri</span></span>
<span data-ttu-id="80997-143">Specifica l'URI assoluto di un file da copiare in un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="80997-143">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="80997-144">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="80997-144">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="80997-145">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="80997-145">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="80997-146">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="80997-146">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="80997-147">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="80997-147">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="80997-148">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="80997-148">-CloudBlob</span></span>
<span data-ttu-id="80997-149">Specifica un oggetto **CloudBlob** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="80997-149">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="80997-150">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="80997-150">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="80997-151">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="80997-151">-CloudBlobContainer</span></span>
<span data-ttu-id="80997-152">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="80997-152">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="80997-153">Questo cmdlet copia un BLOB dal contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="80997-153">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="80997-154">Per ottenere un oggetto **CloudBlobContainer** , usa il cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="80997-154">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="80997-155">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="80997-155">-ConcurrentTaskCount</span></span>
<span data-ttu-id="80997-156">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="80997-156">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="80997-157">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="80997-157">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="80997-158">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="80997-158">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="80997-159">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="80997-159">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="80997-160">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="80997-160">The default value is 10.</span></span>

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

### <span data-ttu-id="80997-161">-Contesto</span><span class="sxs-lookup"><span data-stu-id="80997-161">-Context</span></span>
<span data-ttu-id="80997-162">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="80997-162">Specifies an Azure storage context.</span></span>
<span data-ttu-id="80997-163">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="80997-163">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="80997-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80997-164">-DefaultProfile</span></span>
<span data-ttu-id="80997-165">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80997-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80997-166">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="80997-166">-DestBlob</span></span>
<span data-ttu-id="80997-167">Specifica il nome del BLOB di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80997-167">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="80997-168">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="80997-168">-DestCloudBlob</span></span>
<span data-ttu-id="80997-169">Specifica un oggetto **CloudBlob** di destinazione</span><span class="sxs-lookup"><span data-stu-id="80997-169">Specifies a destination **CloudBlob** object</span></span>

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

### <span data-ttu-id="80997-170">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="80997-170">-DestContainer</span></span>
<span data-ttu-id="80997-171">Specifica il nome del contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80997-171">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="80997-172">-DestContext</span><span class="sxs-lookup"><span data-stu-id="80997-172">-DestContext</span></span>
<span data-ttu-id="80997-173">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="80997-173">Specifies an Azure storage context.</span></span>
<span data-ttu-id="80997-174">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="80997-174">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="80997-175">-Force</span><span class="sxs-lookup"><span data-stu-id="80997-175">-Force</span></span>
<span data-ttu-id="80997-176">Indica che questo cmdlet sovrascrive il BLOB di destinazione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="80997-176">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="80997-177">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="80997-177">-PremiumPageBlobTier</span></span>
<span data-ttu-id="80997-178">Livello di BLOB di pagine Premium</span><span class="sxs-lookup"><span data-stu-id="80997-178">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80997-179">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="80997-179">-RehydratePriority</span></span>
<span data-ttu-id="80997-180">Bloccare i BLOB RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="80997-180">Block Blob RehydratePriority.</span></span> <span data-ttu-id="80997-181">Indica la priorità con cui reidratare un BLOB archiviato.</span><span class="sxs-lookup"><span data-stu-id="80997-181">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="80997-182">I valori validi sono high/standard.</span><span class="sxs-lookup"><span data-stu-id="80997-182">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80997-183">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="80997-183">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="80997-184">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="80997-184">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="80997-185">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="80997-185">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="80997-186">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="80997-186">-SrcBlob</span></span>
<span data-ttu-id="80997-187">Specifica il nome del BLOB di origine.</span><span class="sxs-lookup"><span data-stu-id="80997-187">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="80997-188">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="80997-188">-SrcContainer</span></span>
<span data-ttu-id="80997-189">Specifica il nome del contenitore di origine.</span><span class="sxs-lookup"><span data-stu-id="80997-189">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="80997-190">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="80997-190">-SrcDir</span></span>
<span data-ttu-id="80997-191">Specifica un oggetto **CloudFileDirectory** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="80997-191">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

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

### <span data-ttu-id="80997-192">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="80997-192">-SrcFile</span></span>
<span data-ttu-id="80997-193">Specifica un oggetto **CloudFile** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="80997-193">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="80997-194">Puoi crearlo o usare Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80997-194">You can create it or use Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="80997-195">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="80997-195">-SrcFilePath</span></span>
<span data-ttu-id="80997-196">Specifica il percorso relativo del file di origine della directory di origine o della condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="80997-196">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="80997-197">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="80997-197">-SrcShare</span></span>
<span data-ttu-id="80997-198">Specifica un oggetto **CloudFileShare** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="80997-198">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="80997-199">Puoi crearlo o usare Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80997-199">You can create it or use Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="80997-200">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="80997-200">-SrcShareName</span></span>
<span data-ttu-id="80997-201">Specifica il nome della condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="80997-201">Specifies the source share name.</span></span>

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

### <span data-ttu-id="80997-202">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="80997-202">-StandardBlobTier</span></span>
<span data-ttu-id="80997-203">Blocca livello BLOB i valori validi sono hot/cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="80997-203">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="80997-204">Vedere dettagli in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="80997-204">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80997-205">-Confermare</span><span class="sxs-lookup"><span data-stu-id="80997-205">-Confirm</span></span>
<span data-ttu-id="80997-206">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80997-206">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80997-207">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80997-207">-WhatIf</span></span>
<span data-ttu-id="80997-208">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80997-208">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80997-209">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80997-209">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80997-210">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80997-210">CommonParameters</span></span>
<span data-ttu-id="80997-211">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80997-211">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80997-212">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80997-212">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80997-213">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80997-213">INPUTS</span></span>

### <span data-ttu-id="80997-214">Microsoft. Azure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="80997-214">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="80997-215">Microsoft. Azure. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="80997-215">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="80997-216">Microsoft. Azure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="80997-216">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="80997-217">System. String</span><span class="sxs-lookup"><span data-stu-id="80997-217">System.String</span></span>

### <span data-ttu-id="80997-218">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="80997-218">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="80997-219">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80997-219">OUTPUTS</span></span>

### <span data-ttu-id="80997-220">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="80997-220">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="80997-221">Note</span><span class="sxs-lookup"><span data-stu-id="80997-221">NOTES</span></span>

## <span data-ttu-id="80997-222">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80997-222">RELATED LINKS</span></span>

[<span data-ttu-id="80997-223">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="80997-223">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="80997-224">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="80997-224">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
