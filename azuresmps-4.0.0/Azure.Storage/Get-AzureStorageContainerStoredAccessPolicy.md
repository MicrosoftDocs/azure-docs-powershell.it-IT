---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e9ea56c53d73b9c71d2eade4fec7025466ed82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507072"
---
# <span data-ttu-id="ca07c-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca07c-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="ca07c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca07c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca07c-103">Ottiene i criteri di accesso archiviati o i criteri per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca07c-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="ca07c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca07c-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ca07c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca07c-105">DESCRIPTION</span></span>
<span data-ttu-id="ca07c-106">Il cmdlet **Get-AzureStorageContainerStoredAccessPolicy** elenca i criteri di accesso archiviati o i criteri per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca07c-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="ca07c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca07c-107">EXAMPLES</span></span>

### <span data-ttu-id="ca07c-108">Esempio 1: ottenere un criterio di accesso archiviato in un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ca07c-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="ca07c-109">Questo comando consente di ottenere i criteri di accesso denominati Policy22 nel contenitore di archiviazione denominato Container07.</span><span class="sxs-lookup"><span data-stu-id="ca07c-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="ca07c-110">Esempio 2: ottenere tutti i criteri di accesso archiviati in un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ca07c-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="ca07c-111">Questo comando consente di ottenere tutti i criteri di accesso nel contenitore di archiviazione denominato Container07.</span><span class="sxs-lookup"><span data-stu-id="ca07c-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="ca07c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca07c-112">PARAMETERS</span></span>

### <span data-ttu-id="ca07c-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ca07c-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ca07c-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="ca07c-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ca07c-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ca07c-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ca07c-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ca07c-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ca07c-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ca07c-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ca07c-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="ca07c-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ca07c-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="ca07c-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ca07c-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="ca07c-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ca07c-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ca07c-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ca07c-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="ca07c-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ca07c-123">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="ca07c-123">-Container</span></span>
<span data-ttu-id="ca07c-124">Specifica il nome del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca07c-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="ca07c-125">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ca07c-125">-Context</span></span>
<span data-ttu-id="ca07c-126">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca07c-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="ca07c-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="ca07c-127">-Policy</span></span>
<span data-ttu-id="ca07c-128">Specifica i criteri di accesso archiviati di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca07c-128">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="ca07c-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ca07c-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ca07c-130">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="ca07c-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ca07c-131">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ca07c-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ca07c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca07c-132">CommonParameters</span></span>
<span data-ttu-id="ca07c-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca07c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca07c-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca07c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca07c-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca07c-135">INPUTS</span></span>

## <span data-ttu-id="ca07c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca07c-136">OUTPUTS</span></span>

## <span data-ttu-id="ca07c-137">Note</span><span class="sxs-lookup"><span data-stu-id="ca07c-137">NOTES</span></span>

## <span data-ttu-id="ca07c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca07c-138">RELATED LINKS</span></span>

[<span data-ttu-id="ca07c-139">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca07c-139">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ca07c-140">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca07c-140">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ca07c-141">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca07c-141">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


