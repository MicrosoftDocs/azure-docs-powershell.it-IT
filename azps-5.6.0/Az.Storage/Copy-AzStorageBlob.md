---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/copy-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
ms.openlocfilehash: 76e89c90da10e8e232a564fb5fb7e5f8cc807327
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988761"
---
# <span data-ttu-id="753b5-101">Copy-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="753b5-101">Copy-AzStorageBlob</span></span>

## <span data-ttu-id="753b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="753b5-102">SYNOPSIS</span></span>
<span data-ttu-id="753b5-103">Copiare un BLOB in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="753b5-103">Copy a blob synchronously.</span></span>

## <span data-ttu-id="753b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="753b5-104">SYNTAX</span></span>

### <span data-ttu-id="753b5-105">ContainerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="753b5-105">ContainerName (Default)</span></span>
```
Copy-AzStorageBlob [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="753b5-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="753b5-106">BlobInstance</span></span>
```
Copy-AzStorageBlob [-BlobBaseClient <BlobBaseClient>] -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="753b5-107">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="753b5-107">UriPipeline</span></span>
```
Copy-AzStorageBlob -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="753b5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="753b5-108">DESCRIPTION</span></span>
<span data-ttu-id="753b5-109">Il cmdlet **Copy-AzStorageBlob** copia un BLOB in modo sincrono, attualmente supporta solo blob di blocco.</span><span class="sxs-lookup"><span data-stu-id="753b5-109">The **Copy-AzStorageBlob** cmdlet copies a blob synchronously, currently only support block blob.</span></span>

## <span data-ttu-id="753b5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="753b5-110">EXAMPLES</span></span>

### <span data-ttu-id="753b5-111">Esempio 1: Copiare un BLOB denominato in un altro</span><span class="sxs-lookup"><span data-stu-id="753b5-111">Example 1: Copy a named blob to another</span></span>
```
C:\PS> $destBlob = Copy-AzStorageBlob -SrcContainer "sourcecontainername" -SrcBlob "srcblobname" -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="753b5-112">Questo comando copia un BLOB dal contenitore di origine al contenitore di destinazione con un nuovo nome DI BLOB.</span><span class="sxs-lookup"><span data-stu-id="753b5-112">This command copies a blob from source container to the destination container with a new blob name.</span></span> 

### <span data-ttu-id="753b5-113">Esempio 2: Copiare BLOB da un oggetto BLOB</span><span class="sxs-lookup"><span data-stu-id="753b5-113">Example 2: Copy blob from a blob object</span></span>
```
C:\PS> $srcBlob = Get-AzStorageBlob -Container $containerName -Blob $blobName  -Context $ctx 
C:\PS> $destBlob =  $srcBlob | Copy-AzStorageBlob  -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="753b5-114">Questo comando copia un BLOB dall'oggetto BLOB di origine al contenitore di destinazione con un nuovo nome DI BLOB.</span><span class="sxs-lookup"><span data-stu-id="753b5-114">This command copies a blob from source blob object to the destination container with a new blob name.</span></span>

### <span data-ttu-id="753b5-115">Esempio 3: Copiare BLOB da un URI BLOB</span><span class="sxs-lookup"><span data-stu-id="753b5-115">Example 3: Copy blob from a blob Uri</span></span>
```
C:\PS> $srcBlobUri = New-AzStorageBlobSASToken -Container $srcContainerName -Blob $srcBlobName -Permission rt -ExpiryTime (Get-Date).AddDays(7) -FullUri 
C:\PS> $destBlob = Copy-AzStorageBlob -AbsoluteUri $srcBlobUri -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="753b5-116">Il primo comando crea un URI BLOB del BLOB di origine, con il token sas dell'autorizzazione "rt".</span><span class="sxs-lookup"><span data-stu-id="753b5-116">The first command creates a blob Uri of the source blob, with sas token of permission "rt".</span></span> <span data-ttu-id="753b5-117">Il secondo comando copia l'URI del BLOB di origine nel BLOB di destinazione.</span><span class="sxs-lookup"><span data-stu-id="753b5-117">The second command copies from source blob Uri to the destination blob.</span></span>

### <span data-ttu-id="753b5-118">Esempio 4: Aggiornare un ambito di crittografia BLOB di blocco</span><span class="sxs-lookup"><span data-stu-id="753b5-118">Example 4: Update a block blob encryption scope</span></span>
```
C:\PS> $blob = Copy-AzStorageBlob -SrcContainer $containerName -SrcBlob $blobname -DestContainer $containername -EncryptionScope $newScopeName -Force
```

<span data-ttu-id="753b5-119">Questo comando aggiorna un ambito di crittografia BLOB di blocco copiarlo in se stesso con un nuovo ambito di crittografia.</span><span class="sxs-lookup"><span data-stu-id="753b5-119">This command update a block blob encryption scope by copy it to itself with a new encryption scope.</span></span>

## <span data-ttu-id="753b5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="753b5-120">PARAMETERS</span></span>

