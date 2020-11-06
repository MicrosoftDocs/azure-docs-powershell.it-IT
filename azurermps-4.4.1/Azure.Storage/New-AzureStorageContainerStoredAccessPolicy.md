---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3429c142ce31f8cd08786e180b6725130501ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511435"
---
# <span data-ttu-id="3b105-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b105-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="3b105-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b105-102">SYNOPSIS</span></span>
<span data-ttu-id="3b105-103">Crea un criterio di accesso archiviato per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b105-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b105-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b105-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b105-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b105-105">DESCRIPTION</span></span>
<span data-ttu-id="3b105-106">Il cmdlet **New-AzureStorageContainerStoredAccessPolicy** crea un criterio di accesso archiviato per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b105-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="3b105-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b105-107">EXAMPLES</span></span>

### <span data-ttu-id="3b105-108">Esempio 1: creare un criterio di accesso archiviato in un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3b105-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="3b105-109">Questo comando crea un criterio di accesso denominato Policy01 nel contenitore di archiviazione denominato concontainer.</span><span class="sxs-lookup"><span data-stu-id="3b105-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="3b105-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b105-110">PARAMETERS</span></span>

### <span data-ttu-id="3b105-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3b105-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3b105-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="3b105-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3b105-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="3b105-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3b105-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="3b105-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3b105-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3b105-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3b105-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="3b105-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3b105-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="3b105-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3b105-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="3b105-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3b105-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="3b105-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3b105-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="3b105-120">The default value is 10.</span></span>

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

### <span data-ttu-id="3b105-121">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="3b105-121">-Container</span></span>
<span data-ttu-id="3b105-122">Specifica il nome del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b105-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="3b105-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3b105-123">-Context</span></span>
<span data-ttu-id="3b105-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b105-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3b105-125">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3b105-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3b105-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3b105-126">-ExpiryTime</span></span>
<span data-ttu-id="3b105-127">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="3b105-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="3b105-128">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="3b105-128">-Permission</span></span>
<span data-ttu-id="3b105-129">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere al contenitore.</span><span class="sxs-lookup"><span data-stu-id="3b105-129">Specifies permissions in the stored access policy to access the container.</span></span>

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

### <span data-ttu-id="3b105-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="3b105-130">-Policy</span></span>
<span data-ttu-id="3b105-131">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS.</span><span class="sxs-lookup"><span data-stu-id="3b105-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="3b105-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3b105-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3b105-133">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="3b105-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3b105-134">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="3b105-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3b105-135">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="3b105-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3b105-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3b105-136">-StartTime</span></span>
<span data-ttu-id="3b105-137">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="3b105-137">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="3b105-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b105-138">CommonParameters</span></span>
<span data-ttu-id="3b105-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b105-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b105-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b105-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b105-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b105-141">INPUTS</span></span>

### <span data-ttu-id="3b105-142">Stringa</span><span class="sxs-lookup"><span data-stu-id="3b105-142">String</span></span>

<span data-ttu-id="3b105-143">Il parametro "container" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3b105-143">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="3b105-144">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b105-144">IStorageContext</span></span>

<span data-ttu-id="3b105-145">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3b105-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="3b105-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b105-146">OUTPUTS</span></span>

### <span data-ttu-id="3b105-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3b105-147">System.String</span></span>

## <span data-ttu-id="3b105-148">Note</span><span class="sxs-lookup"><span data-stu-id="3b105-148">NOTES</span></span>

## <span data-ttu-id="3b105-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b105-149">RELATED LINKS</span></span>

[<span data-ttu-id="3b105-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b105-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="3b105-151">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b105-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3b105-152">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b105-152">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="3b105-153">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b105-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


