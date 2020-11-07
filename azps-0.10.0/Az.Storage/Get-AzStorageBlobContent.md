---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: 53f162ccf811176d375c745b1dbb539dba10f000
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862253"
---
# <span data-ttu-id="59752-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="59752-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="59752-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59752-102">SYNOPSIS</span></span>
<span data-ttu-id="59752-103">Scarica un BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="59752-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="59752-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59752-104">SYNTAX</span></span>

### <span data-ttu-id="59752-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59752-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59752-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="59752-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59752-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="59752-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59752-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59752-108">DESCRIPTION</span></span>
<span data-ttu-id="59752-109">Il cmdlet **Get-AzStorageBlobContent** Scarica il BLOB di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="59752-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="59752-110">Se il nome del BLOB non è valido per il computer locale, questo cmdlet lo risolve automaticamente, se possibile.</span><span class="sxs-lookup"><span data-stu-id="59752-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="59752-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59752-111">EXAMPLES</span></span>

### <span data-ttu-id="59752-112">Esempio 1: scaricare il contenuto BLOB per nome</span><span class="sxs-lookup"><span data-stu-id="59752-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="59752-113">Questo comando Scarica un BLOB per nome.</span><span class="sxs-lookup"><span data-stu-id="59752-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="59752-114">Esempio 2: scaricare il contenuto BLOB usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="59752-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="59752-115">Questo comando usa la pipeline per trovare e scaricare contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="59752-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="59752-116">Esempio 3: scaricare il contenuto BLOB usando la pipeline e un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="59752-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="59752-117">Questo esempio usa il carattere jolly asterisco e la pipeline per trovare e scaricare contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="59752-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="59752-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59752-118">PARAMETERS</span></span>

### <span data-ttu-id="59752-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="59752-119">-Blob</span></span>
<span data-ttu-id="59752-120">Specifica il nome del BLOB da scaricare.</span><span class="sxs-lookup"><span data-stu-id="59752-120">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="59752-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="59752-121">-CheckMd5</span></span>
<span data-ttu-id="59752-122">Specifica se controllare la somma MD5 per il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="59752-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="59752-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="59752-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="59752-124">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="59752-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="59752-125">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="59752-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="59752-126">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="59752-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="59752-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="59752-127">-CloudBlob</span></span>
<span data-ttu-id="59752-128">Specifica un BLOB cloud.</span><span class="sxs-lookup"><span data-stu-id="59752-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="59752-129">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="59752-129">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59752-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="59752-130">-CloudBlobContainer</span></span>
<span data-ttu-id="59752-131">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="59752-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="59752-132">Puoi crearlo o usare il cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="59752-132">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59752-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="59752-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="59752-134">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="59752-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="59752-135">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="59752-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="59752-136">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="59752-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="59752-137">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="59752-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="59752-138">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="59752-138">The default value is 10.</span></span>
<span data-ttu-id="59752-139">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="59752-139">The default value is 10.</span></span>

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

### <span data-ttu-id="59752-140">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="59752-140">-Container</span></span>
<span data-ttu-id="59752-141">Specifica il nome del contenitore con il BLOB che si vuole scaricare.</span><span class="sxs-lookup"><span data-stu-id="59752-141">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="59752-142">-Contesto</span><span class="sxs-lookup"><span data-stu-id="59752-142">-Context</span></span>
<span data-ttu-id="59752-143">Specifica l'account di archiviazione di Azure da cui si vuole scaricare il contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="59752-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="59752-144">Puoi usare il cmdlet New-AzStorageContext per creare un contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="59752-144">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="59752-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59752-145">-DefaultProfile</span></span>
<span data-ttu-id="59752-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59752-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59752-147">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="59752-147">-Destination</span></span>
<span data-ttu-id="59752-148">Specifica il percorso in cui archiviare il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="59752-148">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="59752-149">-Force</span><span class="sxs-lookup"><span data-stu-id="59752-149">-Force</span></span>
<span data-ttu-id="59752-150">Sovrascrive un file esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="59752-150">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="59752-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="59752-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="59752-152">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="59752-152">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="59752-153">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="59752-153">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="59752-154">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59752-154">-Confirm</span></span>
<span data-ttu-id="59752-155">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59752-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59752-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59752-156">-WhatIf</span></span>
<span data-ttu-id="59752-157">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59752-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59752-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59752-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59752-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59752-159">CommonParameters</span></span>
<span data-ttu-id="59752-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59752-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59752-161">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59752-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59752-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59752-162">INPUTS</span></span>

### <span data-ttu-id="59752-163">Microsoft. WindowsAz. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="59752-163">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="59752-164">Microsoft. WindowsAz. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="59752-164">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="59752-165">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="59752-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="59752-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59752-166">OUTPUTS</span></span>

### <span data-ttu-id="59752-167">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="59752-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="59752-168">Note</span><span class="sxs-lookup"><span data-stu-id="59752-168">NOTES</span></span>
* <span data-ttu-id="59752-169">Se il nome del BLOB non è valido per il computer locale, questo cmdlet la risolve in autonomia, se possibile.</span><span class="sxs-lookup"><span data-stu-id="59752-169">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="59752-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59752-170">RELATED LINKS</span></span>

[<span data-ttu-id="59752-171">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="59752-171">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="59752-172">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="59752-172">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="59752-173">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="59752-173">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
