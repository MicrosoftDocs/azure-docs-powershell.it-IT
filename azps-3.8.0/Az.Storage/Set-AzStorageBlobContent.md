---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 7490062a096c561d1d0d5ba2edee070da8c3b687
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021012"
---
# <span data-ttu-id="9f51d-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9f51d-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="9f51d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f51d-102">SYNOPSIS</span></span>
<span data-ttu-id="9f51d-103">Carica un file locale in un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9f51d-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="9f51d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f51d-104">SYNTAX</span></span>

### <span data-ttu-id="9f51d-105">SendManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9f51d-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f51d-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="9f51d-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f51d-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="9f51d-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f51d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f51d-108">DESCRIPTION</span></span>
<span data-ttu-id="9f51d-109">Il cmdlet **set-AzStorageBlobContent** carica un file locale in un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9f51d-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="9f51d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f51d-110">EXAMPLES</span></span>

### <span data-ttu-id="9f51d-111">Esempio 1: caricare un file denominato</span><span class="sxs-lookup"><span data-stu-id="9f51d-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="9f51d-112">Questo comando carica il file denominato PlanningData in un BLOB denominato Planning2015.</span><span class="sxs-lookup"><span data-stu-id="9f51d-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="9f51d-113">Esempio 2: caricare tutti i file nella cartella corrente</span><span class="sxs-lookup"><span data-stu-id="9f51d-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="9f51d-114">Questo comando usa il cmdlet di Windows PowerShell di base Get-ChildItem per ottenere tutti i file nella cartella corrente e nelle sottocartelle e quindi li passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="9f51d-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9f51d-115">Il cmdlet **set-AzStorageBlobContent** carica i file nel contenitore denominato ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="9f51d-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="9f51d-116">Esempio 3: sovrascrivere un BLOB esistente</span><span class="sxs-lookup"><span data-stu-id="9f51d-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="9f51d-117">Questo comando ottiene il BLOB denominato Planning2015 nel contenitore ContosoUploads usando il cmdlet Get-AzStorageBlob e quindi passa tale BLOB al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="9f51d-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="9f51d-118">Il comando carica il file denominato ContosoPlanning come Planning2015.</span><span class="sxs-lookup"><span data-stu-id="9f51d-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="9f51d-119">Questo comando non specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="9f51d-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="9f51d-120">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="9f51d-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="9f51d-121">Se si conferma il comando, il cmdlet sovrascrive il BLOB esistente.</span><span class="sxs-lookup"><span data-stu-id="9f51d-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="9f51d-122">Esempio 4: caricare un file in un contenitore tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="9f51d-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="9f51d-123">Questo comando ottiene il contenitore che inizia con la stringa ContosoUpload usando il cmdlet **Get-AzStorageContainer** e quindi passa tale BLOB al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="9f51d-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="9f51d-124">Il comando carica il file denominato ContosoPlanning come Planning2015.</span><span class="sxs-lookup"><span data-stu-id="9f51d-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="9f51d-125">Esempio 5: caricare un file nel BLOB della pagina con metadati e PremiumPageBlobTier come P10</span><span class="sxs-lookup"><span data-stu-id="9f51d-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="9f51d-126">Il primo comando crea una tabella hash che contiene metadati per un BLOB e archivia la tabella hash nella variabile $Metadata.</span><span class="sxs-lookup"><span data-stu-id="9f51d-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="9f51d-127">Il secondo comando carica il file denominato ContosoPlanning nel contenitore denominato ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="9f51d-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="9f51d-128">Il BLOB include i metadati archiviati in $Metadata e ha PremiumPageBlobTier come P10.</span><span class="sxs-lookup"><span data-stu-id="9f51d-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="9f51d-129">Esempio 6: caricare un file in BLOB con le proprietà BLOB specificate e impostare StandardBlobTier come cool</span><span class="sxs-lookup"><span data-stu-id="9f51d-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool
```

<span data-ttu-id="9f51d-130">Questo comando carica il file denominato ContosoPlanning nel contenitore denominato ContosoUploads con le proprietà BLOB specificate e imposta StandardBlobTier come cool.</span><span class="sxs-lookup"><span data-stu-id="9f51d-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>

## <span data-ttu-id="9f51d-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f51d-131">PARAMETERS</span></span>

### <span data-ttu-id="9f51d-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f51d-132">-AsJob</span></span>
<span data-ttu-id="9f51d-133">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="9f51d-133">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9f51d-134">-BLOB</span><span class="sxs-lookup"><span data-stu-id="9f51d-134">-Blob</span></span>
<span data-ttu-id="9f51d-135">Specifica il nome di un BLOB.</span><span class="sxs-lookup"><span data-stu-id="9f51d-135">Specifies the name of a blob.</span></span>
<span data-ttu-id="9f51d-136">Questo cmdlet carica un file nel BLOB di archiviazione di Azure specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9f51d-136">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f51d-137">-BlobType</span><span class="sxs-lookup"><span data-stu-id="9f51d-137">-BlobType</span></span>
<span data-ttu-id="9f51d-138">Specifica il tipo per il BLOB caricato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f51d-138">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="9f51d-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9f51d-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f51d-140">Blocco</span><span class="sxs-lookup"><span data-stu-id="9f51d-140">Block</span></span>
- <span data-ttu-id="9f51d-141">Pagina il valore predefinito è Block.</span><span class="sxs-lookup"><span data-stu-id="9f51d-141">Page The default value is Block.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f51d-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9f51d-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9f51d-143">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="9f51d-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9f51d-144">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="9f51d-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9f51d-145">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9f51d-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9f51d-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9f51d-146">-CloudBlob</span></span>
<span data-ttu-id="9f51d-147">Specifica un oggetto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="9f51d-147">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="9f51d-148">Per ottenere un oggetto **CloudBlob** , usa il cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="9f51d-148">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="9f51d-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9f51d-149">-CloudBlobContainer</span></span>
<span data-ttu-id="9f51d-150">Specifica un oggetto **CloudBlobContainer** dalla raccolta client di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9f51d-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="9f51d-151">Questo cmdlet carica il contenuto in un BLOB nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9f51d-151">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="9f51d-152">Per ottenere un oggetto **CloudBlobContainer** , usa il cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="9f51d-152">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="9f51d-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9f51d-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9f51d-154">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="9f51d-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9f51d-155">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="9f51d-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9f51d-156">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="9f51d-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9f51d-157">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="9f51d-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9f51d-158">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="9f51d-158">The default value is 10.</span></span>

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

### <span data-ttu-id="9f51d-159">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="9f51d-159">-Container</span></span>
<span data-ttu-id="9f51d-160">Specifica il nome di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="9f51d-160">Specifies the name of a container.</span></span>
<span data-ttu-id="9f51d-161">Questo cmdlet carica un file in un BLOB nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9f51d-161">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f51d-162">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9f51d-162">-Context</span></span>
<span data-ttu-id="9f51d-163">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9f51d-163">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9f51d-164">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9f51d-164">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="9f51d-165">Per usare un contesto di archiviazione creato da un token SAS senza autorizzazione di lettura, è necessario un parametro Add-Force per ignorare l'esistenza di BLOB di controllo.</span><span class="sxs-lookup"><span data-stu-id="9f51d-165">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="9f51d-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f51d-166">-DefaultProfile</span></span>
<span data-ttu-id="9f51d-167">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f51d-167">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f51d-168">-File</span><span class="sxs-lookup"><span data-stu-id="9f51d-168">-File</span></span>
<span data-ttu-id="9f51d-169">Specifica un percorso di file locale per un file da caricare come contenuto BLOB.</span><span class="sxs-lookup"><span data-stu-id="9f51d-169">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f51d-170">-Force</span><span class="sxs-lookup"><span data-stu-id="9f51d-170">-Force</span></span>
<span data-ttu-id="9f51d-171">Indica che questo cmdlet sovrascrive un BLOB esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9f51d-171">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9f51d-172">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9f51d-172">-Metadata</span></span>
<span data-ttu-id="9f51d-173">Specifica i metadati per il BLOB caricato.</span><span class="sxs-lookup"><span data-stu-id="9f51d-173">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f51d-174">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="9f51d-174">-PremiumPageBlobTier</span></span>
<span data-ttu-id="9f51d-175">Livello BLOB di pagina</span><span class="sxs-lookup"><span data-stu-id="9f51d-175">Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f51d-176">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f51d-176">-Properties</span></span>
<span data-ttu-id="9f51d-177">Specifica le proprietà per il BLOB caricato.</span><span class="sxs-lookup"><span data-stu-id="9f51d-177">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="9f51d-178">Le proprietà supportate sono: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="9f51d-178">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f51d-179">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9f51d-179">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9f51d-180">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="9f51d-180">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9f51d-181">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9f51d-181">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9f51d-182">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="9f51d-182">-StandardBlobTier</span></span>
<span data-ttu-id="9f51d-183">Blocca livello BLOB i valori validi sono hot/cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="9f51d-183">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="9f51d-184">Vedere dettagli in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="9f51d-184">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="9f51d-185">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9f51d-185">-Confirm</span></span>
<span data-ttu-id="9f51d-186">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f51d-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f51d-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f51d-187">-WhatIf</span></span>
<span data-ttu-id="9f51d-188">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f51d-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f51d-189">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f51d-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f51d-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f51d-190">CommonParameters</span></span>
<span data-ttu-id="9f51d-191">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f51d-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f51d-192">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f51d-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f51d-193">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f51d-193">INPUTS</span></span>

### <span data-ttu-id="9f51d-194">System. String</span><span class="sxs-lookup"><span data-stu-id="9f51d-194">System.String</span></span>

### <span data-ttu-id="9f51d-195">Microsoft. Azure. storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9f51d-195">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="9f51d-196">Microsoft. Azure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9f51d-196">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="9f51d-197">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9f51d-197">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9f51d-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f51d-198">OUTPUTS</span></span>

### <span data-ttu-id="9f51d-199">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9f51d-199">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="9f51d-200">Note</span><span class="sxs-lookup"><span data-stu-id="9f51d-200">NOTES</span></span>

## <span data-ttu-id="9f51d-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f51d-201">RELATED LINKS</span></span>

[<span data-ttu-id="9f51d-202">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9f51d-202">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="9f51d-203">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9f51d-203">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="9f51d-204">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9f51d-204">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
