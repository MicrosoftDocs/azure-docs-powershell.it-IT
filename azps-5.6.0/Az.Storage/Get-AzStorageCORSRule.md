---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: e4313dda57632fbc2a5381b1f92067da85c1a905
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002653"
---
# <span data-ttu-id="ca71f-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="ca71f-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="ca71f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca71f-102">SYNOPSIS</span></span>
<span data-ttu-id="ca71f-103">Ottiene le regole CORS per un tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ca71f-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="ca71f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca71f-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ca71f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ca71f-105">DESCRIPTION</span></span>
<span data-ttu-id="ca71f-106">Il cmdlet **Get-AzStorageCORSRule** ottiene le regole di condivisione delle risorse tra origini (CORS) per un tipo di servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca71f-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="ca71f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca71f-107">EXAMPLES</span></span>

### <span data-ttu-id="ca71f-108">Esempio 1: Ottenere le regole CORS del servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="ca71f-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="ca71f-109">Questo comando ottiene le regole CORS per il tipo di servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="ca71f-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="ca71f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca71f-110">PARAMETERS</span></span>

### <span data-ttu-id="ca71f-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ca71f-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ca71f-112">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="ca71f-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ca71f-113">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ca71f-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ca71f-114">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ca71f-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ca71f-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ca71f-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ca71f-116">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="ca71f-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ca71f-117">È possibile usare questo parametro per limitare la simultaneità per limitare l'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="ca71f-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ca71f-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="ca71f-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ca71f-119">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ca71f-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ca71f-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="ca71f-120">The default value is 10.</span></span>

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

### <span data-ttu-id="ca71f-121">-Context</span><span class="sxs-lookup"><span data-stu-id="ca71f-121">-Context</span></span>
<span data-ttu-id="ca71f-122">Specifica un contesto di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca71f-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="ca71f-123">Per ottenere un contesto, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ca71f-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ca71f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca71f-124">-DefaultProfile</span></span>
<span data-ttu-id="ca71f-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca71f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca71f-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ca71f-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ca71f-127">Specifica la durata del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="ca71f-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ca71f-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ca71f-128">-ServiceType</span></span>
<span data-ttu-id="ca71f-129">Specifica il tipo di servizio di archiviazione di Azure per cui questo cmdlet ottiene le regole CORS.</span><span class="sxs-lookup"><span data-stu-id="ca71f-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="ca71f-130">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="ca71f-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ca71f-131">BLOB</span><span class="sxs-lookup"><span data-stu-id="ca71f-131">Blob</span></span> 
- <span data-ttu-id="ca71f-132">tavolo</span><span class="sxs-lookup"><span data-stu-id="ca71f-132">Table</span></span> 
- <span data-ttu-id="ca71f-133">Coda</span><span class="sxs-lookup"><span data-stu-id="ca71f-133">Queue</span></span> 
- <span data-ttu-id="ca71f-134">File</span><span class="sxs-lookup"><span data-stu-id="ca71f-134">File</span></span>

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

### <span data-ttu-id="ca71f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca71f-135">CommonParameters</span></span>
<span data-ttu-id="ca71f-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca71f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca71f-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca71f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca71f-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="ca71f-138">INPUTS</span></span>

### <span data-ttu-id="ca71f-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca71f-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ca71f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca71f-140">OUTPUTS</span></span>

### <span data-ttu-id="ca71f-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="ca71f-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="ca71f-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="ca71f-142">NOTES</span></span>

## <span data-ttu-id="ca71f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca71f-143">RELATED LINKS</span></span>

[<span data-ttu-id="ca71f-144">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="ca71f-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="ca71f-145">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="ca71f-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


