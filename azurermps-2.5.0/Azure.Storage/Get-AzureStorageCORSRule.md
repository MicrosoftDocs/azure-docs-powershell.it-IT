---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecorsrule
schema: 2.0.0
ms.openlocfilehash: cf9f4b3a6d58754c4b992163625887afcb3439b2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866406"
---
# <span data-ttu-id="03dfc-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="03dfc-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="03dfc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="03dfc-103">Ottiene le regole di CORS per un tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03dfc-103">Gets CORS rules for a Storage service type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03dfc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03dfc-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="03dfc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="03dfc-106">Il cmdlet **Get-AzureStorageCORSRule** ottiene le regole CORS (Cross-Origin Resource Sharing) per un tipo di servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="03dfc-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="03dfc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03dfc-107">EXAMPLES</span></span>

### <span data-ttu-id="03dfc-108">Esempio 1: ottenere le regole di CORS del servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="03dfc-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="03dfc-109">Questo comando ottiene le regole CORS per il tipo di servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="03dfc-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="03dfc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03dfc-110">PARAMETERS</span></span>

### <span data-ttu-id="03dfc-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="03dfc-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="03dfc-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="03dfc-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="03dfc-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="03dfc-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="03dfc-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="03dfc-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="03dfc-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="03dfc-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="03dfc-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="03dfc-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="03dfc-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="03dfc-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="03dfc-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="03dfc-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="03dfc-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="03dfc-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="03dfc-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="03dfc-120">The default value is 10.</span></span>

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

### <span data-ttu-id="03dfc-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="03dfc-121">-Context</span></span>
<span data-ttu-id="03dfc-122">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="03dfc-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="03dfc-123">Per ottenere un contesto, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="03dfc-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="03dfc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03dfc-124">-DefaultProfile</span></span>
<span data-ttu-id="03dfc-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03dfc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03dfc-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="03dfc-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="03dfc-127">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="03dfc-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="03dfc-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="03dfc-128">-ServiceType</span></span>
<span data-ttu-id="03dfc-129">Specifica il tipo di servizio di archiviazione di Azure per cui questo cmdlet ottiene le regole di CORS.</span><span class="sxs-lookup"><span data-stu-id="03dfc-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="03dfc-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="03dfc-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03dfc-131">BLOB</span><span class="sxs-lookup"><span data-stu-id="03dfc-131">Blob</span></span> 
- <span data-ttu-id="03dfc-132">tavolo</span><span class="sxs-lookup"><span data-stu-id="03dfc-132">Table</span></span> 
- <span data-ttu-id="03dfc-133">Coda</span><span class="sxs-lookup"><span data-stu-id="03dfc-133">Queue</span></span> 
- <span data-ttu-id="03dfc-134">File</span><span class="sxs-lookup"><span data-stu-id="03dfc-134">File</span></span>

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

### <span data-ttu-id="03dfc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03dfc-135">CommonParameters</span></span>
<span data-ttu-id="03dfc-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03dfc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03dfc-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03dfc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03dfc-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03dfc-138">INPUTS</span></span>

### <span data-ttu-id="03dfc-139">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="03dfc-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="03dfc-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03dfc-140">OUTPUTS</span></span>

### <span data-ttu-id="03dfc-141">Microsoft. WindowsAzure. Commands. storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="03dfc-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="03dfc-142">Note</span><span class="sxs-lookup"><span data-stu-id="03dfc-142">NOTES</span></span>

## <span data-ttu-id="03dfc-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03dfc-143">RELATED LINKS</span></span>

[<span data-ttu-id="03dfc-144">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="03dfc-144">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="03dfc-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="03dfc-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


