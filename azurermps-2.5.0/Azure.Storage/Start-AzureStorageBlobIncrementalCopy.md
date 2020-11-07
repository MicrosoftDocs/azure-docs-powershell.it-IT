---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestorageblobincrementalcopy
schema: 2.0.0
ms.openlocfilehash: 3007dadcdca2494a3f0412fbb4caead3421d2bf9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867159"
---
# <span data-ttu-id="91e4f-101">Start-AzureStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="91e4f-101">Start-AzureStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="91e4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="91e4f-103">Avviare un'operazione di copia incrementale da uno snapshot BLOB della pagina nel BLOB della pagina di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="91e4f-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91e4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91e4f-104">SYNTAX</span></span>

### <span data-ttu-id="91e4f-105">ContainerInstance (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="91e4f-105">ContainerInstance (Default)</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91e4f-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="91e4f-106">BlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91e4f-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="91e4f-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91e4f-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="91e4f-108">ContainerName</span></span>
```
Start-AzureStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91e4f-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="91e4f-109">UriPipeline</span></span>
```
Start-AzureStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91e4f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91e4f-110">DESCRIPTION</span></span>
<span data-ttu-id="91e4f-111">Avviare un'operazione di copia incrementale da uno snapshot BLOB della pagina nel BLOB della pagina di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="91e4f-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="91e4f-112">Vedere altri dettagli della funzionalità https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="91e4f-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="91e4f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91e4f-113">EXAMPLES</span></span>

### <span data-ttu-id="91e4f-114">Esempio 1: avviare l'operazione di copia incrementale per nome BLOB e tempo istantaneo</span><span class="sxs-lookup"><span data-stu-id="91e4f-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="91e4f-115">Questo comando avvia l'operazione di copia incrementale per nome BLOB e tempo istantaneo</span><span class="sxs-lookup"><span data-stu-id="91e4f-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="91e4f-116">Esempio 2: avviare l'operazione di copia incrementale usando l'URI di origine</span><span class="sxs-lookup"><span data-stu-id="91e4f-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="91e4f-117">Questo comando avvia l'operazione di copia incrementale usando l'URI di origine</span><span class="sxs-lookup"><span data-stu-id="91e4f-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="91e4f-118">Esempio 3: avviare l'operazione di copia incrementale usando pipeline di contenitori da GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="91e4f-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container1 | Start-AzureStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="91e4f-119">Questo comando avvia l'operazione di copia incrementale usando pipeline di contenitori da GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="91e4f-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="91e4f-120">Esempio 4: avviare l'operazione di copia incrementale dall'oggetto CloudPageBlob al BLOB di destinazione con il nome BLOB</span><span class="sxs-lookup"><span data-stu-id="91e4f-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzureStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzureStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="91e4f-121">Questo comando avvia l'operazione di copia incrementale dall'oggetto CloudPageBlob al BLOB di destinazione con il nome BLOB</span><span class="sxs-lookup"><span data-stu-id="91e4f-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="91e4f-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91e4f-122">PARAMETERS</span></span>

### <span data-ttu-id="91e4f-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="91e4f-123">-AbsoluteUri</span></span>
<span data-ttu-id="91e4f-124">URI assoluto per l'origine.</span><span class="sxs-lookup"><span data-stu-id="91e4f-124">Absolute Uri to the source.</span></span> <span data-ttu-id="91e4f-125">Notare che le credenziali devono essere fornite nell'URI, se l'origine ne richiede.</span><span class="sxs-lookup"><span data-stu-id="91e4f-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="91e4f-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="91e4f-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="91e4f-127">Il tempo di esecuzione massimo lato client per ogni richiesta in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="91e4f-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="91e4f-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="91e4f-128">-CloudBlob</span></span>
<span data-ttu-id="91e4f-129">Oggetto CloudBlob dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="91e4f-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="91e4f-130">Puoi crearlo o usare Get-AzureStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91e4f-130">You can create it or use Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="91e4f-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="91e4f-131">-CloudBlobContainer</span></span>
<span data-ttu-id="91e4f-132">Oggetto CloudBlobContainer dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="91e4f-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="91e4f-133">Puoi crearlo o usare Get-AzureStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91e4f-133">You can create it or use Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="91e4f-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="91e4f-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="91e4f-135">La quantità totale di attività asincrone simultanee.</span><span class="sxs-lookup"><span data-stu-id="91e4f-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="91e4f-136">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="91e4f-136">The default value is 10.</span></span>

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

