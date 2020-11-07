---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: caaa36aa27cfb008fbbecced78f1fefc04958f4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676480"
---
# <span data-ttu-id="58347-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="58347-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="58347-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58347-102">SYNOPSIS</span></span>
<span data-ttu-id="58347-103">Avviare un'operazione di copia incrementale da uno snapshot BLOB della pagina nel BLOB della pagina di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="58347-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="58347-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58347-104">SYNTAX</span></span>

### <span data-ttu-id="58347-105">ContainerInstance (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58347-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58347-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="58347-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58347-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="58347-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58347-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="58347-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58347-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="58347-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58347-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58347-110">DESCRIPTION</span></span>
<span data-ttu-id="58347-111">Avviare un'operazione di copia incrementale da uno snapshot BLOB della pagina nel BLOB della pagina di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="58347-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="58347-112">Vedere altri dettagli della funzionalità https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="58347-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="58347-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58347-113">EXAMPLES</span></span>

### <span data-ttu-id="58347-114">Esempio 1: avviare l'operazione di copia incrementale per nome BLOB e tempo istantaneo</span><span class="sxs-lookup"><span data-stu-id="58347-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="58347-115">Questo comando avvia l'operazione di copia incrementale per nome BLOB e tempo istantaneo</span><span class="sxs-lookup"><span data-stu-id="58347-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="58347-116">Esempio 2: avviare l'operazione di copia incrementale usando l'URI di origine</span><span class="sxs-lookup"><span data-stu-id="58347-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="58347-117">Questo comando avvia l'operazione di copia incrementale usando l'URI di origine</span><span class="sxs-lookup"><span data-stu-id="58347-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="58347-118">Esempio 3: avviare l'operazione di copia incrementale usando pipeline di contenitori da GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="58347-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="58347-119">Questo comando avvia l'operazione di copia incrementale usando pipeline di contenitori da GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="58347-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="58347-120">Esempio 4: avviare l'operazione di copia incrementale dall'oggetto CloudPageBlob al BLOB di destinazione con il nome BLOB</span><span class="sxs-lookup"><span data-stu-id="58347-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="58347-121">Questo comando avvia l'operazione di copia incrementale dall'oggetto CloudPageBlob al BLOB di destinazione con il nome BLOB</span><span class="sxs-lookup"><span data-stu-id="58347-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="58347-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58347-122">PARAMETERS</span></span>

### <span data-ttu-id="58347-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="58347-123">-AbsoluteUri</span></span>
<span data-ttu-id="58347-124">URI assoluto per l'origine.</span><span class="sxs-lookup"><span data-stu-id="58347-124">Absolute Uri to the source.</span></span> <span data-ttu-id="58347-125">Notare che le credenziali devono essere fornite nell'URI, se l'origine ne richiede.</span><span class="sxs-lookup"><span data-stu-id="58347-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="58347-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="58347-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="58347-127">Il tempo di esecuzione massimo lato client per ogni richiesta in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="58347-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="58347-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="58347-128">-CloudBlob</span></span>
<span data-ttu-id="58347-129">Oggetto CloudBlob dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="58347-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="58347-130">Puoi crearlo o usare Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58347-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58347-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="58347-131">-CloudBlobContainer</span></span>
<span data-ttu-id="58347-132">Oggetto CloudBlobContainer dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="58347-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="58347-133">Puoi crearlo o usare Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58347-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58347-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="58347-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="58347-135">La quantità totale di attività asincrone simultanee.</span><span class="sxs-lookup"><span data-stu-id="58347-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="58347-136">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="58347-136">The default value is 10.</span></span>

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

### <span data-ttu-id="58347-137">-Contesto</span><span class="sxs-lookup"><span data-stu-id="58347-137">-Context</span></span>
<span data-ttu-id="58347-138">Contesto di archiviazione di Azure di origine.</span><span class="sxs-lookup"><span data-stu-id="58347-138">Source Azure Storage Context.</span></span> <span data-ttu-id="58347-139">Puoi crearla tramite il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="58347-139">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="58347-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58347-140">-DefaultProfile</span></span>
<span data-ttu-id="58347-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58347-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58347-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="58347-142">-DestBlob</span></span>
<span data-ttu-id="58347-143">Nome BLOB di destinazione</span><span class="sxs-lookup"><span data-stu-id="58347-143">Destination blob name</span></span>

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

### <span data-ttu-id="58347-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="58347-144">-DestCloudBlob</span></span>
<span data-ttu-id="58347-145">Oggetto CloudBlob di destinazione</span><span class="sxs-lookup"><span data-stu-id="58347-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58347-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="58347-146">-DestContainer</span></span>
<span data-ttu-id="58347-147">Nome contenitore di destinazione</span><span class="sxs-lookup"><span data-stu-id="58347-147">Destination container name</span></span>

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

### <span data-ttu-id="58347-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="58347-148">-DestContext</span></span>
<span data-ttu-id="58347-149">Contesto di archiviazione di Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="58347-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="58347-150">Puoi crearla tramite il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="58347-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="58347-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="58347-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="58347-152">Timeout del server per ogni richiesta in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="58347-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="58347-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="58347-153">-SrcBlob</span></span>
<span data-ttu-id="58347-154">Nome BLOB della pagina di origine.</span><span class="sxs-lookup"><span data-stu-id="58347-154">Source page blob name.</span></span>

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

### <span data-ttu-id="58347-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="58347-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="58347-156">Tempo di snapshot BLOB della pagina di origine.</span><span class="sxs-lookup"><span data-stu-id="58347-156">Source page blob snapshot time.</span></span>

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

### <span data-ttu-id="58347-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="58347-157">-SrcContainer</span></span>
<span data-ttu-id="58347-158">Nome del contenitore di origine</span><span class="sxs-lookup"><span data-stu-id="58347-158">Source Container name</span></span>

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

### <span data-ttu-id="58347-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="58347-159">-Confirm</span></span>
<span data-ttu-id="58347-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58347-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58347-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58347-161">-WhatIf</span></span>
<span data-ttu-id="58347-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58347-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58347-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58347-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58347-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58347-164">CommonParameters</span></span>
<span data-ttu-id="58347-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58347-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58347-166">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58347-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58347-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58347-167">INPUTS</span></span>

### <span data-ttu-id="58347-168">Microsoft. WindowsAzure. storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="58347-168">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="58347-169">Microsoft. WindowsAzure. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="58347-169">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="58347-170">System. String</span><span class="sxs-lookup"><span data-stu-id="58347-170">System.String</span></span>

### <span data-ttu-id="58347-171">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="58347-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="58347-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58347-172">OUTPUTS</span></span>

### <span data-ttu-id="58347-173">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="58347-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="58347-174">Note</span><span class="sxs-lookup"><span data-stu-id="58347-174">NOTES</span></span>

## <span data-ttu-id="58347-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58347-175">RELATED LINKS</span></span>