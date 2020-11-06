---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: ''
schema: 2.0.0
ms.openlocfilehash: d80a8a75082503cf8cde9df7a779ca7f0d7d4b92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507024"
---
# <span data-ttu-id="f7e35-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f7e35-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="f7e35-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7e35-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e35-103">Crea un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f7e35-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="f7e35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7e35-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f7e35-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7e35-105">DESCRIPTION</span></span>
<span data-ttu-id="f7e35-106">Il cmdlet **New-AzureStorageContainer** crea un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f7e35-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="f7e35-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7e35-107">EXAMPLES</span></span>

### <span data-ttu-id="f7e35-108">Esempio 1: creare un contenitore di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="f7e35-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="f7e35-109">Questo comando crea un contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f7e35-109">This command creates a storage container.</span></span>

### <span data-ttu-id="f7e35-110">Esempio 2: creare più contenitori di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="f7e35-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="f7e35-111">Questo esempio crea più contenitori di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f7e35-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="f7e35-112">Usa il metodo **Split** della classe **String** .NET e quindi passa i nomi sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f7e35-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="f7e35-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7e35-113">PARAMETERS</span></span>

### <span data-ttu-id="f7e35-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f7e35-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f7e35-115">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="f7e35-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f7e35-116">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="f7e35-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f7e35-117">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="f7e35-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f7e35-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f7e35-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f7e35-119">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="f7e35-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f7e35-120">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="f7e35-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f7e35-121">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="f7e35-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f7e35-122">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="f7e35-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f7e35-123">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="f7e35-123">The default value is 10.</span></span>

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

### <span data-ttu-id="f7e35-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f7e35-124">-Context</span></span>
<span data-ttu-id="f7e35-125">Specifica un contesto per il nuovo contenitore.</span><span class="sxs-lookup"><span data-stu-id="f7e35-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="f7e35-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7e35-126">-Name</span></span>
<span data-ttu-id="f7e35-127">Specifica un nome per il nuovo contenitore.</span><span class="sxs-lookup"><span data-stu-id="f7e35-127">Specifies a name for the new container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7e35-128">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="f7e35-128">-Permission</span></span>
<span data-ttu-id="f7e35-129">Specifica il livello di accesso pubblico al contenitore.</span><span class="sxs-lookup"><span data-stu-id="f7e35-129">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="f7e35-130">Per impostazione predefinita, è possibile accedere al contenitore e a qualsiasi BLOB in esso solo dal proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f7e35-130">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="f7e35-131">Per concedere agli utenti anonimi le autorizzazioni di lettura per un contenitore e i relativi BLOB, è possibile impostare le autorizzazioni del contenitore per consentire l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="f7e35-131">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="f7e35-132">Gli utenti anonimi possono leggere i BLOB in un contenitore disponibile pubblicamente senza autenticazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="f7e35-132">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="f7e35-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7e35-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7e35-134">Contenitore.</span><span class="sxs-lookup"><span data-stu-id="f7e35-134">Container.</span></span>
<span data-ttu-id="f7e35-135">Fornisce l'accesso in lettura completo a un contenitore e ai relativi BLOB.</span><span class="sxs-lookup"><span data-stu-id="f7e35-135">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="f7e35-136">I client possono enumerare i BLOB nel contenitore tramite una richiesta anonima, ma non possono enumerare i contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f7e35-136">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="f7e35-137">BLOB.</span><span class="sxs-lookup"><span data-stu-id="f7e35-137">Blob.</span></span>
<span data-ttu-id="f7e35-138">Fornisce l'accesso in lettura ai dati BLOB in un contenitore tramite una richiesta anonima, ma non consente l'accesso ai dati del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f7e35-138">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="f7e35-139">I client non possono enumerare i BLOB nel contenitore usando la richiesta anonima.</span><span class="sxs-lookup"><span data-stu-id="f7e35-139">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="f7e35-140">Disattivare.</span><span class="sxs-lookup"><span data-stu-id="f7e35-140">Off.</span></span>
<span data-ttu-id="f7e35-141">Che limita l'accesso solo al proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f7e35-141">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e35-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f7e35-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f7e35-143">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="f7e35-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="f7e35-144">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="f7e35-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="f7e35-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e35-145">CommonParameters</span></span>
<span data-ttu-id="f7e35-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7e35-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e35-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7e35-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e35-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7e35-148">INPUTS</span></span>

## <span data-ttu-id="f7e35-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7e35-149">OUTPUTS</span></span>

## <span data-ttu-id="f7e35-150">Note</span><span class="sxs-lookup"><span data-stu-id="f7e35-150">NOTES</span></span>

## <span data-ttu-id="f7e35-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7e35-151">RELATED LINKS</span></span>

[<span data-ttu-id="f7e35-152">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f7e35-152">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="f7e35-153">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f7e35-153">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="f7e35-154">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="f7e35-154">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


