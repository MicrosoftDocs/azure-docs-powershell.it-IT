---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: faccb7c040b628899746973bcf4c54bb01b8d555
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374020"
---
# <span data-ttu-id="ed92f-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ed92f-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="ed92f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed92f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed92f-103">Crea un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ed92f-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="ed92f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed92f-104">SYNTAX</span></span>

### <span data-ttu-id="ed92f-105">ContainerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed92f-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ed92f-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="ed92f-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ed92f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed92f-107">DESCRIPTION</span></span>
<span data-ttu-id="ed92f-108">Il cmdlet **New-AzStorageContainer** crea un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ed92f-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="ed92f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed92f-109">EXAMPLES</span></span>

### <span data-ttu-id="ed92f-110">Esempio 1: creare un contenitore di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="ed92f-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="ed92f-111">Questo comando crea un contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ed92f-111">This command creates a storage container.</span></span>

### <span data-ttu-id="ed92f-112">Esempio 2: creare più contenitori di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="ed92f-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="ed92f-113">Questo esempio crea più contenitori di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ed92f-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="ed92f-114">Usa il metodo **Split** della classe **String** .NET e quindi passa i nomi sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed92f-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="ed92f-115">Esempio 3: creare un contenitore di archiviazione di Azure con l'ambito di crittografia</span><span class="sxs-lookup"><span data-stu-id="ed92f-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="ed92f-116">Questo comando crea un contenitore di archiviazione con l'ambito di crittografia predefinito come myencryptscope e il caricamento BLOB Prevert con un ambito di crittografia diverso per questo contenitore.</span><span class="sxs-lookup"><span data-stu-id="ed92f-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="ed92f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed92f-117">PARAMETERS</span></span>

### <span data-ttu-id="ed92f-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ed92f-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ed92f-119">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="ed92f-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ed92f-120">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ed92f-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ed92f-121">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ed92f-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ed92f-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ed92f-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ed92f-123">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="ed92f-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ed92f-124">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="ed92f-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ed92f-125">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="ed92f-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ed92f-126">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ed92f-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ed92f-127">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="ed92f-127">The default value is 10.</span></span>

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

### <span data-ttu-id="ed92f-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ed92f-128">-Context</span></span>
<span data-ttu-id="ed92f-129">Specifica un contesto per il nuovo contenitore.</span><span class="sxs-lookup"><span data-stu-id="ed92f-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="ed92f-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="ed92f-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="ed92f-131">Predefinito il contenitore per usare l'ambito di crittografia specificato per tutte le Scritture.</span><span class="sxs-lookup"><span data-stu-id="ed92f-131">Default the container to use specified encryption scope for all writes.</span></span>

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

### <span data-ttu-id="ed92f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed92f-132">-DefaultProfile</span></span>
<span data-ttu-id="ed92f-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed92f-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed92f-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed92f-134">-Name</span></span>
<span data-ttu-id="ed92f-135">Specifica un nome per il nuovo contenitore.</span><span class="sxs-lookup"><span data-stu-id="ed92f-135">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="ed92f-136">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="ed92f-136">-Permission</span></span>
<span data-ttu-id="ed92f-137">Specifica il livello di accesso pubblico al contenitore.</span><span class="sxs-lookup"><span data-stu-id="ed92f-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="ed92f-138">Per impostazione predefinita, è possibile accedere al contenitore e a qualsiasi BLOB in esso solo dal proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ed92f-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="ed92f-139">Per concedere agli utenti anonimi le autorizzazioni di lettura per un contenitore e i relativi BLOB, è possibile impostare le autorizzazioni del contenitore per consentire l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="ed92f-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="ed92f-140">Gli utenti anonimi possono leggere i BLOB in un contenitore disponibile pubblicamente senza autenticazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="ed92f-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="ed92f-141">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ed92f-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed92f-142">Contenitore.</span><span class="sxs-lookup"><span data-stu-id="ed92f-142">Container.</span></span>
<span data-ttu-id="ed92f-143">Fornisce l'accesso in lettura completo a un contenitore e ai relativi BLOB.</span><span class="sxs-lookup"><span data-stu-id="ed92f-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="ed92f-144">I client possono enumerare i BLOB nel contenitore tramite una richiesta anonima, ma non possono enumerare i contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ed92f-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="ed92f-145">BLOB.</span><span class="sxs-lookup"><span data-stu-id="ed92f-145">Blob.</span></span>
<span data-ttu-id="ed92f-146">Fornisce l'accesso in lettura ai dati BLOB in un contenitore tramite una richiesta anonima, ma non consente l'accesso ai dati del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ed92f-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="ed92f-147">I client non possono enumerare i BLOB nel contenitore usando la richiesta anonima.</span><span class="sxs-lookup"><span data-stu-id="ed92f-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="ed92f-148">Disattivare.</span><span class="sxs-lookup"><span data-stu-id="ed92f-148">Off.</span></span>
<span data-ttu-id="ed92f-149">Che limita l'accesso solo al proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ed92f-149">Which restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="ed92f-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="ed92f-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="ed92f-151">Bloccare l'override dell'ambito di crittografia dal contenitore default.</span><span class="sxs-lookup"><span data-stu-id="ed92f-151">Block override of encryption scope from the container default.</span></span>

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

### <span data-ttu-id="ed92f-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ed92f-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ed92f-153">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="ed92f-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ed92f-154">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ed92f-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ed92f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed92f-155">CommonParameters</span></span>
<span data-ttu-id="ed92f-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed92f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed92f-157">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed92f-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed92f-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed92f-158">INPUTS</span></span>

### <span data-ttu-id="ed92f-159">System. String</span><span class="sxs-lookup"><span data-stu-id="ed92f-159">System.String</span></span>

### <span data-ttu-id="ed92f-160">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ed92f-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ed92f-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed92f-161">OUTPUTS</span></span>

### <span data-ttu-id="ed92f-162">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ed92f-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="ed92f-163">Note</span><span class="sxs-lookup"><span data-stu-id="ed92f-163">NOTES</span></span>

## <span data-ttu-id="ed92f-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed92f-164">RELATED LINKS</span></span>

[<span data-ttu-id="ed92f-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ed92f-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="ed92f-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ed92f-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="ed92f-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="ed92f-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


