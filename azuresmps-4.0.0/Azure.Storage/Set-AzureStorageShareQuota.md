---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 778c5020dc47bc8db7bda664b2e352045d851dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507164"
---
# <span data-ttu-id="8a664-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="8a664-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="8a664-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a664-102">SYNOPSIS</span></span>
<span data-ttu-id="8a664-103">Imposta la capacità di archiviazione per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="8a664-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="8a664-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a664-104">SYNTAX</span></span>

### <span data-ttu-id="8a664-105">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="8a664-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a664-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="8a664-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8a664-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a664-107">DESCRIPTION</span></span>
<span data-ttu-id="8a664-108">Il cmdlet **set-AzureStorageShareQuota** imposta la capacità di archiviazione per una condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="8a664-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="8a664-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a664-109">EXAMPLES</span></span>

### <span data-ttu-id="8a664-110">Esempio 1: impostare la capacità di archiviazione di una condivisione</span><span class="sxs-lookup"><span data-stu-id="8a664-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="8a664-111">Questo comando imposta la capacità di archiviazione per una condivisione denominata ContosoShare01 in 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="8a664-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="8a664-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a664-112">PARAMETERS</span></span>

### <span data-ttu-id="8a664-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8a664-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8a664-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="8a664-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8a664-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8a664-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8a664-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="8a664-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8a664-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8a664-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8a664-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="8a664-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8a664-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="8a664-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8a664-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="8a664-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8a664-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="8a664-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8a664-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="8a664-122">The default value is 10.</span></span>

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

### <span data-ttu-id="8a664-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8a664-123">-Context</span></span>
<span data-ttu-id="8a664-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8a664-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8a664-125">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="8a664-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8a664-126">-Quota</span><span class="sxs-lookup"><span data-stu-id="8a664-126">-Quota</span></span>
<span data-ttu-id="8a664-127">Specifica il valore di quota in gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="8a664-127">Specifies the quota value in gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a664-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8a664-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8a664-129">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="8a664-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8a664-130">-Condividi</span><span class="sxs-lookup"><span data-stu-id="8a664-130">-Share</span></span>
<span data-ttu-id="8a664-131">Specifica un oggetto **CloudFileShare** per rappresentare la condivisione per cui questo cmdlet imposta una quota.</span><span class="sxs-lookup"><span data-stu-id="8a664-131">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="8a664-132">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="8a664-132">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="8a664-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8a664-133">-ShareName</span></span>
<span data-ttu-id="8a664-134">Specifica il nome della condivisione file per cui impostare una quota.</span><span class="sxs-lookup"><span data-stu-id="8a664-134">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a664-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a664-135">CommonParameters</span></span>
<span data-ttu-id="8a664-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a664-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a664-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a664-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a664-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a664-138">INPUTS</span></span>

## <span data-ttu-id="8a664-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a664-139">OUTPUTS</span></span>

## <span data-ttu-id="8a664-140">Note</span><span class="sxs-lookup"><span data-stu-id="8a664-140">NOTES</span></span>

## <span data-ttu-id="8a664-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a664-141">RELATED LINKS</span></span>

[<span data-ttu-id="8a664-142">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8a664-142">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="8a664-143">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="8a664-143">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="8a664-144">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8a664-144">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
