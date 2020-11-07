---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: 76af94e4ab2518a47fad03f31a2f0f24bb0d0422
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676631"
---
# <span data-ttu-id="a0bcb-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a0bcb-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="a0bcb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="a0bcb-103">Scarica un BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="a0bcb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0bcb-104">SYNTAX</span></span>

### <span data-ttu-id="a0bcb-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0bcb-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0bcb-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="a0bcb-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0bcb-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="a0bcb-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0bcb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0bcb-108">DESCRIPTION</span></span>
<span data-ttu-id="a0bcb-109">Il cmdlet **Get-AzStorageBlobContent** Scarica il BLOB di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="a0bcb-110">Se il nome del BLOB non è valido per il computer locale, questo cmdlet lo risolve automaticamente, se possibile.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="a0bcb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0bcb-111">EXAMPLES</span></span>

### <span data-ttu-id="a0bcb-112">Esempio 1: scaricare il contenuto BLOB per nome</span><span class="sxs-lookup"><span data-stu-id="a0bcb-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="a0bcb-113">Questo comando Scarica un BLOB per nome.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="a0bcb-114">Esempio 2: scaricare il contenuto BLOB usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="a0bcb-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="a0bcb-115">Questo comando usa la pipeline per trovare e scaricare contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="a0bcb-116">Esempio 3: scaricare il contenuto BLOB usando la pipeline e un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="a0bcb-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="a0bcb-117">Questo esempio usa il carattere jolly asterisco e la pipeline per trovare e scaricare contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="a0bcb-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0bcb-118">PARAMETERS</span></span>

### <span data-ttu-id="a0bcb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0bcb-119">-AsJob</span></span>
<span data-ttu-id="a0bcb-120">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a0bcb-121">-BLOB</span><span class="sxs-lookup"><span data-stu-id="a0bcb-121">-Blob</span></span>
<span data-ttu-id="a0bcb-122">Specifica il nome del BLOB da scaricare.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-122">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="a0bcb-123">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="a0bcb-123">-CheckMd5</span></span>
<span data-ttu-id="a0bcb-124">Specifica se controllare la somma MD5 per il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-124">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="a0bcb-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0bcb-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a0bcb-126">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-126">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a0bcb-127">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-127">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a0bcb-128">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-128">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a0bcb-129">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a0bcb-129">-CloudBlob</span></span>
<span data-ttu-id="a0bcb-130">Specifica un BLOB cloud.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-130">Specifies a cloud blob.</span></span>
<span data-ttu-id="a0bcb-131">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-131">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="a0bcb-132">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a0bcb-132">-CloudBlobContainer</span></span>
<span data-ttu-id="a0bcb-133">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-133">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="a0bcb-134">Puoi crearlo o usare il cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-134">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="a0bcb-135">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a0bcb-135">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a0bcb-136">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-136">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a0bcb-137">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-137">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a0bcb-138">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-138">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a0bcb-139">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-139">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a0bcb-140">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-140">The default value is 10.</span></span>
<span data-ttu-id="a0bcb-141">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-141">The default value is 10.</span></span>

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

### <span data-ttu-id="a0bcb-142">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="a0bcb-142">-Container</span></span>
<span data-ttu-id="a0bcb-143">Specifica il nome del contenitore con il BLOB che si vuole scaricare.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-143">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="a0bcb-144">-Contesto</span><span class="sxs-lookup"><span data-stu-id="a0bcb-144">-Context</span></span>
<span data-ttu-id="a0bcb-145">Specifica l'account di archiviazione di Azure da cui si vuole scaricare il contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-145">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="a0bcb-146">Puoi usare il cmdlet New-AzStorageContext per creare un contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-146">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="a0bcb-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0bcb-147">-DefaultProfile</span></span>
<span data-ttu-id="a0bcb-148">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0bcb-149">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="a0bcb-149">-Destination</span></span>
<span data-ttu-id="a0bcb-150">Specifica il percorso in cui archiviare il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-150">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="a0bcb-151">-Force</span><span class="sxs-lookup"><span data-stu-id="a0bcb-151">-Force</span></span>
<span data-ttu-id="a0bcb-152">Sovrascrive un file esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-152">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="a0bcb-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0bcb-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a0bcb-154">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-154">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a0bcb-155">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-155">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a0bcb-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0bcb-156">-Confirm</span></span>
<span data-ttu-id="a0bcb-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0bcb-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0bcb-158">-WhatIf</span></span>
<span data-ttu-id="a0bcb-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0bcb-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0bcb-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0bcb-161">CommonParameters</span></span>
<span data-ttu-id="a0bcb-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0bcb-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0bcb-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0bcb-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0bcb-164">INPUTS</span></span>

### <span data-ttu-id="a0bcb-165">Microsoft. WindowsAzure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a0bcb-165">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="a0bcb-166">Microsoft. WindowsAzure. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a0bcb-166">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="a0bcb-167">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a0bcb-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a0bcb-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0bcb-168">OUTPUTS</span></span>

### <span data-ttu-id="a0bcb-169">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a0bcb-169">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="a0bcb-170">Note</span><span class="sxs-lookup"><span data-stu-id="a0bcb-170">NOTES</span></span>
* <span data-ttu-id="a0bcb-171">Se il nome del BLOB non è valido per il computer locale, questo cmdlet la risolve in autonomia, se possibile.</span><span class="sxs-lookup"><span data-stu-id="a0bcb-171">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="a0bcb-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0bcb-172">RELATED LINKS</span></span>

[<span data-ttu-id="a0bcb-173">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a0bcb-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="a0bcb-174">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a0bcb-174">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="a0bcb-175">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a0bcb-175">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
