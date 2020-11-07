---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 7d2363f0fc9955ac75444c18da137dcfee345664
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676538"
---
# <span data-ttu-id="dc579-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="dc579-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="dc579-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc579-102">SYNOPSIS</span></span>
<span data-ttu-id="dc579-103">Rimuove il BLOB di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="dc579-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="dc579-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc579-104">SYNTAX</span></span>

### <span data-ttu-id="dc579-105">NamePipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dc579-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc579-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="dc579-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc579-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="dc579-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc579-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc579-108">DESCRIPTION</span></span>
<span data-ttu-id="dc579-109">Il cmdlet **Remove-AzStorageBlob** rimuove il blob specificato da un account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="dc579-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="dc579-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc579-110">EXAMPLES</span></span>

### <span data-ttu-id="dc579-111">Esempio 1: rimuovere un BLOB di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="dc579-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="dc579-112">Questo comando rimuove un BLOB identificato dal relativo nome.</span><span class="sxs-lookup"><span data-stu-id="dc579-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="dc579-113">Esempio 2: rimuovere un BLOB di archiviazione tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="dc579-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="dc579-114">Questo comando usa la pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc579-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="dc579-115">Esempio 3: rimuovere i BLOB di archiviazione tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="dc579-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="dc579-116">Questo comando usa il carattere jolly asterisco (\*) e la pipeline per recuperare BLOB o BLOB e quindi rimuoverli.</span><span class="sxs-lookup"><span data-stu-id="dc579-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="dc579-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc579-117">PARAMETERS</span></span>

### <span data-ttu-id="dc579-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="dc579-118">-Blob</span></span>
<span data-ttu-id="dc579-119">Specifica il nome del BLOB che si vuole rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dc579-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="dc579-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dc579-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dc579-121">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="dc579-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dc579-122">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="dc579-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dc579-123">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="dc579-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dc579-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="dc579-124">-CloudBlob</span></span>
<span data-ttu-id="dc579-125">Specifica un BLOB cloud.</span><span class="sxs-lookup"><span data-stu-id="dc579-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="dc579-126">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="dc579-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="dc579-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="dc579-127">-CloudBlobContainer</span></span>
<span data-ttu-id="dc579-128">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dc579-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="dc579-129">Puoi usare il cmdlet Get-AzStorageContainer per recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="dc579-129">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="dc579-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dc579-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dc579-131">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="dc579-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="dc579-132">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="dc579-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="dc579-133">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="dc579-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="dc579-134">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="dc579-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="dc579-135">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="dc579-135">The default value is 10.</span></span>

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

### <span data-ttu-id="dc579-136">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="dc579-136">-Container</span></span>
<span data-ttu-id="dc579-137">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="dc579-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="dc579-138">-Contesto</span><span class="sxs-lookup"><span data-stu-id="dc579-138">-Context</span></span>
<span data-ttu-id="dc579-139">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dc579-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="dc579-140">Puoi usare il cmdlet New-AzStorageContext per crearlo.</span><span class="sxs-lookup"><span data-stu-id="dc579-140">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="dc579-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc579-141">-DefaultProfile</span></span>
<span data-ttu-id="dc579-142">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc579-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc579-143">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="dc579-143">-DeleteSnapshot</span></span>
<span data-ttu-id="dc579-144">Specifica che tutti gli snapshot verranno eliminati, ma non per i BLOB di base.</span><span class="sxs-lookup"><span data-stu-id="dc579-144">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="dc579-145">Se questo parametro non viene specificato, il BLOB di base e i relativi snapshot vengono eliminati insieme.</span><span class="sxs-lookup"><span data-stu-id="dc579-145">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="dc579-146">All'utente viene richiesto di confermare l'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="dc579-146">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="dc579-147">-Force</span><span class="sxs-lookup"><span data-stu-id="dc579-147">-Force</span></span>
<span data-ttu-id="dc579-148">Indica che questo cmdlet rimuove il BLOB e lo snapshot senza conferma.</span><span class="sxs-lookup"><span data-stu-id="dc579-148">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="dc579-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc579-149">-PassThru</span></span>
<span data-ttu-id="dc579-150">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dc579-150">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="dc579-151">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="dc579-151">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="dc579-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dc579-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dc579-153">Specifica il profilo Azure per il cmdlet da leggere.</span><span class="sxs-lookup"><span data-stu-id="dc579-153">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="dc579-154">Se non specificato, il cmdlet legge il profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="dc579-154">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="dc579-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dc579-155">-Confirm</span></span>
<span data-ttu-id="dc579-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc579-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc579-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc579-157">-WhatIf</span></span>
<span data-ttu-id="dc579-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc579-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc579-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc579-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc579-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc579-160">CommonParameters</span></span>
<span data-ttu-id="dc579-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc579-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc579-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc579-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc579-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc579-163">INPUTS</span></span>

### <span data-ttu-id="dc579-164">Microsoft. WindowsAzure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="dc579-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="dc579-165">Microsoft. WindowsAzure. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="dc579-165">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="dc579-166">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dc579-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dc579-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc579-167">OUTPUTS</span></span>

### <span data-ttu-id="dc579-168">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc579-168">System.Boolean</span></span>

## <span data-ttu-id="dc579-169">Note</span><span class="sxs-lookup"><span data-stu-id="dc579-169">NOTES</span></span>

## <span data-ttu-id="dc579-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc579-170">RELATED LINKS</span></span>

[<span data-ttu-id="dc579-171">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="dc579-171">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="dc579-172">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dc579-172">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="dc579-173">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dc579-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)