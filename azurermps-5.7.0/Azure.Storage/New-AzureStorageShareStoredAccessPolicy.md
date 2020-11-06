---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2eaa58523ef71d90aa7ef6566d18c050fe16a51f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515871"
---
# <span data-ttu-id="93ca8-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="93ca8-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="93ca8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="93ca8-103">Crea un criterio di accesso archiviato in una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="93ca8-103">Creates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93ca8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93ca8-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="93ca8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93ca8-105">DESCRIPTION</span></span>
<span data-ttu-id="93ca8-106">Il cmdlet **New-AzureStorageShareStoredAccessPolicy** crea un criterio di accesso archiviato in una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="93ca8-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="93ca8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93ca8-107">EXAMPLES</span></span>

### <span data-ttu-id="93ca8-108">Esempio 1: creare un criterio di accesso archiviato in una condivisione</span><span class="sxs-lookup"><span data-stu-id="93ca8-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="93ca8-109">Questo comando crea un criterio di accesso archiviato con l'autorizzazione completa in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="93ca8-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="93ca8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93ca8-110">PARAMETERS</span></span>

### <span data-ttu-id="93ca8-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="93ca8-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="93ca8-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="93ca8-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="93ca8-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="93ca8-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="93ca8-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="93ca8-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="93ca8-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="93ca8-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="93ca8-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="93ca8-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="93ca8-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="93ca8-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="93ca8-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="93ca8-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="93ca8-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="93ca8-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="93ca8-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="93ca8-120">The default value is 10.</span></span>

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

### <span data-ttu-id="93ca8-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="93ca8-121">-Context</span></span>
<span data-ttu-id="93ca8-122">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="93ca8-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="93ca8-123">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="93ca8-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="93ca8-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="93ca8-124">-ExpiryTime</span></span>
<span data-ttu-id="93ca8-125">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="93ca8-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="93ca8-126">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="93ca8-126">-Permission</span></span>
<span data-ttu-id="93ca8-127">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla condivisione di archiviazione o ai file sotto di essa.</span><span class="sxs-lookup"><span data-stu-id="93ca8-127">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>

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

### <span data-ttu-id="93ca8-128">-Policy</span><span class="sxs-lookup"><span data-stu-id="93ca8-128">-Policy</span></span>
<span data-ttu-id="93ca8-129">Specifica un nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="93ca8-129">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="93ca8-130">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="93ca8-130">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="93ca8-131">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="93ca8-131">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="93ca8-132">-ShareName</span><span class="sxs-lookup"><span data-stu-id="93ca8-132">-ShareName</span></span>
<span data-ttu-id="93ca8-133">Specifica il nome della condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="93ca8-133">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="93ca8-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="93ca8-134">-StartTime</span></span>
<span data-ttu-id="93ca8-135">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="93ca8-135">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="93ca8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ca8-136">CommonParameters</span></span>
<span data-ttu-id="93ca8-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ca8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ca8-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ca8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ca8-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93ca8-139">INPUTS</span></span>

### <span data-ttu-id="93ca8-140">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="93ca8-140">IStorageContext</span></span>

<span data-ttu-id="93ca8-141">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="93ca8-141">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="93ca8-142">Stringa</span><span class="sxs-lookup"><span data-stu-id="93ca8-142">String</span></span>

<span data-ttu-id="93ca8-143">Il parametro "ShareName" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="93ca8-143">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="93ca8-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93ca8-144">OUTPUTS</span></span>

### <span data-ttu-id="93ca8-145">System. String</span><span class="sxs-lookup"><span data-stu-id="93ca8-145">System.String</span></span>

## <span data-ttu-id="93ca8-146">Note</span><span class="sxs-lookup"><span data-stu-id="93ca8-146">NOTES</span></span>

## <span data-ttu-id="93ca8-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93ca8-147">RELATED LINKS</span></span>

[<span data-ttu-id="93ca8-148">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="93ca8-148">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="93ca8-149">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="93ca8-149">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="93ca8-150">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="93ca8-150">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="93ca8-151">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="93ca8-151">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
