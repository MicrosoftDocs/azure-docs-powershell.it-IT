---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: aeae25ab3a8ff0b1fa3eb91db90497b44555631f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348556"
---
# <span data-ttu-id="baf01-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="baf01-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="baf01-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="baf01-102">SYNOPSIS</span></span>
<span data-ttu-id="baf01-103">Rimuove CORS per un servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="baf01-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="baf01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="baf01-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="baf01-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="baf01-105">DESCRIPTION</span></span>
<span data-ttu-id="baf01-106">Il cmdlet **Remove-AzStorageCORSRule** rimuove la condivisione di risorse CORS (Cross-Origin Resource Sharing) per un servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="baf01-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="baf01-107">Questo cmdlet elimina tutte le regole di CORS in un tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="baf01-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="baf01-108">I tipi di servizi di archiviazione per questo cmdlet sono BLOB, Table, Queue e file.</span><span class="sxs-lookup"><span data-stu-id="baf01-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="baf01-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="baf01-109">EXAMPLES</span></span>

### <span data-ttu-id="baf01-110">Esempio 1: rimuovere le regole di CORS per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="baf01-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="baf01-111">Questo comando rimuove le regole di CORS per il tipo di servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="baf01-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="baf01-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="baf01-112">PARAMETERS</span></span>

### <span data-ttu-id="baf01-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="baf01-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="baf01-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="baf01-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="baf01-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="baf01-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="baf01-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="baf01-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="baf01-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="baf01-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="baf01-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="baf01-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="baf01-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="baf01-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="baf01-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="baf01-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="baf01-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="baf01-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="baf01-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="baf01-122">The default value is 10.</span></span>

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

### <span data-ttu-id="baf01-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="baf01-123">-Context</span></span>
<span data-ttu-id="baf01-124">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="baf01-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="baf01-125">Per ottenere il contesto di archiviazione, il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="baf01-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="baf01-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf01-126">-DefaultProfile</span></span>
<span data-ttu-id="baf01-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="baf01-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baf01-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="baf01-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="baf01-129">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="baf01-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="baf01-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="baf01-130">-ServiceType</span></span>
<span data-ttu-id="baf01-131">Specifica il tipo di servizio di archiviazione di Azure per cui questo cmdlet rimuove le regole.</span><span class="sxs-lookup"><span data-stu-id="baf01-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="baf01-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="baf01-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="baf01-133">BLOB</span><span class="sxs-lookup"><span data-stu-id="baf01-133">Blob</span></span> 
- <span data-ttu-id="baf01-134">tavolo</span><span class="sxs-lookup"><span data-stu-id="baf01-134">Table</span></span> 
- <span data-ttu-id="baf01-135">Coda</span><span class="sxs-lookup"><span data-stu-id="baf01-135">Queue</span></span> 
- <span data-ttu-id="baf01-136">File</span><span class="sxs-lookup"><span data-stu-id="baf01-136">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf01-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf01-137">CommonParameters</span></span>
<span data-ttu-id="baf01-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baf01-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf01-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baf01-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf01-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="baf01-140">INPUTS</span></span>

### <span data-ttu-id="baf01-141">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="baf01-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="baf01-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="baf01-142">OUTPUTS</span></span>

### <span data-ttu-id="baf01-143">System. void</span><span class="sxs-lookup"><span data-stu-id="baf01-143">System.Void</span></span>

## <span data-ttu-id="baf01-144">Note</span><span class="sxs-lookup"><span data-stu-id="baf01-144">NOTES</span></span>

## <span data-ttu-id="baf01-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="baf01-145">RELATED LINKS</span></span>

[<span data-ttu-id="baf01-146">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="baf01-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="baf01-147">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="baf01-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


