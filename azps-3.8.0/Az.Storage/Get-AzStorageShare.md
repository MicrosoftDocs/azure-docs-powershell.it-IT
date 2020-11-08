---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: d25ebb69521ea1e16dc5ff5103ea64819202e2d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020237"
---
# <span data-ttu-id="0c6d7-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="0c6d7-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="0c6d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6d7-103">Ottiene un elenco di condivisioni file.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="0c6d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c6d7-104">SYNTAX</span></span>

### <span data-ttu-id="0c6d7-105">MatchingPrefix (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c6d7-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c6d7-106">Specifico</span><span class="sxs-lookup"><span data-stu-id="0c6d7-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0c6d7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c6d7-107">DESCRIPTION</span></span>
<span data-ttu-id="0c6d7-108">Il cmdlet **Get-AzStorageShare** ottiene un elenco di condivisioni di file per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="0c6d7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c6d7-109">EXAMPLES</span></span>

### <span data-ttu-id="0c6d7-110">Esempio 1: ottenere una condivisione file</span><span class="sxs-lookup"><span data-stu-id="0c6d7-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="0c6d7-111">Questo comando consente di ottenere la condivisione di file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="0c6d7-112">Esempio 2: ottenere tutte le condivisioni di file che iniziano con una stringa</span><span class="sxs-lookup"><span data-stu-id="0c6d7-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="0c6d7-113">Questo comando consente di ottenere tutte le condivisioni file con nomi che iniziano con contoso.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="0c6d7-114">Esempio 3: ottenere tutte le condivisioni di file in un contesto specificato</span><span class="sxs-lookup"><span data-stu-id="0c6d7-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="0c6d7-115">Il primo comando usa il cmdlet **New-AzStorageContext** per creare un contesto usando il parametro *local* e quindi archivia tale oggetto Context nella variabile $context.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="0c6d7-116">Il secondo comando consente di ottenere le condivisioni file per l'oggetto context archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="0c6d7-117">Esempio 4: ottenere uno snapshot della condivisione file con un nome di condivisione specifico e SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="0c6d7-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="0c6d7-118">Questo comando ottiene uno snapshot della condivisione file con un nome di condivisione specifico e SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="0c6d7-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c6d7-119">PARAMETERS</span></span>

### <span data-ttu-id="0c6d7-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c6d7-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0c6d7-121">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0c6d7-122">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0c6d7-123">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6d7-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0c6d7-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0c6d7-125">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0c6d7-126">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0c6d7-127">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0c6d7-128">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0c6d7-129">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-129">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6d7-130">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0c6d7-130">-Context</span></span>
<span data-ttu-id="0c6d7-131">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="0c6d7-132">Per ottenere un contesto, usa il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="0c6d7-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6d7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6d7-133">-DefaultProfile</span></span>
<span data-ttu-id="0c6d7-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6d7-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c6d7-135">-Name</span></span>
<span data-ttu-id="0c6d7-136">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="0c6d7-137">Questo cmdlet ottiene la condivisione di file specificata da questo parametro oppure Nothing se si specifica il nome di una condivisione file che non esiste.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6d7-138">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="0c6d7-138">-Prefix</span></span>
<span data-ttu-id="0c6d7-139">Specifica il prefisso per le condivisioni file.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="0c6d7-140">Questo cmdlet ottiene le condivisioni di file che corrispondono al prefisso specificato da questo parametro oppure non condivide file se nessuna delle condivisioni file corrisponde al prefisso indicato.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6d7-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c6d7-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0c6d7-142">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-142">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6d7-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="0c6d7-143">-SnapshotTime</span></span>
<span data-ttu-id="0c6d7-144">SnapshotTime dello snapshot della condivisione file da ricevere.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6d7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6d7-145">CommonParameters</span></span>
<span data-ttu-id="0c6d7-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c6d7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6d7-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c6d7-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6d7-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c6d7-148">INPUTS</span></span>

### <span data-ttu-id="0c6d7-149">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0c6d7-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0c6d7-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c6d7-150">OUTPUTS</span></span>

### <span data-ttu-id="0c6d7-151">Microsoft. Azure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="0c6d7-151">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="0c6d7-152">Note</span><span class="sxs-lookup"><span data-stu-id="0c6d7-152">NOTES</span></span>

## <span data-ttu-id="0c6d7-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c6d7-153">RELATED LINKS</span></span>

[<span data-ttu-id="0c6d7-154">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="0c6d7-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="0c6d7-155">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="0c6d7-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
