---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202784"
---
# <span data-ttu-id="b5775-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b5775-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="b5775-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5775-102">SYNOPSIS</span></span>
<span data-ttu-id="b5775-103">Rimuove il BLOB di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="b5775-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="b5775-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5775-104">SYNTAX</span></span>

### <span data-ttu-id="b5775-105">NamePipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5775-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5775-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="b5775-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5775-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="b5775-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5775-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5775-108">DESCRIPTION</span></span>
<span data-ttu-id="b5775-109">Il cmdlet **Remove-AzStorageBlob** rimuove il blob specificato da un account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="b5775-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="b5775-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5775-110">EXAMPLES</span></span>

### <span data-ttu-id="b5775-111">Esempio 1: rimuovere un BLOB di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="b5775-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="b5775-112">Questo comando rimuove un BLOB identificato dal relativo nome.</span><span class="sxs-lookup"><span data-stu-id="b5775-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="b5775-113">Esempio 2: rimuovere un BLOB di archiviazione tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="b5775-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="b5775-114">Questo comando usa la pipeline.</span><span class="sxs-lookup"><span data-stu-id="b5775-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="b5775-115">Esempio 3: rimuovere i BLOB di archiviazione tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="b5775-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="b5775-116">Questo comando usa il carattere jolly asterisco (\*) e la pipeline per recuperare BLOB o BLOB e quindi rimuoverli.</span><span class="sxs-lookup"><span data-stu-id="b5775-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="b5775-117">Esempio 4: rimuovere una singola versione BLOB</span><span class="sxs-lookup"><span data-stu-id="b5775-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="b5775-118">Questo comando consente di rimuovere un singolo BLOB verion con VersionId.</span><span class="sxs-lookup"><span data-stu-id="b5775-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="b5775-119">Esempio 5: rimuovere un singolo snapshot BLOB</span><span class="sxs-lookup"><span data-stu-id="b5775-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="b5775-120">Questo comando rimuove un singolo snapshot BLOB con SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="b5775-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="b5775-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5775-121">PARAMETERS</span></span>

### <span data-ttu-id="b5775-122">-BLOB</span><span class="sxs-lookup"><span data-stu-id="b5775-122">-Blob</span></span>
<span data-ttu-id="b5775-123">Specifica il nome del BLOB che si vuole rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b5775-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="b5775-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="b5775-124">-BlobBaseClient</span></span>
<span data-ttu-id="b5775-125">Oggetto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="b5775-125">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5775-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b5775-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b5775-127">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="b5775-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b5775-128">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="b5775-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b5775-129">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="b5775-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b5775-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b5775-130">-CloudBlob</span></span>
<span data-ttu-id="b5775-131">Specifica un BLOB cloud.</span><span class="sxs-lookup"><span data-stu-id="b5775-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="b5775-132">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="b5775-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="b5775-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b5775-133">-CloudBlobContainer</span></span>
<span data-ttu-id="b5775-134">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5775-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="b5775-135">Puoi usare il cmdlet Get-AzStorageContainer per recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="b5775-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="b5775-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b5775-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b5775-137">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="b5775-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b5775-138">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="b5775-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b5775-139">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="b5775-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b5775-140">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="b5775-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b5775-141">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="b5775-141">The default value is 10.</span></span>

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

### <span data-ttu-id="b5775-142">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="b5775-142">-Container</span></span>
<span data-ttu-id="b5775-143">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="b5775-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="b5775-144">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b5775-144">-Context</span></span>
<span data-ttu-id="b5775-145">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5775-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b5775-146">Puoi usare il cmdlet New-AzStorageContext per crearlo.</span><span class="sxs-lookup"><span data-stu-id="b5775-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="b5775-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5775-147">-DefaultProfile</span></span>
<span data-ttu-id="b5775-148">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5775-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5775-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="b5775-149">-DeleteSnapshot</span></span>
<span data-ttu-id="b5775-150">Specifica che tutti gli snapshot verranno eliminati, ma non per i BLOB di base.</span><span class="sxs-lookup"><span data-stu-id="b5775-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="b5775-151">Se questo parametro non viene specificato, il BLOB di base e i relativi snapshot vengono eliminati insieme.</span><span class="sxs-lookup"><span data-stu-id="b5775-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="b5775-152">All'utente viene richiesto di confermare l'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="b5775-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="b5775-153">-Force</span><span class="sxs-lookup"><span data-stu-id="b5775-153">-Force</span></span>
<span data-ttu-id="b5775-154">Indica che questo cmdlet rimuove il BLOB e lo snapshot senza conferma.</span><span class="sxs-lookup"><span data-stu-id="b5775-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="b5775-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5775-155">-PassThru</span></span>
<span data-ttu-id="b5775-156">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b5775-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b5775-157">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b5775-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b5775-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b5775-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b5775-159">Specifica il profilo Azure per il cmdlet da leggere.</span><span class="sxs-lookup"><span data-stu-id="b5775-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="b5775-160">Se non specificato, il cmdlet legge il profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="b5775-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="b5775-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="b5775-161">-SnapshotTime</span></span>
<span data-ttu-id="b5775-162">BLOB SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="b5775-162">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5775-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="b5775-163">-VersionId</span></span>
<span data-ttu-id="b5775-164">BLOB VersionId</span><span class="sxs-lookup"><span data-stu-id="b5775-164">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5775-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b5775-165">-Confirm</span></span>
<span data-ttu-id="b5775-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5775-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5775-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5775-167">-WhatIf</span></span>
<span data-ttu-id="b5775-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5775-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5775-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5775-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5775-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5775-170">CommonParameters</span></span>
<span data-ttu-id="b5775-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5775-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5775-172">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5775-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5775-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5775-173">INPUTS</span></span>

### <span data-ttu-id="b5775-174">Microsoft. Azure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b5775-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="b5775-175">Microsoft. Azure. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b5775-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="b5775-176">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b5775-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b5775-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5775-177">OUTPUTS</span></span>

### <span data-ttu-id="b5775-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5775-178">System.Boolean</span></span>

## <span data-ttu-id="b5775-179">Note</span><span class="sxs-lookup"><span data-stu-id="b5775-179">NOTES</span></span>

## <span data-ttu-id="b5775-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5775-180">RELATED LINKS</span></span>

[<span data-ttu-id="b5775-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b5775-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="b5775-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b5775-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="b5775-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b5775-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
