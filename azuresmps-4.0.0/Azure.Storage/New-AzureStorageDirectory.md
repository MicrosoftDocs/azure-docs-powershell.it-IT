---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bd97057cfafc48b3f1edd8539e7808056599117
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491446"
---
# <span data-ttu-id="30061-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="30061-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="30061-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30061-102">SYNOPSIS</span></span>
<span data-ttu-id="30061-103">Crea una directory.</span><span class="sxs-lookup"><span data-stu-id="30061-103">Creates a directory.</span></span>

## <span data-ttu-id="30061-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30061-104">SYNTAX</span></span>

### <span data-ttu-id="30061-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="30061-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="30061-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="30061-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="30061-107">Directory</span><span class="sxs-lookup"><span data-stu-id="30061-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="30061-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30061-108">DESCRIPTION</span></span>
<span data-ttu-id="30061-109">Il cmdlet **New-AzureStorageDirectory** crea una directory.</span><span class="sxs-lookup"><span data-stu-id="30061-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="30061-110">Questo cmdlet restituisce un oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="30061-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="30061-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30061-111">EXAMPLES</span></span>

### <span data-ttu-id="30061-112">Esempio 1: creare una cartella in una condivisione file</span><span class="sxs-lookup"><span data-stu-id="30061-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="30061-113">Questo comando crea una cartella denominata ContosoWorkingFolder nella condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="30061-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="30061-114">Esempio 2: creare una cartella in una condivisione file specificata in un oggetto condivisione file</span><span class="sxs-lookup"><span data-stu-id="30061-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="30061-115">Questo comando usa il cmdlet **Get-AzureStorageShare** per ottenere la condivisione di file denominata ContosoShare06 e quindi la passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="30061-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="30061-116">Il cmdlet corrente crea la cartella denominata ContosoWorkingFolder in ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="30061-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="30061-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30061-117">PARAMETERS</span></span>

### <span data-ttu-id="30061-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="30061-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="30061-119">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="30061-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="30061-120">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="30061-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="30061-121">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="30061-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="30061-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="30061-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="30061-123">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="30061-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="30061-124">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="30061-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="30061-125">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="30061-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="30061-126">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="30061-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="30061-127">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="30061-127">The default value is 10.</span></span>

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

### <span data-ttu-id="30061-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="30061-128">-Context</span></span>
<span data-ttu-id="30061-129">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="30061-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="30061-130">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="30061-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30061-131">-Directory</span><span class="sxs-lookup"><span data-stu-id="30061-131">-Directory</span></span>
<span data-ttu-id="30061-132">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="30061-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="30061-133">Questo cmdlet crea la cartella nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="30061-133">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="30061-134">Per ottenere una directory, usare il cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="30061-134">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="30061-135">Puoi anche usare il cmdlet Get-AzureStorageFile per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="30061-135">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30061-136">-Path</span><span class="sxs-lookup"><span data-stu-id="30061-136">-Path</span></span>
<span data-ttu-id="30061-137">Specifica il percorso di una cartella.</span><span class="sxs-lookup"><span data-stu-id="30061-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="30061-138">Questo cmdlet crea una cartella per il percorso specificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30061-138">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30061-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="30061-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="30061-140">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="30061-140">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="30061-141">-Condividi</span><span class="sxs-lookup"><span data-stu-id="30061-141">-Share</span></span>
<span data-ttu-id="30061-142">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="30061-142">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="30061-143">Questo cmdlet crea una cartella nella condivisione file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="30061-143">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="30061-144">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="30061-144">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="30061-145">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="30061-145">This object contains the storage context.</span></span>
<span data-ttu-id="30061-146">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="30061-146">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30061-147">-ShareName</span><span class="sxs-lookup"><span data-stu-id="30061-147">-ShareName</span></span>
<span data-ttu-id="30061-148">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="30061-148">Specifies the name of the file share.</span></span>
<span data-ttu-id="30061-149">Questo cmdlet crea una cartella nella condivisione file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="30061-149">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30061-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30061-150">CommonParameters</span></span>
<span data-ttu-id="30061-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30061-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30061-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30061-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30061-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30061-153">INPUTS</span></span>

## <span data-ttu-id="30061-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30061-154">OUTPUTS</span></span>

## <span data-ttu-id="30061-155">Note</span><span class="sxs-lookup"><span data-stu-id="30061-155">NOTES</span></span>

## <span data-ttu-id="30061-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30061-156">RELATED LINKS</span></span>

[<span data-ttu-id="30061-157">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="30061-157">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="30061-158">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="30061-158">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="30061-159">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="30061-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="30061-160">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="30061-160">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="30061-161">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="30061-161">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
