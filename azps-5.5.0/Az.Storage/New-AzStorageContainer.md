---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: faccb7c040b628899746973bcf4c54bb01b8d555
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198439"
---
# <span data-ttu-id="4c6f4-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4c6f4-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="4c6f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c6f4-102">SYNOPSIS</span></span>
<span data-ttu-id="4c6f4-103">Crea un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="4c6f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c6f4-104">SYNTAX</span></span>

### <span data-ttu-id="4c6f4-105">ContainerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c6f4-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4c6f4-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="4c6f4-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4c6f4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c6f4-107">DESCRIPTION</span></span>
<span data-ttu-id="4c6f4-108">Il cmdlet **New-AzStorageContainer** crea un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="4c6f4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c6f4-109">EXAMPLES</span></span>

### <span data-ttu-id="4c6f4-110">Esempio 1: Creare un contenitore di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="4c6f4-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="4c6f4-111">Questo comando crea un contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-111">This command creates a storage container.</span></span>

### <span data-ttu-id="4c6f4-112">Esempio 2: Creare più contenitori di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="4c6f4-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="4c6f4-113">Questo esempio crea più contenitori di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="4c6f4-114">Usa il **metodo Split** della classe **stringa** .NET e quindi passa i nomi alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="4c6f4-115">Esempio 3: Creare un contenitore di archiviazione di Azure con ambito di crittografia</span><span class="sxs-lookup"><span data-stu-id="4c6f4-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="4c6f4-116">Questo comando crea un contenitore di archiviazione con ambito di crittografia predefinito come myencryptscope e preverte il caricamento BLOB con un ambito di crittografia diverso in questo contenitore.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="4c6f4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c6f4-117">PARAMETERS</span></span>

### <span data-ttu-id="4c6f4-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4c6f4-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4c6f4-119">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4c6f4-120">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4c6f4-121">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4c6f4-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4c6f4-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4c6f4-123">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4c6f4-124">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4c6f4-125">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4c6f4-126">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4c6f4-127">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-127">The default value is 10.</span></span>

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

### <span data-ttu-id="4c6f4-128">-Context</span><span class="sxs-lookup"><span data-stu-id="4c6f4-128">-Context</span></span>
<span data-ttu-id="4c6f4-129">Specifica un contesto per il nuovo contenitore.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="4c6f4-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="4c6f4-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="4c6f4-131">Impostazione predefinita del contenitore da usare con l'ambito di crittografia specificato per tutte le operazioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-131">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6f4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c6f4-132">-DefaultProfile</span></span>
<span data-ttu-id="4c6f4-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c6f4-134">-Name</span><span class="sxs-lookup"><span data-stu-id="4c6f4-134">-Name</span></span>
<span data-ttu-id="4c6f4-135">Specifica un nome per il nuovo contenitore.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-135">Specifies a name for the new container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6f4-136">-Permission</span><span class="sxs-lookup"><span data-stu-id="4c6f4-136">-Permission</span></span>
<span data-ttu-id="4c6f4-137">Specifica il livello di accesso pubblico al contenitore.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="4c6f4-138">Per impostazione predefinita, il contenitore e gli eventuali BLOB in esso contenuti sono accessibili solo al proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="4c6f4-139">Per concedere agli utenti anonimi le autorizzazioni di lettura per un contenitore e i relativi BLOB, è possibile impostare le autorizzazioni del contenitore per abilitare l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="4c6f4-140">Gli utenti anonimi possono leggere i BLOB in un contenitore disponibile pubblicamente senza autenticare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="4c6f4-141">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="4c6f4-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c6f4-142">Contenitore.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-142">Container.</span></span>
<span data-ttu-id="4c6f4-143">Fornisce l'accesso completo in lettura a un contenitore e ai relativi BLOB.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="4c6f4-144">I client possono enumerare i BLOB nel contenitore tramite richiesta anonima, ma non possono enumerare i contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="4c6f4-145">BLOB.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-145">Blob.</span></span>
<span data-ttu-id="4c6f4-146">Fornisce l'accesso in lettura ai dati dei BLOB in tutto un contenitore tramite richiesta anonima, ma non fornisce l'accesso ai dati del contenitore.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="4c6f4-147">I client non possono enumerare i BLOB nel contenitore usando una richiesta anonima.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="4c6f4-148">Disattivato.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-148">Off.</span></span>
<span data-ttu-id="4c6f4-149">In questo modo l'accesso viene limitato solo al proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-149">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6f4-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="4c6f4-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="4c6f4-151">Bloccare l'override dell'ambito di crittografia dal contenitore predefinito.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-151">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6f4-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4c6f4-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4c6f4-153">Specifica l'intervallo di timeout del lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="4c6f4-154">Se prima dell'elaborazione della richiesta da parte del servizio è trascorso l'intervallo specificato, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="4c6f4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c6f4-155">CommonParameters</span></span>
<span data-ttu-id="4c6f4-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c6f4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c6f4-157">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c6f4-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c6f4-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c6f4-158">INPUTS</span></span>

### <span data-ttu-id="4c6f4-159">System.String</span><span class="sxs-lookup"><span data-stu-id="4c6f4-159">System.String</span></span>

### <span data-ttu-id="4c6f4-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4c6f4-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4c6f4-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c6f4-161">OUTPUTS</span></span>

### <span data-ttu-id="4c6f4-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4c6f4-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="4c6f4-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c6f4-163">NOTES</span></span>

## <span data-ttu-id="4c6f4-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c6f4-164">RELATED LINKS</span></span>

[<span data-ttu-id="4c6f4-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4c6f4-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="4c6f4-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4c6f4-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="4c6f4-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="4c6f4-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


