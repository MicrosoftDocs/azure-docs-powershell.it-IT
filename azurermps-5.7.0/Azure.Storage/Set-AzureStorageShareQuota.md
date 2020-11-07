---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
ms.openlocfilehash: 54636c226d3e8eb7ca9572a8f2e6c95e96981875
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688475"
---
# <span data-ttu-id="ec8b2-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ec8b2-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="ec8b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec8b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8b2-103">Imposta la capacità di archiviazione per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-103">Sets the storage capacity for a share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec8b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec8b2-104">SYNTAX</span></span>

### <span data-ttu-id="ec8b2-105">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="ec8b2-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec8b2-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="ec8b2-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ec8b2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec8b2-107">DESCRIPTION</span></span>
<span data-ttu-id="ec8b2-108">Il cmdlet **set-AzureStorageShareQuota** imposta la capacità di archiviazione per una condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="ec8b2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec8b2-109">EXAMPLES</span></span>

### <span data-ttu-id="ec8b2-110">Esempio 1: impostare la capacità di archiviazione di una condivisione</span><span class="sxs-lookup"><span data-stu-id="ec8b2-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="ec8b2-111">Questo comando imposta la capacità di archiviazione per una condivisione denominata ContosoShare01 in 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="ec8b2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec8b2-112">PARAMETERS</span></span>

### <span data-ttu-id="ec8b2-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ec8b2-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ec8b2-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ec8b2-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ec8b2-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ec8b2-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ec8b2-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ec8b2-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ec8b2-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ec8b2-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ec8b2-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ec8b2-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ec8b2-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ec8b2-123">-Context</span></span>
<span data-ttu-id="ec8b2-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ec8b2-125">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="ec8b2-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="ec8b2-126">-Quota</span><span class="sxs-lookup"><span data-stu-id="ec8b2-126">-Quota</span></span>
<span data-ttu-id="ec8b2-127">Specifica il valore di quota in gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="ec8b2-127">Specifies the quota value in gigabytes (GB).</span></span>

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

### <span data-ttu-id="ec8b2-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ec8b2-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ec8b2-129">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ec8b2-130">-Condividi</span><span class="sxs-lookup"><span data-stu-id="ec8b2-130">-Share</span></span>
<span data-ttu-id="ec8b2-131">Specifica un oggetto **CloudFileShare** per rappresentare la condivisione per cui questo cmdlet imposta una quota.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-131">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="ec8b2-132">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-132">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="ec8b2-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ec8b2-133">-ShareName</span></span>
<span data-ttu-id="ec8b2-134">Specifica il nome della condivisione file per cui impostare una quota.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-134">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="ec8b2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8b2-135">CommonParameters</span></span>
<span data-ttu-id="ec8b2-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8b2-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec8b2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8b2-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec8b2-138">INPUTS</span></span>

### <span data-ttu-id="ec8b2-139">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ec8b2-139">IStorageContext</span></span>

<span data-ttu-id="ec8b2-140">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ec8b2-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ec8b2-141">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="ec8b2-141">CloudFileShare</span></span>

<span data-ttu-id="ec8b2-142">Il parametro "Share" accetta il valore di tipo "CloudFileShare" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ec8b2-142">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

### <span data-ttu-id="ec8b2-143">Stringa</span><span class="sxs-lookup"><span data-stu-id="ec8b2-143">String</span></span>

<span data-ttu-id="ec8b2-144">Il parametro "ShareName" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ec8b2-144">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ec8b2-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec8b2-145">OUTPUTS</span></span>

### <span data-ttu-id="ec8b2-146">Microsoft. WindowsAzure. storage. file. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="ec8b2-146">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="ec8b2-147">Note</span><span class="sxs-lookup"><span data-stu-id="ec8b2-147">NOTES</span></span>

## <span data-ttu-id="ec8b2-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec8b2-148">RELATED LINKS</span></span>

[<span data-ttu-id="ec8b2-149">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ec8b2-149">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="ec8b2-150">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="ec8b2-150">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="ec8b2-151">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ec8b2-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
