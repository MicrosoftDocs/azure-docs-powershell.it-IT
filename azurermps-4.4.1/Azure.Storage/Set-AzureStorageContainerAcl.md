---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 8c16d52db3b2a1606cbab5999a8a165466fcdb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520837"
---
# <span data-ttu-id="ec482-101">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="ec482-101">Set-AzureStorageContainerAcl</span></span>

## <span data-ttu-id="ec482-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec482-102">SYNOPSIS</span></span>
<span data-ttu-id="ec482-103">Imposta l'autorizzazione di accesso pubblico per un contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ec482-103">Sets the public access permission to a storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec482-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec482-104">SYNTAX</span></span>

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ec482-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec482-105">DESCRIPTION</span></span>
<span data-ttu-id="ec482-106">Il cmdlet **set-AzureStorageContainerAcl** imposta l'autorizzazione di accesso pubblico sul contenitore di archiviazione specificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="ec482-106">The **Set-AzureStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="ec482-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec482-107">EXAMPLES</span></span>

### <span data-ttu-id="ec482-108">Esempio 1: impostare l'ACL del contenitore di archiviazione di Azure per nome</span><span class="sxs-lookup"><span data-stu-id="ec482-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="ec482-109">Questo comando crea un contenitore che non ha accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="ec482-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="ec482-110">Esempio 2: impostare l'ACL del contenitore di archiviazione di Azure usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="ec482-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="ec482-111">Questo comando consente di ottenere tutti i contenitori di archiviazione il cui nome inizia con container e quindi passa il risultato sulla pipeline per impostare l'autorizzazione per tutti per l'accesso BLOB.</span><span class="sxs-lookup"><span data-stu-id="ec482-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="ec482-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec482-112">PARAMETERS</span></span>

### <span data-ttu-id="ec482-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ec482-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ec482-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="ec482-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ec482-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ec482-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ec482-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ec482-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ec482-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ec482-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ec482-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="ec482-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ec482-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="ec482-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ec482-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="ec482-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ec482-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ec482-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ec482-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="ec482-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ec482-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ec482-123">-Context</span></span>
<span data-ttu-id="ec482-124">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec482-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ec482-125">Puoi crearlo usando il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ec482-125">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ec482-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec482-126">-Name</span></span>
<span data-ttu-id="ec482-127">Specifica un nome di contenitore.</span><span class="sxs-lookup"><span data-stu-id="ec482-127">Specifies a container name.</span></span>

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

### <span data-ttu-id="ec482-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec482-128">-PassThru</span></span>
<span data-ttu-id="ec482-129">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ec482-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ec482-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ec482-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ec482-131">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="ec482-131">-Permission</span></span>
<span data-ttu-id="ec482-132">Specifica il livello di accesso pubblico al contenitore.</span><span class="sxs-lookup"><span data-stu-id="ec482-132">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="ec482-133">Per impostazione predefinita, è possibile accedere al contenitore e a qualsiasi BLOB in esso solo dal proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ec482-133">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="ec482-134">Per concedere agli utenti anonimi le autorizzazioni di lettura per un contenitore e i relativi BLOB, è possibile impostare le autorizzazioni del contenitore per consentire l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="ec482-134">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="ec482-135">Gli utenti anonimi possono leggere i BLOB in un contenitore disponibile pubblicamente senza autenticazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="ec482-135">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="ec482-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ec482-136">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="ec482-137">--Container.</span><span class="sxs-lookup"><span data-stu-id="ec482-137">--Container.</span></span>
<span data-ttu-id="ec482-138">Fornisce l'accesso in lettura completo a un contenitore e ai relativi BLOB.</span><span class="sxs-lookup"><span data-stu-id="ec482-138">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="ec482-139">I client possono enumerare i BLOB nel contenitore tramite una richiesta anonima, ma non possono enumerare i contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ec482-139">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="ec482-140">--BLOB.</span><span class="sxs-lookup"><span data-stu-id="ec482-140">--Blob.</span></span>
<span data-ttu-id="ec482-141">Fornisce l'accesso in lettura ai dati BLOB in un contenitore tramite una richiesta anonima, ma non consente l'accesso ai dati del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ec482-141">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="ec482-142">I client non possono enumerare i BLOB nel contenitore usando la richiesta anonima.</span><span class="sxs-lookup"><span data-stu-id="ec482-142">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="ec482-143">--Off.</span><span class="sxs-lookup"><span data-stu-id="ec482-143">--Off.</span></span>
<span data-ttu-id="ec482-144">Limita l'accesso solo al proprietario dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ec482-144">Restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="ec482-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ec482-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ec482-146">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="ec482-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ec482-147">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ec482-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="ec482-148">Timeout lato server per ogni richiesta.</span><span class="sxs-lookup"><span data-stu-id="ec482-148">Server side time out for each request.</span></span>

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

### <span data-ttu-id="ec482-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec482-149">CommonParameters</span></span>
<span data-ttu-id="ec482-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec482-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec482-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec482-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec482-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec482-152">INPUTS</span></span>

### <span data-ttu-id="ec482-153">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ec482-153">IStorageContext</span></span>

<span data-ttu-id="ec482-154">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ec482-154">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ec482-155">Stringa</span><span class="sxs-lookup"><span data-stu-id="ec482-155">String</span></span>

<span data-ttu-id="ec482-156">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ec482-156">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ec482-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec482-157">OUTPUTS</span></span>

### <span data-ttu-id="ec482-158">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ec482-158">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="ec482-159">Note</span><span class="sxs-lookup"><span data-stu-id="ec482-159">NOTES</span></span>

## <span data-ttu-id="ec482-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec482-160">RELATED LINKS</span></span>

[<span data-ttu-id="ec482-161">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ec482-161">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="ec482-162">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ec482-162">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="ec482-163">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ec482-163">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)


