---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95d5afafbed6ab6e3ba81cbfd509fd7b531217e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685270"
---
# <span data-ttu-id="df16f-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="df16f-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="df16f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df16f-102">SYNOPSIS</span></span>
<span data-ttu-id="df16f-103">Crea un criterio di accesso archiviato per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="df16f-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="df16f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df16f-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="df16f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df16f-105">DESCRIPTION</span></span>
<span data-ttu-id="df16f-106">Il cmdlet **New-AzureStorageContainerStoredAccessPolicy** crea un criterio di accesso archiviato per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="df16f-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="df16f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df16f-107">EXAMPLES</span></span>

### <span data-ttu-id="df16f-108">Esempio 1: creare un criterio di accesso archiviato in un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="df16f-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="df16f-109">Questo comando crea un criterio di accesso denominato Policy01 nel contenitore di archiviazione denominato concontainer.</span><span class="sxs-lookup"><span data-stu-id="df16f-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="df16f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df16f-110">PARAMETERS</span></span>

### <span data-ttu-id="df16f-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="df16f-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="df16f-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="df16f-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="df16f-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="df16f-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="df16f-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="df16f-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="df16f-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="df16f-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="df16f-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="df16f-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="df16f-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="df16f-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="df16f-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="df16f-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="df16f-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="df16f-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="df16f-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="df16f-120">The default value is 10.</span></span>

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

### <span data-ttu-id="df16f-121">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="df16f-121">-Container</span></span>
<span data-ttu-id="df16f-122">Specifica il nome del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="df16f-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="df16f-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="df16f-123">-Context</span></span>
<span data-ttu-id="df16f-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="df16f-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="df16f-125">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="df16f-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="df16f-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="df16f-126">-ExpiryTime</span></span>
<span data-ttu-id="df16f-127">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="df16f-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df16f-128">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="df16f-128">-Permission</span></span>
<span data-ttu-id="df16f-129">Specifica il livello di accesso pubblico al contenitore.</span><span class="sxs-lookup"><span data-stu-id="df16f-129">Specifies the level of public access to this container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df16f-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="df16f-130">-Policy</span></span>
<span data-ttu-id="df16f-131">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS.</span><span class="sxs-lookup"><span data-stu-id="df16f-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df16f-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="df16f-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="df16f-133">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="df16f-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="df16f-134">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="df16f-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="df16f-135">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="df16f-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="df16f-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="df16f-136">-StartTime</span></span>
<span data-ttu-id="df16f-137">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="df16f-137">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df16f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df16f-138">CommonParameters</span></span>
<span data-ttu-id="df16f-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df16f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df16f-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df16f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df16f-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df16f-141">INPUTS</span></span>

## <span data-ttu-id="df16f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df16f-142">OUTPUTS</span></span>

## <span data-ttu-id="df16f-143">Note</span><span class="sxs-lookup"><span data-stu-id="df16f-143">NOTES</span></span>

## <span data-ttu-id="df16f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df16f-144">RELATED LINKS</span></span>

[<span data-ttu-id="df16f-145">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="df16f-145">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="df16f-146">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="df16f-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="df16f-147">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="df16f-147">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="df16f-148">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="df16f-148">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


