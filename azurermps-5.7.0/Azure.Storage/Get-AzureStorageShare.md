---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
ms.openlocfilehash: c0c3aedf6c92df8b81beed92ef4ea779dd8ff131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515904"
---
# <span data-ttu-id="3af64-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="3af64-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="3af64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3af64-102">SYNOPSIS</span></span>
<span data-ttu-id="3af64-103">Ottiene un elenco di condivisioni file.</span><span class="sxs-lookup"><span data-stu-id="3af64-103">Gets a list of file shares.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3af64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3af64-104">SYNTAX</span></span>

### <span data-ttu-id="3af64-105">MatchingPrefix (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3af64-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3af64-106">Specifico</span><span class="sxs-lookup"><span data-stu-id="3af64-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [-SnapshotTime <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="3af64-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3af64-107">DESCRIPTION</span></span>
<span data-ttu-id="3af64-108">Il cmdlet **Get-AzureStorageShare** ottiene un elenco di condivisioni di file per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3af64-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="3af64-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3af64-109">EXAMPLES</span></span>

### <span data-ttu-id="3af64-110">Esempio 1: ottenere una condivisione file</span><span class="sxs-lookup"><span data-stu-id="3af64-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="3af64-111">Questo comando consente di ottenere la condivisione di file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="3af64-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="3af64-112">Esempio 2: ottenere tutte le condivisioni di file che iniziano con una stringa</span><span class="sxs-lookup"><span data-stu-id="3af64-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="3af64-113">Questo comando consente di ottenere tutte le condivisioni file con nomi che iniziano con contoso.</span><span class="sxs-lookup"><span data-stu-id="3af64-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="3af64-114">Esempio 3: ottenere tutte le condivisioni di file in un contesto specificato</span><span class="sxs-lookup"><span data-stu-id="3af64-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="3af64-115">Il primo comando usa il cmdlet **New-AzureStorageContext** per creare un contesto usando il parametro *local* e quindi archivia tale oggetto Context nella variabile $context.</span><span class="sxs-lookup"><span data-stu-id="3af64-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>

<span data-ttu-id="3af64-116">Il secondo comando consente di ottenere le condivisioni file per l'oggetto context archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="3af64-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="3af64-117">Esempio 4: ottenere uno snapshot della condivisione file con un nome di condivisione specifico e SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="3af64-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="3af64-118">Questo comando ottiene uno snapshot della condivisione file con un nome di condivisione specifico e SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="3af64-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="3af64-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3af64-119">PARAMETERS</span></span>

### <span data-ttu-id="3af64-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3af64-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3af64-121">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="3af64-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3af64-122">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="3af64-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3af64-123">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="3af64-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3af64-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3af64-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3af64-125">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="3af64-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3af64-126">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="3af64-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3af64-127">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="3af64-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3af64-128">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="3af64-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3af64-129">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="3af64-129">The default value is 10.</span></span>

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

### <span data-ttu-id="3af64-130">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3af64-130">-Context</span></span>
<span data-ttu-id="3af64-131">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3af64-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3af64-132">Per ottenere un contesto, usa il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="3af64-132">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="3af64-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="3af64-133">-Name</span></span>
<span data-ttu-id="3af64-134">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3af64-134">Specifies the name of the file share.</span></span>
<span data-ttu-id="3af64-135">Questo cmdlet ottiene la condivisione di file specificata da questo parametro oppure Nothing se si specifica il nome di una condivisione file che non esiste.</span><span class="sxs-lookup"><span data-stu-id="3af64-135">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: String
Parameter Sets: Specific
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af64-136">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="3af64-136">-Prefix</span></span>
<span data-ttu-id="3af64-137">Specifica il prefisso per le condivisioni file.</span><span class="sxs-lookup"><span data-stu-id="3af64-137">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="3af64-138">Questo cmdlet ottiene le condivisioni di file che corrispondono al prefisso specificato da questo parametro oppure non condivide file se nessuna delle condivisioni file corrisponde al prefisso indicato.</span><span class="sxs-lookup"><span data-stu-id="3af64-138">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: String
Parameter Sets: MatchingPrefix
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af64-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3af64-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3af64-140">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="3af64-140">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3af64-141">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="3af64-141">-SnapshotTime</span></span>
<span data-ttu-id="3af64-142">SnapshotTime dello snapshot della condivisione file da ricevere.</span><span class="sxs-lookup"><span data-stu-id="3af64-142">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: Specific
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af64-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af64-143">CommonParameters</span></span>
<span data-ttu-id="3af64-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af64-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af64-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af64-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af64-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3af64-146">INPUTS</span></span>

### <span data-ttu-id="3af64-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3af64-147">IStorageContext</span></span>

<span data-ttu-id="3af64-148">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3af64-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="3af64-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3af64-149">OUTPUTS</span></span>

## <span data-ttu-id="3af64-150">Note</span><span class="sxs-lookup"><span data-stu-id="3af64-150">NOTES</span></span>

## <span data-ttu-id="3af64-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3af64-151">RELATED LINKS</span></span>

[<span data-ttu-id="3af64-152">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="3af64-152">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="3af64-153">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="3af64-153">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