### <span data-ttu-id="91e4f-137">-Contesto</span><span class="sxs-lookup"><span data-stu-id="91e4f-137">-Context</span></span>
<span data-ttu-id="91e4f-138">Contesto di archiviazione di Azure di origine.</span><span class="sxs-lookup"><span data-stu-id="91e4f-138">Source Azure Storage Context.</span></span> <span data-ttu-id="91e4f-139">Puoi crearla tramite il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="91e4f-139">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="91e4f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e4f-140">-DefaultProfile</span></span>
<span data-ttu-id="91e4f-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91e4f-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91e4f-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="91e4f-142">-DestBlob</span></span>
<span data-ttu-id="91e4f-143">Nome BLOB di destinazione</span><span class="sxs-lookup"><span data-stu-id="91e4f-143">Destination blob name</span></span>

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

### <span data-ttu-id="91e4f-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="91e4f-144">-DestCloudBlob</span></span>
<span data-ttu-id="91e4f-145">Oggetto CloudBlob di destinazione</span><span class="sxs-lookup"><span data-stu-id="91e4f-145">Destination CloudBlob object</span></span>

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

### <span data-ttu-id="91e4f-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="91e4f-146">-DestContainer</span></span>
<span data-ttu-id="91e4f-147">Nome contenitore di destinazione</span><span class="sxs-lookup"><span data-stu-id="91e4f-147">Destination container name</span></span>

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

### <span data-ttu-id="91e4f-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="91e4f-148">-DestContext</span></span>
<span data-ttu-id="91e4f-149">Contesto di archiviazione di Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="91e4f-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="91e4f-150">Puoi crearla tramite il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="91e4f-150">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="91e4f-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="91e4f-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="91e4f-152">Timeout del server per ogni richiesta in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="91e4f-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="91e4f-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="91e4f-153">-SrcBlob</span></span>
<span data-ttu-id="91e4f-154">Nome BLOB della pagina di origine.</span><span class="sxs-lookup"><span data-stu-id="91e4f-154">Source page blob name.</span></span>

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

### <span data-ttu-id="91e4f-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="91e4f-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="91e4f-156">Tempo di snapshot BLOB della pagina di origine.</span><span class="sxs-lookup"><span data-stu-id="91e4f-156">Source page blob snapshot time.</span></span>

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

### <span data-ttu-id="91e4f-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="91e4f-157">-SrcContainer</span></span>
<span data-ttu-id="91e4f-158">Nome del contenitore di origine</span><span class="sxs-lookup"><span data-stu-id="91e4f-158">Source Container name</span></span>

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

### <span data-ttu-id="91e4f-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91e4f-159">-Confirm</span></span>
<span data-ttu-id="91e4f-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91e4f-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91e4f-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91e4f-161">-WhatIf</span></span>
<span data-ttu-id="91e4f-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91e4f-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91e4f-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91e4f-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91e4f-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e4f-164">CommonParameters</span></span>
<span data-ttu-id="91e4f-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e4f-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e4f-166">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91e4f-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e4f-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91e4f-167">INPUTS</span></span>

### <span data-ttu-id="91e4f-168">Microsoft. WindowsAzure. storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="91e4f-168">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="91e4f-169">Microsoft. WindowsAzure. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="91e4f-169">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="91e4f-170">System. String</span><span class="sxs-lookup"><span data-stu-id="91e4f-170">System.String</span></span>

### <span data-ttu-id="91e4f-171">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="91e4f-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="91e4f-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91e4f-172">OUTPUTS</span></span>

### <span data-ttu-id="91e4f-173">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="91e4f-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="91e4f-174">Note</span><span class="sxs-lookup"><span data-stu-id="91e4f-174">NOTES</span></span>

## <span data-ttu-id="91e4f-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91e4f-175">RELATED LINKS</span></span>
