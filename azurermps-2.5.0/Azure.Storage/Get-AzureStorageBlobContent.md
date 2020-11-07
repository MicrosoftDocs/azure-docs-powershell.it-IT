---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcontent
schema: 2.0.0
ms.openlocfilehash: 4b48e4c2e1184c26fd7b50a05e979fad1a61bf3b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866409"
---
# <span data-ttu-id="c9a80-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c9a80-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="c9a80-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9a80-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a80-103">Scarica un BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c9a80-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9a80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9a80-104">SYNTAX</span></span>

### <span data-ttu-id="c9a80-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c9a80-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9a80-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="c9a80-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9a80-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="c9a80-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9a80-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9a80-108">DESCRIPTION</span></span>
<span data-ttu-id="c9a80-109">Il cmdlet **Get-AzureStorageBlobContent** Scarica il BLOB di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="c9a80-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="c9a80-110">Se il nome del BLOB non è valido per il computer locale, questo cmdlet lo risolve automaticamente, se possibile.</span><span class="sxs-lookup"><span data-stu-id="c9a80-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="c9a80-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9a80-111">EXAMPLES</span></span>

### <span data-ttu-id="c9a80-112">Esempio 1: scaricare il contenuto BLOB per nome</span><span class="sxs-lookup"><span data-stu-id="c9a80-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="c9a80-113">Questo comando Scarica un BLOB per nome.</span><span class="sxs-lookup"><span data-stu-id="c9a80-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="c9a80-114">Esempio 2: scaricare il contenuto BLOB usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="c9a80-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="c9a80-115">Questo comando usa la pipeline per trovare e scaricare contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="c9a80-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="c9a80-116">Esempio 3: scaricare il contenuto BLOB usando la pipeline e un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="c9a80-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="c9a80-117">Questo esempio usa il carattere jolly asterisco e la pipeline per trovare e scaricare contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="c9a80-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="c9a80-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9a80-118">PARAMETERS</span></span>

### <span data-ttu-id="c9a80-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="c9a80-119">-Blob</span></span>
<span data-ttu-id="c9a80-120">Specifica il nome del BLOB da scaricare.</span><span class="sxs-lookup"><span data-stu-id="c9a80-120">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="c9a80-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="c9a80-121">-CheckMd5</span></span>
<span data-ttu-id="c9a80-122">Specifica se controllare la somma MD5 per il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="c9a80-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="c9a80-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c9a80-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c9a80-124">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="c9a80-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c9a80-125">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c9a80-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c9a80-126">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="c9a80-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c9a80-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c9a80-127">-CloudBlob</span></span>
<span data-ttu-id="c9a80-128">Specifica un BLOB cloud.</span><span class="sxs-lookup"><span data-stu-id="c9a80-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="c9a80-129">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="c9a80-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9a80-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c9a80-130">-CloudBlobContainer</span></span>
<span data-ttu-id="c9a80-131">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9a80-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="c9a80-132">Puoi crearlo o usare il cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="c9a80-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9a80-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c9a80-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c9a80-134">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="c9a80-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c9a80-135">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="c9a80-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c9a80-136">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="c9a80-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c9a80-137">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="c9a80-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c9a80-138">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="c9a80-138">The default value is 10.</span></span>
<span data-ttu-id="c9a80-139">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="c9a80-139">The default value is 10.</span></span>

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

### <span data-ttu-id="c9a80-140">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="c9a80-140">-Container</span></span>
<span data-ttu-id="c9a80-141">Specifica il nome del contenitore con il BLOB che si vuole scaricare.</span><span class="sxs-lookup"><span data-stu-id="c9a80-141">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="c9a80-142">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c9a80-142">-Context</span></span>
<span data-ttu-id="c9a80-143">Specifica l'account di archiviazione di Azure da cui si vuole scaricare il contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="c9a80-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="c9a80-144">Puoi usare il cmdlet New-AzureStorageContext per creare un contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c9a80-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="c9a80-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a80-145">-DefaultProfile</span></span>
<span data-ttu-id="c9a80-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9a80-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9a80-147">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="c9a80-147">-Destination</span></span>
<span data-ttu-id="c9a80-148">Specifica il percorso in cui archiviare il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="c9a80-148">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="c9a80-149">-Force</span><span class="sxs-lookup"><span data-stu-id="c9a80-149">-Force</span></span>
<span data-ttu-id="c9a80-150">Sovrascrive un file esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="c9a80-150">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="c9a80-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c9a80-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c9a80-152">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="c9a80-152">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c9a80-153">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="c9a80-153">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c9a80-154">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c9a80-154">-Confirm</span></span>
<span data-ttu-id="c9a80-155">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9a80-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9a80-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9a80-156">-WhatIf</span></span>
<span data-ttu-id="c9a80-157">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9a80-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9a80-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9a80-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9a80-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a80-159">CommonParameters</span></span>
<span data-ttu-id="c9a80-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9a80-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a80-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9a80-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a80-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9a80-162">INPUTS</span></span>

### <span data-ttu-id="c9a80-163">Microsoft. WindowsAzure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c9a80-163">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="c9a80-164">Microsoft. WindowsAzure. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c9a80-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="c9a80-165">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c9a80-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c9a80-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9a80-166">OUTPUTS</span></span>

### <span data-ttu-id="c9a80-167">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c9a80-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="c9a80-168">Note</span><span class="sxs-lookup"><span data-stu-id="c9a80-168">NOTES</span></span>
* <span data-ttu-id="c9a80-169">Se il nome del BLOB non è valido per il computer locale, questo cmdlet la risolve in autonomia, se possibile.</span><span class="sxs-lookup"><span data-stu-id="c9a80-169">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="c9a80-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9a80-170">RELATED LINKS</span></span>

[<span data-ttu-id="c9a80-171">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c9a80-171">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="c9a80-172">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c9a80-172">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="c9a80-173">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c9a80-173">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
