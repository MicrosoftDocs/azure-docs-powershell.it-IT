---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageBlob.md
ms.openlocfilehash: b9d987dad0542f7637f7d061ee510c1601dc6e6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512768"
---
# <span data-ttu-id="6ff64-101">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6ff64-101">Remove-AzureStorageBlob</span></span>

## <span data-ttu-id="6ff64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ff64-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff64-103">Rimuove il BLOB di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="6ff64-103">Removes the specified storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ff64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ff64-104">SYNTAX</span></span>

### <span data-ttu-id="6ff64-105">NamePipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ff64-105">NamePipeline (Default)</span></span>
```
Remove-AzureStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ff64-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="6ff64-106">BlobPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ff64-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="6ff64-107">ContainerPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ff64-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ff64-108">DESCRIPTION</span></span>
<span data-ttu-id="6ff64-109">Il cmdlet **Remove-AzureStorageBlob** rimuove il blob specificato da un account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff64-109">The **Remove-AzureStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="6ff64-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ff64-110">EXAMPLES</span></span>

### <span data-ttu-id="6ff64-111">Esempio 1: rimuovere un BLOB di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="6ff64-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzureStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="6ff64-112">Questo comando rimuove un BLOB identificato dal relativo nome.</span><span class="sxs-lookup"><span data-stu-id="6ff64-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="6ff64-113">Esempio 2: rimuovere un BLOB di archiviazione tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="6ff64-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzureStorageBlob
```

<span data-ttu-id="6ff64-114">Questo comando usa la pipeline.</span><span class="sxs-lookup"><span data-stu-id="6ff64-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="6ff64-115">Esempio 3: rimuovere i BLOB di archiviazione tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="6ff64-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container* | Remove-AzureStorageBlob -Blob "BlobName"
```

<span data-ttu-id="6ff64-116">Questo comando usa il carattere jolly asterisco (\*) e la pipeline per recuperare BLOB o BLOB e quindi rimuoverli.</span><span class="sxs-lookup"><span data-stu-id="6ff64-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="6ff64-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ff64-117">PARAMETERS</span></span>

### <span data-ttu-id="6ff64-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="6ff64-118">-Blob</span></span>
<span data-ttu-id="6ff64-119">Specifica il nome del BLOB che si vuole rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6ff64-119">Specifies the name of the blob you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ff64-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6ff64-121">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="6ff64-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6ff64-122">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="6ff64-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6ff64-123">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="6ff64-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6ff64-124">-CloudBlob</span></span>
<span data-ttu-id="6ff64-125">Specifica un BLOB cloud.</span><span class="sxs-lookup"><span data-stu-id="6ff64-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="6ff64-126">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="6ff64-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6ff64-127">-CloudBlobContainer</span></span>
<span data-ttu-id="6ff64-128">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff64-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="6ff64-129">Puoi usare il cmdlet Get-AzureStorageContainer per recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="6ff64-129">You can use the Get-AzureStorageContainer cmdlet to get it.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6ff64-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6ff64-131">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="6ff64-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6ff64-132">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="6ff64-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6ff64-133">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="6ff64-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6ff64-134">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="6ff64-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6ff64-135">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="6ff64-135">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-136">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="6ff64-136">-Container</span></span>
<span data-ttu-id="6ff64-137">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="6ff64-137">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-138">-Contesto</span><span class="sxs-lookup"><span data-stu-id="6ff64-138">-Context</span></span>
<span data-ttu-id="6ff64-139">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff64-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6ff64-140">Puoi usare il cmdlet New-AzureStorageContext per crearlo.</span><span class="sxs-lookup"><span data-stu-id="6ff64-140">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-141">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="6ff64-141">-DeleteSnapshot</span></span>
<span data-ttu-id="6ff64-142">Specifica che tutti gli snapshot verranno eliminati, ma non per i BLOB di base.</span><span class="sxs-lookup"><span data-stu-id="6ff64-142">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="6ff64-143">Se questo parametro non viene specificato, il BLOB di base e i relativi snapshot vengono eliminati insieme.</span><span class="sxs-lookup"><span data-stu-id="6ff64-143">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="6ff64-144">All'utente viene richiesto di confermare l'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="6ff64-144">The user is prompted to confirm the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-145">-Force</span><span class="sxs-lookup"><span data-stu-id="6ff64-145">-Force</span></span>
<span data-ttu-id="6ff64-146">Indica che questo cmdlet rimuove il BLOB e lo snapshot senza conferma.</span><span class="sxs-lookup"><span data-stu-id="6ff64-146">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ff64-147">-PassThru</span></span>
<span data-ttu-id="6ff64-148">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6ff64-148">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6ff64-149">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6ff64-149">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-150">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ff64-150">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6ff64-151">Specifica il profilo Azure per il cmdlet da leggere.</span><span class="sxs-lookup"><span data-stu-id="6ff64-151">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="6ff64-152">Se non specificato, il cmdlet legge il profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="6ff64-152">If not specified, the cmdlet reads from the default profile.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ff64-153">-Confirm</span></span>
<span data-ttu-id="6ff64-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff64-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff64-155">-WhatIf</span></span>
<span data-ttu-id="6ff64-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ff64-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ff64-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ff64-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff64-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff64-158">CommonParameters</span></span>
<span data-ttu-id="6ff64-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff64-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff64-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ff64-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff64-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ff64-161">INPUTS</span></span>

### <span data-ttu-id="6ff64-162">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ff64-162">IStorageContext</span></span>

<span data-ttu-id="6ff64-163">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6ff64-163">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="6ff64-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ff64-164">OUTPUTS</span></span>

### <span data-ttu-id="6ff64-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ff64-165">System.Boolean</span></span>

## <span data-ttu-id="6ff64-166">Note</span><span class="sxs-lookup"><span data-stu-id="6ff64-166">NOTES</span></span>

## <span data-ttu-id="6ff64-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ff64-167">RELATED LINKS</span></span>

[<span data-ttu-id="6ff64-168">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6ff64-168">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="6ff64-169">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6ff64-169">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="6ff64-170">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6ff64-170">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)