### <span data-ttu-id="753b5-121">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="753b5-121">-AbsoluteUri</span></span>
<span data-ttu-id="753b5-122">URI BLOB di origine</span><span class="sxs-lookup"><span data-stu-id="753b5-122">Source blob uri</span></span>

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

### <span data-ttu-id="753b5-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="753b5-123">-AsJob</span></span>
<span data-ttu-id="753b5-124">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="753b5-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="753b5-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="753b5-125">-BlobBaseClient</span></span>
<span data-ttu-id="753b5-126">Oggetto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="753b5-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="753b5-127">-Context</span><span class="sxs-lookup"><span data-stu-id="753b5-127">-Context</span></span>
<span data-ttu-id="753b5-128">Oggetto contesto di archiviazione di Azure di origine</span><span class="sxs-lookup"><span data-stu-id="753b5-128">Source Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance
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

### <span data-ttu-id="753b5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="753b5-129">-DefaultProfile</span></span>
<span data-ttu-id="753b5-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="753b5-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="753b5-131">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="753b5-131">-DestBlob</span></span>
<span data-ttu-id="753b5-132">Nome BLOB di destinazione</span><span class="sxs-lookup"><span data-stu-id="753b5-132">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance
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

### <span data-ttu-id="753b5-133">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="753b5-133">-DestContainer</span></span>
<span data-ttu-id="753b5-134">Nome contenitore di destinazione</span><span class="sxs-lookup"><span data-stu-id="753b5-134">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="753b5-135">-DestContext</span><span class="sxs-lookup"><span data-stu-id="753b5-135">-DestContext</span></span>
<span data-ttu-id="753b5-136">Oggetto contesto Archiviazione di destinazione</span><span class="sxs-lookup"><span data-stu-id="753b5-136">Destination Storage context object</span></span>

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

### <span data-ttu-id="753b5-137">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="753b5-137">-EncryptionScope</span></span>
<span data-ttu-id="753b5-138">Ambito di crittografia da usare quando si effettuano richieste al BLOB più recente.</span><span class="sxs-lookup"><span data-stu-id="753b5-138">Encryption scope to be used when making requests to the dest blob.</span></span>

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

### <span data-ttu-id="753b5-139">-Force</span><span class="sxs-lookup"><span data-stu-id="753b5-139">-Force</span></span>
<span data-ttu-id="753b5-140">Forzare la sovrascrittura del BLOB o del file esistente</span><span class="sxs-lookup"><span data-stu-id="753b5-140">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="753b5-141">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="753b5-141">-RehydratePriority</span></span>
<span data-ttu-id="753b5-142">Bloccare BLOB RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="753b5-142">Block Blob RehydratePriority.</span></span>
<span data-ttu-id="753b5-143">Indica la priorità con cui rehydrate un BLOB archiviato.</span><span class="sxs-lookup"><span data-stu-id="753b5-143">Indicates the priority with which to rehydrate an archived blob.</span></span>
<span data-ttu-id="753b5-144">I valori validi sono High/Standard.</span><span class="sxs-lookup"><span data-stu-id="753b5-144">Valid values are High/Standard.</span></span>

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

### <span data-ttu-id="753b5-145">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="753b5-145">-SrcBlob</span></span>
<span data-ttu-id="753b5-146">Nome BLOB</span><span class="sxs-lookup"><span data-stu-id="753b5-146">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="753b5-147">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="753b5-147">-SrcContainer</span></span>
<span data-ttu-id="753b5-148">Nome contenitore di origine</span><span class="sxs-lookup"><span data-stu-id="753b5-148">Source Container name</span></span>

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

### <span data-ttu-id="753b5-149">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="753b5-149">-StandardBlobTier</span></span>
<span data-ttu-id="753b5-150">Livello BLOB block, i valori validi sono Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="753b5-150">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="753b5-151">Vedi i dettagli in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="753b5-151">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="753b5-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="753b5-152">-Confirm</span></span>
<span data-ttu-id="753b5-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="753b5-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="753b5-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="753b5-154">-WhatIf</span></span>
<span data-ttu-id="753b5-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="753b5-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="753b5-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="753b5-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="753b5-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="753b5-157">CommonParameters</span></span>
<span data-ttu-id="753b5-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="753b5-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="753b5-159">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="753b5-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="753b5-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="753b5-160">INPUTS</span></span>

### <span data-ttu-id="753b5-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="753b5-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="753b5-162">System.String</span><span class="sxs-lookup"><span data-stu-id="753b5-162">System.String</span></span>

### <span data-ttu-id="753b5-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="753b5-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="753b5-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="753b5-164">OUTPUTS</span></span>

### <span data-ttu-id="753b5-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="753b5-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="753b5-166">NOTE</span><span class="sxs-lookup"><span data-stu-id="753b5-166">NOTES</span></span>

## <span data-ttu-id="753b5-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="753b5-167">RELATED LINKS</span></span>
