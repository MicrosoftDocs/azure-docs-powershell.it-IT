---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: 1eb5803c65739c2e202d042efbf6ba4dff815394
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195806"
---
# <span data-ttu-id="7202a-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="7202a-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="7202a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7202a-102">SYNOPSIS</span></span>
<span data-ttu-id="7202a-103">Ottiene le regole CORS per un tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7202a-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="7202a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7202a-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7202a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7202a-105">DESCRIPTION</span></span>
<span data-ttu-id="7202a-106">Il cmdlet **Get-AzStorageCORSRule** ottiene le regole di condivisione delle risorse tra origini (CORS) per un tipo di servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7202a-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="7202a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7202a-107">EXAMPLES</span></span>

### <span data-ttu-id="7202a-108">Esempio 1: Ottenere le regole CORS del servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="7202a-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="7202a-109">Questo comando ottiene le regole CORS per il tipo di servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="7202a-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="7202a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7202a-110">PARAMETERS</span></span>

### <span data-ttu-id="7202a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7202a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7202a-112">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="7202a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7202a-113">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="7202a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7202a-114">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="7202a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7202a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7202a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7202a-116">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="7202a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7202a-117">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="7202a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7202a-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="7202a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7202a-119">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="7202a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7202a-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="7202a-120">The default value is 10.</span></span>

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

### <span data-ttu-id="7202a-121">-Context</span><span class="sxs-lookup"><span data-stu-id="7202a-121">-Context</span></span>
<span data-ttu-id="7202a-122">Specifica un contesto di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7202a-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="7202a-123">Per ottenere un contesto, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7202a-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7202a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7202a-124">-DefaultProfile</span></span>
<span data-ttu-id="7202a-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7202a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7202a-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7202a-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7202a-127">Specifica la durata del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="7202a-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7202a-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="7202a-128">-ServiceType</span></span>
<span data-ttu-id="7202a-129">Specifica il tipo di servizio di archiviazione di Azure per cui questo cmdlet ottiene le regole CORS.</span><span class="sxs-lookup"><span data-stu-id="7202a-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="7202a-130">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="7202a-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7202a-131">BLOB</span><span class="sxs-lookup"><span data-stu-id="7202a-131">Blob</span></span> 
- <span data-ttu-id="7202a-132">tavolo</span><span class="sxs-lookup"><span data-stu-id="7202a-132">Table</span></span> 
- <span data-ttu-id="7202a-133">Coda</span><span class="sxs-lookup"><span data-stu-id="7202a-133">Queue</span></span> 
- <span data-ttu-id="7202a-134">File</span><span class="sxs-lookup"><span data-stu-id="7202a-134">File</span></span>

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

### <span data-ttu-id="7202a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7202a-135">CommonParameters</span></span>
<span data-ttu-id="7202a-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7202a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7202a-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7202a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7202a-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="7202a-138">INPUTS</span></span>

### <span data-ttu-id="7202a-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7202a-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7202a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7202a-140">OUTPUTS</span></span>

### <span data-ttu-id="7202a-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="7202a-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="7202a-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="7202a-142">NOTES</span></span>

## <span data-ttu-id="7202a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7202a-143">RELATED LINKS</span></span>

[<span data-ttu-id="7202a-144">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="7202a-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="7202a-145">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="7202a-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


