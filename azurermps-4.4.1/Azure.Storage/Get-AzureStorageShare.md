---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 65ba11bcbe26ce91ce4c9ff2f84dc0cff30e125c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508899"
---
# <span data-ttu-id="bcec1-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bcec1-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="bcec1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcec1-102">SYNOPSIS</span></span>
<span data-ttu-id="bcec1-103">Ottiene un elenco di condivisioni file.</span><span class="sxs-lookup"><span data-stu-id="bcec1-103">Gets a list of file shares.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcec1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcec1-104">SYNTAX</span></span>

### <span data-ttu-id="bcec1-105">MatchingPrefix (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bcec1-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="bcec1-106">Specifico</span><span class="sxs-lookup"><span data-stu-id="bcec1-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="bcec1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcec1-107">DESCRIPTION</span></span>
<span data-ttu-id="bcec1-108">Il cmdlet **Get-AzureStorageShare** ottiene un elenco di condivisioni di file per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bcec1-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="bcec1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcec1-109">EXAMPLES</span></span>

### <span data-ttu-id="bcec1-110">Esempio 1: ottenere una condivisione file</span><span class="sxs-lookup"><span data-stu-id="bcec1-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="bcec1-111">Questo comando consente di ottenere la condivisione di file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="bcec1-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="bcec1-112">Esempio 2: ottenere tutte le condivisioni di file che iniziano con una stringa</span><span class="sxs-lookup"><span data-stu-id="bcec1-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="bcec1-113">Questo comando consente di ottenere tutte le condivisioni file con nomi che iniziano con contoso.</span><span class="sxs-lookup"><span data-stu-id="bcec1-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="bcec1-114">Esempio 3: ottenere tutte le condivisioni di file in un contesto specificato</span><span class="sxs-lookup"><span data-stu-id="bcec1-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="bcec1-115">Il primo comando usa il cmdlet **New-AzureStorageContext** per creare un contesto usando il parametro *local* e quindi archivia tale oggetto Context nella variabile $context.</span><span class="sxs-lookup"><span data-stu-id="bcec1-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>

<span data-ttu-id="bcec1-116">Il secondo comando consente di ottenere le condivisioni file per l'oggetto context archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="bcec1-116">The second command gets the file shares for the context object stored in $Context.</span></span>

## <span data-ttu-id="bcec1-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcec1-117">PARAMETERS</span></span>

### <span data-ttu-id="bcec1-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bcec1-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bcec1-119">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="bcec1-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bcec1-120">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="bcec1-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bcec1-121">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="bcec1-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bcec1-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bcec1-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bcec1-123">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="bcec1-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bcec1-124">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="bcec1-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bcec1-125">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="bcec1-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bcec1-126">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="bcec1-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bcec1-127">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="bcec1-127">The default value is 10.</span></span>

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

### <span data-ttu-id="bcec1-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bcec1-128">-Context</span></span>
<span data-ttu-id="bcec1-129">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bcec1-129">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="bcec1-130">Per ottenere un contesto, usa il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="bcec1-130">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="bcec1-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcec1-131">-Name</span></span>
<span data-ttu-id="bcec1-132">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="bcec1-132">Specifies the name of the file share.</span></span>
<span data-ttu-id="bcec1-133">Questo cmdlet ottiene la condivisione di file specificata da questo parametro oppure Nothing se si specifica il nome di una condivisione file che non esiste.</span><span class="sxs-lookup"><span data-stu-id="bcec1-133">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

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

### <span data-ttu-id="bcec1-134">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="bcec1-134">-Prefix</span></span>
<span data-ttu-id="bcec1-135">Specifica il prefisso per le condivisioni file.</span><span class="sxs-lookup"><span data-stu-id="bcec1-135">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="bcec1-136">Questo cmdlet ottiene le condivisioni di file che corrispondono al prefisso specificato da questo parametro oppure non condivide file se nessuna delle condivisioni file corrisponde al prefisso indicato.</span><span class="sxs-lookup"><span data-stu-id="bcec1-136">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

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

### <span data-ttu-id="bcec1-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bcec1-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bcec1-138">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="bcec1-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bcec1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcec1-139">CommonParameters</span></span>
<span data-ttu-id="bcec1-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcec1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcec1-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcec1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcec1-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcec1-142">INPUTS</span></span>

### <span data-ttu-id="bcec1-143">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bcec1-143">IStorageContext</span></span>

<span data-ttu-id="bcec1-144">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bcec1-144">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="bcec1-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcec1-145">OUTPUTS</span></span>

## <span data-ttu-id="bcec1-146">Note</span><span class="sxs-lookup"><span data-stu-id="bcec1-146">NOTES</span></span>

## <span data-ttu-id="bcec1-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcec1-147">RELATED LINKS</span></span>

[<span data-ttu-id="bcec1-148">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bcec1-148">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="bcec1-149">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bcec1-149">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
