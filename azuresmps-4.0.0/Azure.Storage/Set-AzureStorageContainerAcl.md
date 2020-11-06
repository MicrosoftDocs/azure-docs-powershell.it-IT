---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa33f6ba457ad51504cc9005f70f0e4c8f529359
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507171"
---
# <span data-ttu-id="e13a5-101">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="e13a5-101">Set-AzureStorageContainerAcl</span></span>

## <span data-ttu-id="e13a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e13a5-102">SYNOPSIS</span></span>
<span data-ttu-id="e13a5-103">Imposta l'autorizzazione di accesso pubblico per un contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e13a5-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="e13a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e13a5-104">SYNTAX</span></span>

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e13a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e13a5-105">DESCRIPTION</span></span>
<span data-ttu-id="e13a5-106">Il cmdlet **set-AzureStorageContainerAcl** imposta l'autorizzazione di accesso pubblico sul contenitore di archiviazione specificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="e13a5-106">The **Set-AzureStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="e13a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e13a5-107">EXAMPLES</span></span>

### <span data-ttu-id="e13a5-108">Esempio 1: impostare l'ACL del contenitore di archiviazione di Azure per nome</span><span class="sxs-lookup"><span data-stu-id="e13a5-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="e13a5-109">Questo comando crea un contenitore che non ha accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="e13a5-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="e13a5-110">Esempio 2: impostare l'ACL del contenitore di archiviazione di Azure usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="e13a5-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="e13a5-111">Questo comando consente di ottenere tutti i contenitori di archiviazione il cui nome inizia con container e quindi passa il risultato sulla pipeline per impostare l'autorizzazione per tutti per l'accesso BLOB.</span><span class="sxs-lookup"><span data-stu-id="e13a5-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="e13a5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e13a5-112">PARAMETERS</span></span>

### <span data-ttu-id="e13a5-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e13a5-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e13a5-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="e13a5-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e13a5-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e13a5-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e13a5-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e13a5-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e13a5-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e13a5-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e13a5-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="e13a5-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e13a5-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="e13a5-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e13a5-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="e13a5-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e13a5-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="e13a5-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e13a5-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="e13a5-122">The default value is 10.</span></span>

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

### <span data-ttu-id="e13a5-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e13a5-123">-Context</span></span>
<span data-ttu-id="e13a5-124">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e13a5-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e13a5-125">Puoi crearlo usando il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e13a5-125">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e13a5-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="e13a5-126">-Name</span></span>
<span data-ttu-id="e13a5-127">Specifica un nome di contenitore.</span><span class="sxs-lookup"><span data-stu-id="e13a5-127">Specifies a container name.</span></span>

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

### <span data-ttu-id="e13a5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e13a5-128">-PassThru</span></span>
<span data-ttu-id="e13a5-129">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e13a5-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e13a5-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e13a5-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e13a5-131">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="e13a5-131">-Permission</span></span>
<span data-ttu-id="e13a5-132">Specifica il livello di accesso pubblico al contenitore.</span><span class="sxs-lookup"><span data-stu-id="e13a5-132">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="e13a5-133">Per impostazione predefinita, è possibile accedere al contenitore e a qualsiasi BLOB in esso solo dal proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e13a5-133">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="e13a5-134">Per concedere agli utenti anonimi le autorizzazioni di lettura per un contenitore e i relativi BLOB, è possibile impostare le autorizzazioni del contenitore per consentire l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="e13a5-134">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="e13a5-135">Gli utenti anonimi possono leggere i BLOB in un contenitore disponibile pubblicamente senza autenticazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="e13a5-135">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="e13a5-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e13a5-136">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="e13a5-137">--Container.</span><span class="sxs-lookup"><span data-stu-id="e13a5-137">--Container.</span></span>
<span data-ttu-id="e13a5-138">Fornisce l'accesso in lettura completo a un contenitore e ai relativi BLOB.</span><span class="sxs-lookup"><span data-stu-id="e13a5-138">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="e13a5-139">I client possono enumerare i BLOB nel contenitore tramite una richiesta anonima, ma non possono enumerare i contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e13a5-139">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="e13a5-140">--BLOB.</span><span class="sxs-lookup"><span data-stu-id="e13a5-140">--Blob.</span></span>
<span data-ttu-id="e13a5-141">Fornisce l'accesso in lettura ai dati BLOB in un contenitore tramite una richiesta anonima, ma non consente l'accesso ai dati del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e13a5-141">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="e13a5-142">I client non possono enumerare i BLOB nel contenitore usando la richiesta anonima.</span><span class="sxs-lookup"><span data-stu-id="e13a5-142">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="e13a5-143">--Off.</span><span class="sxs-lookup"><span data-stu-id="e13a5-143">--Off.</span></span>
<span data-ttu-id="e13a5-144">Limita l'accesso solo al proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e13a5-144">Restricts access to only the storage account owner.</span></span>

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e13a5-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e13a5-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e13a5-146">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="e13a5-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="e13a5-147">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e13a5-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="e13a5-148">Timeout lato server per ogni richiesta.</span><span class="sxs-lookup"><span data-stu-id="e13a5-148">Server side time out for each request.</span></span>

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

### <span data-ttu-id="e13a5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e13a5-149">CommonParameters</span></span>
<span data-ttu-id="e13a5-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e13a5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e13a5-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e13a5-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e13a5-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e13a5-152">INPUTS</span></span>

## <span data-ttu-id="e13a5-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e13a5-153">OUTPUTS</span></span>

## <span data-ttu-id="e13a5-154">Note</span><span class="sxs-lookup"><span data-stu-id="e13a5-154">NOTES</span></span>

## <span data-ttu-id="e13a5-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e13a5-155">RELATED LINKS</span></span>

[<span data-ttu-id="e13a5-156">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e13a5-156">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="e13a5-157">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e13a5-157">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="e13a5-158">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e13a5-158">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)


