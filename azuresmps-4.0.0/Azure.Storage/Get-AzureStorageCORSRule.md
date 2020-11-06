---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c65daf144708340649b9f7b1566c5e5f2dd81e45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507080"
---
# <span data-ttu-id="6023d-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6023d-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="6023d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6023d-102">SYNOPSIS</span></span>
<span data-ttu-id="6023d-103">Ottiene le regole di CORS per un tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6023d-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="6023d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6023d-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="6023d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6023d-105">DESCRIPTION</span></span>
<span data-ttu-id="6023d-106">Il cmdlet **Get-AzureStorageCORSRule** ottiene le regole CORS (Cross-Origin Resource Sharing) per un tipo di servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6023d-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="6023d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6023d-107">EXAMPLES</span></span>

### <span data-ttu-id="6023d-108">Esempio 1: ottenere le regole di CORS del servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="6023d-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="6023d-109">Questo comando ottiene le regole CORS per il tipo di servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="6023d-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="6023d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6023d-110">PARAMETERS</span></span>

### <span data-ttu-id="6023d-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6023d-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6023d-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="6023d-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6023d-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="6023d-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6023d-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="6023d-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6023d-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6023d-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6023d-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="6023d-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6023d-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="6023d-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6023d-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="6023d-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6023d-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="6023d-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6023d-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="6023d-120">The default value is 10.</span></span>

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

### <span data-ttu-id="6023d-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="6023d-121">-Context</span></span>
<span data-ttu-id="6023d-122">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6023d-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="6023d-123">Per ottenere un contesto, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6023d-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6023d-124">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6023d-124">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6023d-125">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="6023d-125">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="6023d-126">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6023d-126">-ServiceType</span></span>
<span data-ttu-id="6023d-127">Specifica il tipo di servizio di archiviazione di Azure per cui questo cmdlet ottiene le regole di CORS.</span><span class="sxs-lookup"><span data-stu-id="6023d-127">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="6023d-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6023d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6023d-129">BLOB</span><span class="sxs-lookup"><span data-stu-id="6023d-129">Blob</span></span> 
- <span data-ttu-id="6023d-130">tavolo</span><span class="sxs-lookup"><span data-stu-id="6023d-130">Table</span></span> 
- <span data-ttu-id="6023d-131">Coda</span><span class="sxs-lookup"><span data-stu-id="6023d-131">Queue</span></span> 
- <span data-ttu-id="6023d-132">File</span><span class="sxs-lookup"><span data-stu-id="6023d-132">File</span></span>

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

### <span data-ttu-id="6023d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6023d-133">CommonParameters</span></span>
<span data-ttu-id="6023d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6023d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6023d-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6023d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6023d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6023d-136">INPUTS</span></span>

## <span data-ttu-id="6023d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6023d-137">OUTPUTS</span></span>

###  
<span data-ttu-id="6023d-138">Questo cmdlet restituisce una matrice di oggetti **PSCORSRule** che rappresentano le regole CORS attualmente in un servizio.</span><span class="sxs-lookup"><span data-stu-id="6023d-138">This cmdlet returns an array of **PSCORSRule** objects which represent the CORS rules currently on a service.</span></span>

## <span data-ttu-id="6023d-139">Note</span><span class="sxs-lookup"><span data-stu-id="6023d-139">NOTES</span></span>

## <span data-ttu-id="6023d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6023d-140">RELATED LINKS</span></span>

[<span data-ttu-id="6023d-141">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6023d-141">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="6023d-142">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6023d-142">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


