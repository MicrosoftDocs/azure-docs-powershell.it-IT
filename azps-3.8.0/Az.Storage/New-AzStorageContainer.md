---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: b056504786d641d137d5188ed529eecb0ede690f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020563"
---
# <span data-ttu-id="a7a70-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7a70-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="a7a70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7a70-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a70-103">Crea un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7a70-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="a7a70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7a70-104">SYNTAX</span></span>

```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a7a70-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7a70-105">DESCRIPTION</span></span>
<span data-ttu-id="a7a70-106">Il cmdlet **New-AzStorageContainer** crea un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7a70-106">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="a7a70-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7a70-107">EXAMPLES</span></span>

### <span data-ttu-id="a7a70-108">Esempio 1: creare un contenitore di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="a7a70-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="a7a70-109">Questo comando crea un contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a7a70-109">This command creates a storage container.</span></span>

### <span data-ttu-id="a7a70-110">Esempio 2: creare più contenitori di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="a7a70-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="a7a70-111">Questo esempio crea più contenitori di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a7a70-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="a7a70-112">Usa il metodo **Split** della classe **String** .NET e quindi passa i nomi sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="a7a70-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="a7a70-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7a70-113">PARAMETERS</span></span>

### <span data-ttu-id="a7a70-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a7a70-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a7a70-115">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="a7a70-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a7a70-116">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a7a70-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a7a70-117">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="a7a70-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a7a70-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a7a70-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a7a70-119">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="a7a70-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a7a70-120">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="a7a70-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a7a70-121">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="a7a70-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a7a70-122">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="a7a70-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a7a70-123">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="a7a70-123">The default value is 10.</span></span>

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

### <span data-ttu-id="a7a70-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="a7a70-124">-Context</span></span>
<span data-ttu-id="a7a70-125">Specifica un contesto per il nuovo contenitore.</span><span class="sxs-lookup"><span data-stu-id="a7a70-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="a7a70-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a70-126">-DefaultProfile</span></span>
<span data-ttu-id="a7a70-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7a70-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7a70-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7a70-128">-Name</span></span>
<span data-ttu-id="a7a70-129">Specifica un nome per il nuovo contenitore.</span><span class="sxs-lookup"><span data-stu-id="a7a70-129">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="a7a70-130">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="a7a70-130">-Permission</span></span>
<span data-ttu-id="a7a70-131">Specifica il livello di accesso pubblico al contenitore.</span><span class="sxs-lookup"><span data-stu-id="a7a70-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="a7a70-132">Per impostazione predefinita, è possibile accedere al contenitore e a qualsiasi BLOB in esso solo dal proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a7a70-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="a7a70-133">Per concedere agli utenti anonimi le autorizzazioni di lettura per un contenitore e i relativi BLOB, è possibile impostare le autorizzazioni del contenitore per consentire l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="a7a70-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="a7a70-134">Gli utenti anonimi possono leggere i BLOB in un contenitore disponibile pubblicamente senza autenticazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="a7a70-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="a7a70-135">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7a70-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a7a70-136">Contenitore.</span><span class="sxs-lookup"><span data-stu-id="a7a70-136">Container.</span></span>
<span data-ttu-id="a7a70-137">Fornisce l'accesso in lettura completo a un contenitore e ai relativi BLOB.</span><span class="sxs-lookup"><span data-stu-id="a7a70-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="a7a70-138">I client possono enumerare i BLOB nel contenitore tramite una richiesta anonima, ma non possono enumerare i contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a7a70-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="a7a70-139">BLOB.</span><span class="sxs-lookup"><span data-stu-id="a7a70-139">Blob.</span></span>
<span data-ttu-id="a7a70-140">Fornisce l'accesso in lettura ai dati BLOB in un contenitore tramite una richiesta anonima, ma non consente l'accesso ai dati del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a7a70-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="a7a70-141">I client non possono enumerare i BLOB nel contenitore usando la richiesta anonima.</span><span class="sxs-lookup"><span data-stu-id="a7a70-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="a7a70-142">Disattivare.</span><span class="sxs-lookup"><span data-stu-id="a7a70-142">Off.</span></span>
<span data-ttu-id="a7a70-143">Che limita l'accesso solo al proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a7a70-143">Which restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="a7a70-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a7a70-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a7a70-145">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="a7a70-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a7a70-146">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="a7a70-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a7a70-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a70-147">CommonParameters</span></span>
<span data-ttu-id="a7a70-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7a70-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a70-149">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a70-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a70-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7a70-150">INPUTS</span></span>

### <span data-ttu-id="a7a70-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a7a70-151">System.String</span></span>

### <span data-ttu-id="a7a70-152">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a7a70-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a7a70-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7a70-153">OUTPUTS</span></span>

### <span data-ttu-id="a7a70-154">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7a70-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="a7a70-155">Note</span><span class="sxs-lookup"><span data-stu-id="a7a70-155">NOTES</span></span>

## <span data-ttu-id="a7a70-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7a70-156">RELATED LINKS</span></span>

[<span data-ttu-id="a7a70-157">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7a70-157">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="a7a70-158">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7a70-158">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="a7a70-159">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="a7a70-159">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


