---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 5c3475a49c76a9a9617de02519a1f37c29059f31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522011"
---
# <span data-ttu-id="fec85-101">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="fec85-101">Remove-AzureStorageCORSRule</span></span>

## <span data-ttu-id="fec85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fec85-102">SYNOPSIS</span></span>
<span data-ttu-id="fec85-103">Rimuove CORS per un servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fec85-103">Removes CORS for a Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fec85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fec85-104">SYNTAX</span></span>

```
Remove-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="fec85-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fec85-105">DESCRIPTION</span></span>
<span data-ttu-id="fec85-106">Il cmdlet **Remove-AzureStorageCORSRule** rimuove la condivisione di risorse CORS (Cross-Origin Resource Sharing) per un servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fec85-106">The **Remove-AzureStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="fec85-107">Questo cmdlet elimina tutte le regole di CORS in un tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fec85-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="fec85-108">I tipi di servizi di archiviazione per questo cmdlet sono BLOB, Table, Queue e file.</span><span class="sxs-lookup"><span data-stu-id="fec85-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="fec85-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fec85-109">EXAMPLES</span></span>

### <span data-ttu-id="fec85-110">Esempio 1: rimuovere le regole di CORS per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="fec85-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="fec85-111">Questo comando rimuove le regole di CORS per il tipo di servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="fec85-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="fec85-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fec85-112">PARAMETERS</span></span>

### <span data-ttu-id="fec85-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fec85-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fec85-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="fec85-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fec85-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="fec85-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fec85-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="fec85-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fec85-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fec85-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fec85-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="fec85-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fec85-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="fec85-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fec85-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="fec85-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fec85-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="fec85-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fec85-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="fec85-122">The default value is 10.</span></span>

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

### <span data-ttu-id="fec85-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="fec85-123">-Context</span></span>
<span data-ttu-id="fec85-124">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fec85-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="fec85-125">Per ottenere il contesto di archiviazione, il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fec85-125">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fec85-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fec85-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fec85-127">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="fec85-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="fec85-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="fec85-128">-ServiceType</span></span>
<span data-ttu-id="fec85-129">Specifica il tipo di servizio di archiviazione di Azure per cui questo cmdlet rimuove le regole.</span><span class="sxs-lookup"><span data-stu-id="fec85-129">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="fec85-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fec85-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fec85-131">BLOB</span><span class="sxs-lookup"><span data-stu-id="fec85-131">Blob</span></span> 
- <span data-ttu-id="fec85-132">tavolo</span><span class="sxs-lookup"><span data-stu-id="fec85-132">Table</span></span> 
- <span data-ttu-id="fec85-133">Coda</span><span class="sxs-lookup"><span data-stu-id="fec85-133">Queue</span></span> 
- <span data-ttu-id="fec85-134">File</span><span class="sxs-lookup"><span data-stu-id="fec85-134">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec85-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec85-135">CommonParameters</span></span>
<span data-ttu-id="fec85-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec85-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec85-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fec85-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec85-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fec85-138">INPUTS</span></span>

### <span data-ttu-id="fec85-139">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fec85-139">IStorageContext</span></span>

<span data-ttu-id="fec85-140">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fec85-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="fec85-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fec85-141">OUTPUTS</span></span>

## <span data-ttu-id="fec85-142">Note</span><span class="sxs-lookup"><span data-stu-id="fec85-142">NOTES</span></span>

## <span data-ttu-id="fec85-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fec85-143">RELATED LINKS</span></span>

[<span data-ttu-id="fec85-144">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="fec85-144">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="fec85-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="fec85-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


