---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: eec7d4b29f752d3bf302dc9f5c35fa5c6da51c6f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349684"
---
# <span data-ttu-id="2f665-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2f665-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="2f665-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f665-102">SYNOPSIS</span></span>
<span data-ttu-id="2f665-103">Scarica un BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2f665-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="2f665-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f665-104">SYNTAX</span></span>

### <span data-ttu-id="2f665-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2f665-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f665-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="2f665-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f665-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="2f665-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f665-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f665-108">DESCRIPTION</span></span>
<span data-ttu-id="2f665-109">Il cmdlet **Get-AzStorageBlobContent** Scarica il BLOB di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="2f665-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="2f665-110">Se il nome del BLOB non è valido per il computer locale, questo cmdlet lo risolve automaticamente, se possibile.</span><span class="sxs-lookup"><span data-stu-id="2f665-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="2f665-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f665-111">EXAMPLES</span></span>

### <span data-ttu-id="2f665-112">Esempio 1: scaricare il contenuto BLOB per nome</span><span class="sxs-lookup"><span data-stu-id="2f665-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="2f665-113">Questo comando Scarica un BLOB per nome.</span><span class="sxs-lookup"><span data-stu-id="2f665-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="2f665-114">Esempio 2: scaricare il contenuto BLOB usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="2f665-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="2f665-115">Questo comando usa la pipeline per trovare e scaricare contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="2f665-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="2f665-116">Esempio 3: scaricare il contenuto BLOB usando la pipeline e un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="2f665-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="2f665-117">Questo esempio usa il carattere jolly asterisco e la pipeline per trovare e scaricare contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="2f665-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="2f665-118">Esempio 4: ottenere un oggetto BLOB e salvarlo in una variabile, quindi scaricare il contenuto BLOB con l'oggetto BLOB</span><span class="sxs-lookup"><span data-stu-id="2f665-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="2f665-119">Questo esempio ottiene prima di tutto un oggetto BLOB e lo salva in una variabile, quindi Scarica il contenuto BLOB con l'oggetto BLOB.</span><span class="sxs-lookup"><span data-stu-id="2f665-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="2f665-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f665-120">PARAMETERS</span></span>

### <span data-ttu-id="2f665-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f665-121">-AsJob</span></span>
<span data-ttu-id="2f665-122">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="2f665-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2f665-123">-BLOB</span><span class="sxs-lookup"><span data-stu-id="2f665-123">-Blob</span></span>
<span data-ttu-id="2f665-124">Specifica il nome del BLOB da scaricare.</span><span class="sxs-lookup"><span data-stu-id="2f665-124">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f665-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="2f665-125">-BlobBaseClient</span></span>
<span data-ttu-id="2f665-126">Oggetto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="2f665-126">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="2f665-127">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="2f665-127">-CheckMd5</span></span>
<span data-ttu-id="2f665-128">Specifica se controllare la somma MD5 per il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="2f665-128">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="2f665-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2f665-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2f665-130">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="2f665-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2f665-131">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="2f665-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2f665-132">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="2f665-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2f665-133">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2f665-133">-CloudBlob</span></span>
<span data-ttu-id="2f665-134">Specifica un BLOB cloud.</span><span class="sxs-lookup"><span data-stu-id="2f665-134">Specifies a cloud blob.</span></span>
<span data-ttu-id="2f665-135">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="2f665-135">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="2f665-136">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2f665-136">-CloudBlobContainer</span></span>
<span data-ttu-id="2f665-137">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2f665-137">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="2f665-138">Puoi crearlo o usare il cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="2f665-138">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="2f665-139">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2f665-139">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2f665-140">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="2f665-140">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2f665-141">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="2f665-141">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2f665-142">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="2f665-142">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2f665-143">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="2f665-143">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2f665-144">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="2f665-144">The default value is 10.</span></span>

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

### <span data-ttu-id="2f665-145">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="2f665-145">-Container</span></span>
<span data-ttu-id="2f665-146">Specifica il nome del contenitore con il BLOB che si vuole scaricare.</span><span class="sxs-lookup"><span data-stu-id="2f665-146">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f665-147">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2f665-147">-Context</span></span>
<span data-ttu-id="2f665-148">Specifica l'account di archiviazione di Azure da cui si vuole scaricare il contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="2f665-148">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="2f665-149">Puoi usare il cmdlet New-AzStorageContext per creare un contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2f665-149">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="2f665-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f665-150">-DefaultProfile</span></span>
<span data-ttu-id="2f665-151">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f665-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f665-152">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="2f665-152">-Destination</span></span>
<span data-ttu-id="2f665-153">Specifica il percorso in cui archiviare il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="2f665-153">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f665-154">-Force</span><span class="sxs-lookup"><span data-stu-id="2f665-154">-Force</span></span>
<span data-ttu-id="2f665-155">Sovrascrive un file esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="2f665-155">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="2f665-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2f665-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2f665-157">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="2f665-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2f665-158">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="2f665-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2f665-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2f665-159">-Confirm</span></span>
<span data-ttu-id="2f665-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f665-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f665-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f665-161">-WhatIf</span></span>
<span data-ttu-id="2f665-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f665-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f665-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f665-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f665-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f665-164">CommonParameters</span></span>
<span data-ttu-id="2f665-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f665-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f665-166">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f665-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f665-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f665-167">INPUTS</span></span>

### <span data-ttu-id="2f665-168">Microsoft. Azure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2f665-168">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="2f665-169">Microsoft. Azure. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2f665-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="2f665-170">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2f665-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2f665-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f665-171">OUTPUTS</span></span>

### <span data-ttu-id="2f665-172">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2f665-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="2f665-173">Note</span><span class="sxs-lookup"><span data-stu-id="2f665-173">NOTES</span></span>
* <span data-ttu-id="2f665-174">Se il nome del BLOB non è valido per il computer locale, questo cmdlet la risolve in autonomia, se possibile.</span><span class="sxs-lookup"><span data-stu-id="2f665-174">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="2f665-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f665-175">RELATED LINKS</span></span>

[<span data-ttu-id="2f665-176">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2f665-176">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="2f665-177">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2f665-177">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="2f665-178">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2f665-178">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
