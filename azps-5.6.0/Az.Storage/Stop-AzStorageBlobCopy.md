---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 1be012a9a9c5a62cbd08451849f8d50e9a5d52a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960062"
---
# <span data-ttu-id="6662e-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6662e-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="6662e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6662e-102">SYNOPSIS</span></span>
<span data-ttu-id="6662e-103">Interrompe un'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="6662e-103">Stops a copy operation.</span></span>

## <span data-ttu-id="6662e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6662e-104">SYNTAX</span></span>

### <span data-ttu-id="6662e-105">NamePipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6662e-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6662e-106">BLOBPipeline</span><span class="sxs-lookup"><span data-stu-id="6662e-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6662e-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="6662e-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6662e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6662e-108">DESCRIPTION</span></span>
<span data-ttu-id="6662e-109">Il **cmdlet Stop-AzStorageBlobCopy** interrompe un'operazione di copia nel BLOB di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="6662e-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="6662e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6662e-110">EXAMPLES</span></span>

### <span data-ttu-id="6662e-111">Esempio 1: Interrompere l'operazione di copia in base al nome</span><span class="sxs-lookup"><span data-stu-id="6662e-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="6662e-112">Questo comando interrompe l'operazione di copia in base al nome.</span><span class="sxs-lookup"><span data-stu-id="6662e-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="6662e-113">Esempio 2: Interrompere l'operazione di copia usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="6662e-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="6662e-114">Questo comando interrompe l'operazione di copia passando il contenitore alla pipeline **da Get-AzStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="6662e-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="6662e-115">Esempio 3: Interrompere l'operazione di copia usando la pipeline e Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6662e-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="6662e-116">Questo esempio interrompe l'operazione di copia passando il contenitore alla pipeline dal cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="6662e-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="6662e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6662e-117">PARAMETERS</span></span>

### <span data-ttu-id="6662e-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="6662e-118">-Blob</span></span>
<span data-ttu-id="6662e-119">Specifica il nome del BLOB.</span><span class="sxs-lookup"><span data-stu-id="6662e-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="6662e-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6662e-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6662e-121">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="6662e-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6662e-122">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="6662e-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6662e-123">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="6662e-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6662e-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6662e-124">-CloudBlob</span></span>
<span data-ttu-id="6662e-125">Specifica un **oggetto CloudBlob** dalla libreria del client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6662e-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="6662e-126">Per ottenere un **oggetto CloudBlob,** usare il cmdlet Get-AzStorageBlob CloudBlob.</span><span class="sxs-lookup"><span data-stu-id="6662e-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="6662e-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6662e-127">-CloudBlobContainer</span></span>
<span data-ttu-id="6662e-128">Specifica un **oggetto CloudBlobContainer** dalla libreria client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6662e-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="6662e-129">È possibile creare l'oggetto o usare Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6662e-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="6662e-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6662e-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6662e-131">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="6662e-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6662e-132">È possibile usare questo parametro per limitare la simultaneità per limitare l'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="6662e-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6662e-133">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="6662e-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6662e-134">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="6662e-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6662e-135">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="6662e-135">The default value is 10.</span></span>

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

### <span data-ttu-id="6662e-136">-Container</span><span class="sxs-lookup"><span data-stu-id="6662e-136">-Container</span></span>
<span data-ttu-id="6662e-137">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="6662e-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="6662e-138">-Context</span><span class="sxs-lookup"><span data-stu-id="6662e-138">-Context</span></span>
<span data-ttu-id="6662e-139">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6662e-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6662e-140">È possibile creare il contesto usando il cmdlet New-AzStorageContext istruzione.</span><span class="sxs-lookup"><span data-stu-id="6662e-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6662e-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="6662e-141">-CopyId</span></span>
<span data-ttu-id="6662e-142">Specifica l'ID copia.</span><span class="sxs-lookup"><span data-stu-id="6662e-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="6662e-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6662e-143">-DefaultProfile</span></span>
<span data-ttu-id="6662e-144">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6662e-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6662e-145">-Force</span><span class="sxs-lookup"><span data-stu-id="6662e-145">-Force</span></span>
<span data-ttu-id="6662e-146">Interrompe l'attività di copia corrente nel BLOB specificato senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6662e-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6662e-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6662e-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6662e-148">Specifica l'intervallo di timeout del lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="6662e-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="6662e-149">Se prima dell'elaborazione della richiesta da parte del servizio è trascorso l'intervallo specificato, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="6662e-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6662e-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6662e-150">-Confirm</span></span>
<span data-ttu-id="6662e-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6662e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6662e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6662e-152">-WhatIf</span></span>
<span data-ttu-id="6662e-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6662e-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6662e-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6662e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6662e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6662e-155">CommonParameters</span></span>
<span data-ttu-id="6662e-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6662e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6662e-157">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6662e-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6662e-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="6662e-158">INPUTS</span></span>

### <span data-ttu-id="6662e-159">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6662e-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="6662e-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6662e-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="6662e-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6662e-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6662e-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6662e-162">OUTPUTS</span></span>

### <span data-ttu-id="6662e-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6662e-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="6662e-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="6662e-164">NOTES</span></span>

## <span data-ttu-id="6662e-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6662e-165">RELATED LINKS</span></span>

[<span data-ttu-id="6662e-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6662e-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="6662e-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6662e-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="6662e-168">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6662e-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="6662e-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="6662e-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
