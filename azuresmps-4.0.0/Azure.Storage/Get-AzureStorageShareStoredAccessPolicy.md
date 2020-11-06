---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc7268d3d7d233f6a3fafeb92540e23ae3eaa6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507036"
---
# <span data-ttu-id="1148c-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1148c-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="1148c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1148c-102">SYNOPSIS</span></span>
<span data-ttu-id="1148c-103">Ottiene i criteri di accesso archiviati per una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1148c-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="1148c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1148c-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="1148c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1148c-105">DESCRIPTION</span></span>
<span data-ttu-id="1148c-106">Il cmdlet **Get-AzureStorageShareStoredAccessPolicy** ottiene i criteri di accesso archiviati per una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1148c-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="1148c-107">Per ottenere un criterio specifico, specificarlo per nome.</span><span class="sxs-lookup"><span data-stu-id="1148c-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="1148c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1148c-108">EXAMPLES</span></span>

### <span data-ttu-id="1148c-109">Esempio 1: ottenere un criterio di accesso archiviato in una condivisione</span><span class="sxs-lookup"><span data-stu-id="1148c-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="1148c-110">Questo comando ottiene un criterio di accesso archiviato denominato GeneralPolicy in ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="1148c-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="1148c-111">Esempio 2: ottenere tutti i criteri di accesso archiviati in Condividi</span><span class="sxs-lookup"><span data-stu-id="1148c-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="1148c-112">Questo comando ottiene tutti i criteri di accesso archiviati in ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="1148c-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="1148c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1148c-113">PARAMETERS</span></span>

### <span data-ttu-id="1148c-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1148c-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1148c-115">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="1148c-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1148c-116">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="1148c-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1148c-117">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="1148c-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1148c-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1148c-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1148c-119">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="1148c-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1148c-120">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="1148c-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1148c-121">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="1148c-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1148c-122">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="1148c-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1148c-123">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="1148c-123">The default value is 10.</span></span>

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

### <span data-ttu-id="1148c-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1148c-124">-Context</span></span>
<span data-ttu-id="1148c-125">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1148c-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="1148c-126">Per ottenere un contesto, usa il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="1148c-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1148c-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="1148c-127">-Policy</span></span>
<span data-ttu-id="1148c-128">Specifica il nome dei criteri di accesso archiviati ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1148c-128">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1148c-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1148c-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1148c-130">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="1148c-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1148c-131">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1148c-131">-ShareName</span></span>
<span data-ttu-id="1148c-132">Specifica il nome della condivisione di archiviazione per cui questo cmdlet ottiene i criteri.</span><span class="sxs-lookup"><span data-stu-id="1148c-132">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1148c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1148c-133">CommonParameters</span></span>
<span data-ttu-id="1148c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1148c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1148c-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1148c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1148c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1148c-136">INPUTS</span></span>

## <span data-ttu-id="1148c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1148c-137">OUTPUTS</span></span>

## <span data-ttu-id="1148c-138">Note</span><span class="sxs-lookup"><span data-stu-id="1148c-138">NOTES</span></span>

## <span data-ttu-id="1148c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1148c-139">RELATED LINKS</span></span>

[<span data-ttu-id="1148c-140">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1148c-140">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1148c-141">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1148c-141">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="1148c-142">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1148c-142">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="1148c-143">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1148c-143">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
