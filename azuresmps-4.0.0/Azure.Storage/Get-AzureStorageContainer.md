---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66845678619a7777bbda9257aa208393b0fa178c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507076"
---
# <span data-ttu-id="2989a-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2989a-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="2989a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2989a-102">SYNOPSIS</span></span>
<span data-ttu-id="2989a-103">Elenca i contenitori di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2989a-103">Lists the storage containers.</span></span>

## <span data-ttu-id="2989a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2989a-104">SYNTAX</span></span>

### <span data-ttu-id="2989a-105">ContainerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2989a-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2989a-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="2989a-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2989a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2989a-107">DESCRIPTION</span></span>
<span data-ttu-id="2989a-108">Il cmdlet **Get-AzureStorageContainer** elenca i contenitori di archiviazione associati all'account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="2989a-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="2989a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2989a-109">EXAMPLES</span></span>

### <span data-ttu-id="2989a-110">Esempio 1: ottenere BLOB di archiviazione di Azure per nome</span><span class="sxs-lookup"><span data-stu-id="2989a-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="2989a-111">Questo esempio usa un carattere jolly per restituire un elenco di tutti i contenitori con un nome che inizia con container.</span><span class="sxs-lookup"><span data-stu-id="2989a-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="2989a-112">Esempio 2: ottenere il contenitore di archiviazione Azure in base al prefisso del nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="2989a-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="2989a-113">Questo esempio usa il parametro *Prefix* per restituire un elenco di tutti i contenitori con un nome che inizia con container.</span><span class="sxs-lookup"><span data-stu-id="2989a-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="2989a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2989a-114">PARAMETERS</span></span>

### <span data-ttu-id="2989a-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2989a-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2989a-116">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="2989a-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2989a-117">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="2989a-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2989a-118">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="2989a-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2989a-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2989a-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2989a-120">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="2989a-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2989a-121">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="2989a-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2989a-122">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="2989a-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2989a-123">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="2989a-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2989a-124">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="2989a-124">The default value is 10.</span></span>

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

### <span data-ttu-id="2989a-125">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2989a-125">-Context</span></span>
<span data-ttu-id="2989a-126">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2989a-126">Specifies the storage context.</span></span>
<span data-ttu-id="2989a-127">Per crearlo, puoi usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2989a-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2989a-128">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="2989a-128">-ContinuationToken</span></span>
<span data-ttu-id="2989a-129">Specifica un token di continuazione per l'elenco di BLOB.</span><span class="sxs-lookup"><span data-stu-id="2989a-129">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2989a-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2989a-130">-MaxCount</span></span>
<span data-ttu-id="2989a-131">Specifica il numero massimo di oggetti restituiti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2989a-131">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="2989a-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="2989a-132">-Name</span></span>
<span data-ttu-id="2989a-133">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="2989a-133">Specifies the container name.</span></span>
<span data-ttu-id="2989a-134">Se il nome del contenitore è vuoto, il cmdlet elenca tutti i contenitori.</span><span class="sxs-lookup"><span data-stu-id="2989a-134">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="2989a-135">In caso contrario, elenca tutti i contenitori che corrispondono al nome specificato o al modello di nome normale.</span><span class="sxs-lookup"><span data-stu-id="2989a-135">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2989a-136">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="2989a-136">-Prefix</span></span>
<span data-ttu-id="2989a-137">Specifica un prefisso usato nel nome del contenitore o dei contenitori che vuoi ottenere.</span><span class="sxs-lookup"><span data-stu-id="2989a-137">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="2989a-138">Puoi usare questa procedura per trovare tutti i contenitori che iniziano con la stessa stringa, ad esempio "My" o "test".</span><span class="sxs-lookup"><span data-stu-id="2989a-138">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: String
Parameter Sets: ContainerPrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2989a-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2989a-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2989a-140">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="2989a-140">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2989a-141">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="2989a-141">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2989a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2989a-142">CommonParameters</span></span>
<span data-ttu-id="2989a-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2989a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2989a-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2989a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2989a-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2989a-145">INPUTS</span></span>

## <span data-ttu-id="2989a-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2989a-146">OUTPUTS</span></span>

## <span data-ttu-id="2989a-147">Note</span><span class="sxs-lookup"><span data-stu-id="2989a-147">NOTES</span></span>

## <span data-ttu-id="2989a-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2989a-148">RELATED LINKS</span></span>

[<span data-ttu-id="2989a-149">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2989a-149">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="2989a-150">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2989a-150">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="2989a-151">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="2989a-151">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)

