---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 772e97611d81362ffb3becea8875826110e822a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002222"
---
# <span data-ttu-id="9a5cf-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="9a5cf-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="9a5cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a5cf-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5cf-103">Avviare un'operazione di copia incrementale da uno snapshot BLOB delle pagine al BLOB delle pagine di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="9a5cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a5cf-104">SYNTAX</span></span>

### <span data-ttu-id="9a5cf-105">ContainerInstance (Default)</span><span class="sxs-lookup"><span data-stu-id="9a5cf-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a5cf-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="9a5cf-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a5cf-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="9a5cf-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a5cf-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="9a5cf-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a5cf-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="9a5cf-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a5cf-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9a5cf-110">DESCRIPTION</span></span>
<span data-ttu-id="9a5cf-111">Avviare un'operazione di copia incrementale da uno snapshot BLOB delle pagine al BLOB delle pagine di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="9a5cf-112">Vedere altri dettagli della funzionalità in https://docs.microsoft.com/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="9a5cf-112">See more details of the feature in https://docs.microsoft.com/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="9a5cf-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a5cf-113">EXAMPLES</span></span>

### <span data-ttu-id="9a5cf-114">Esempio 1: Avviare l'operazione di copia incrementale in base al nome blob e alla data e ora snapshot</span><span class="sxs-lookup"><span data-stu-id="9a5cf-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="9a5cf-115">Questo comando avvia l'operazione di copia incrementale in base al nome BLOB e alla data e ora snapshot</span><span class="sxs-lookup"><span data-stu-id="9a5cf-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="9a5cf-116">Esempio 2: Avviare l'operazione di copia incrementale con l'URI di origine</span><span class="sxs-lookup"><span data-stu-id="9a5cf-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="9a5cf-117">Questo comando avvia l'operazione di copia incrementale con l'URI di origine</span><span class="sxs-lookup"><span data-stu-id="9a5cf-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="9a5cf-118">Esempio 3: Avviare l'operazione di copia incrementale usando la pipeline del contenitore da GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9a5cf-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="9a5cf-119">Questo comando avvia l'operazione di copia incrementale usando la pipeline del contenitore da GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9a5cf-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="9a5cf-120">Esempio 4: avviare l'operazione di copia incrementale dall'oggetto CloudPageBlob al BLOB di destinazione con il nome BLOB</span><span class="sxs-lookup"><span data-stu-id="9a5cf-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="9a5cf-121">Questo comando avvia l'operazione di copia incrementale dall'oggetto CloudPageBlob al BLOB di destinazione con il nome BLOB</span><span class="sxs-lookup"><span data-stu-id="9a5cf-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="9a5cf-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a5cf-122">PARAMETERS</span></span>

### <span data-ttu-id="9a5cf-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="9a5cf-123">-AbsoluteUri</span></span>
<span data-ttu-id="9a5cf-124">Uri assoluto dell'origine.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-124">Absolute Uri to the source.</span></span> <span data-ttu-id="9a5cf-125">Si noti che le credenziali devono essere fornite nell'URI, se l'origine ne richiede una.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="9a5cf-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9a5cf-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9a5cf-127">Il tempo massimo di esecuzione sul lato client per ogni richiesta in secondi.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="9a5cf-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9a5cf-128">-CloudBlob</span></span>
<span data-ttu-id="9a5cf-129">Oggetto CloudBlob dalla libreria del client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="9a5cf-130">È possibile crearlo o usare Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a5cf-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9a5cf-131">-CloudBlobContainer</span></span>
<span data-ttu-id="9a5cf-132">Oggetto CloudBlobContainer dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="9a5cf-133">È possibile crearlo o usare Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="9a5cf-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9a5cf-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9a5cf-135">La quantità totale di attività sincronizzate simultanee.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="9a5cf-136">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-136">The default value is 10.</span></span>

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

### <span data-ttu-id="9a5cf-137">-Context</span><span class="sxs-lookup"><span data-stu-id="9a5cf-137">-Context</span></span>
<span data-ttu-id="9a5cf-138">Contesto di archiviazione di Azure di origine.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-138">Source Azure Storage Context.</span></span> <span data-ttu-id="9a5cf-139">È possibile crearla con New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-139">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
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

### <span data-ttu-id="9a5cf-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5cf-140">-DefaultProfile</span></span>
<span data-ttu-id="9a5cf-141">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a5cf-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="9a5cf-142">-DestBlob</span></span>
<span data-ttu-id="9a5cf-143">Nome BLOB di destinazione</span><span class="sxs-lookup"><span data-stu-id="9a5cf-143">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
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

### <span data-ttu-id="9a5cf-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="9a5cf-144">-DestCloudBlob</span></span>
<span data-ttu-id="9a5cf-145">Oggetto CloudBlob di destinazione</span><span class="sxs-lookup"><span data-stu-id="9a5cf-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5cf-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="9a5cf-146">-DestContainer</span></span>
<span data-ttu-id="9a5cf-147">Nome contenitore di destinazione</span><span class="sxs-lookup"><span data-stu-id="9a5cf-147">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5cf-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="9a5cf-148">-DestContext</span></span>
<span data-ttu-id="9a5cf-149">Contesto di archiviazione di Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="9a5cf-150">È possibile crearla con New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9a5cf-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9a5cf-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9a5cf-152">Timeout del server in ogni richiesta in secondi.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="9a5cf-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="9a5cf-153">-SrcBlob</span></span>
<span data-ttu-id="9a5cf-154">Nome BLOB pagina di origine.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-154">Source page blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5cf-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="9a5cf-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="9a5cf-156">Tempo di snapshot BLOB della pagina di origine.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-156">Source page blob snapshot time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5cf-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="9a5cf-157">-SrcContainer</span></span>
<span data-ttu-id="9a5cf-158">Nome contenitore di origine</span><span class="sxs-lookup"><span data-stu-id="9a5cf-158">Source Container name</span></span>

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

### <span data-ttu-id="9a5cf-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a5cf-159">-Confirm</span></span>
<span data-ttu-id="9a5cf-160">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a5cf-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a5cf-161">-WhatIf</span></span>
<span data-ttu-id="9a5cf-162">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a5cf-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a5cf-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5cf-164">CommonParameters</span></span>
<span data-ttu-id="9a5cf-165">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a5cf-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5cf-166">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a5cf-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5cf-167">INPUT</span><span class="sxs-lookup"><span data-stu-id="9a5cf-167">INPUTS</span></span>

### <span data-ttu-id="9a5cf-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="9a5cf-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="9a5cf-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9a5cf-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="9a5cf-170">System.String</span><span class="sxs-lookup"><span data-stu-id="9a5cf-170">System.String</span></span>

### <span data-ttu-id="9a5cf-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9a5cf-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9a5cf-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a5cf-172">OUTPUTS</span></span>

### <span data-ttu-id="9a5cf-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9a5cf-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="9a5cf-174">NOTE</span><span class="sxs-lookup"><span data-stu-id="9a5cf-174">NOTES</span></span>

## <span data-ttu-id="9a5cf-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a5cf-175">RELATED LINKS</span></span>
