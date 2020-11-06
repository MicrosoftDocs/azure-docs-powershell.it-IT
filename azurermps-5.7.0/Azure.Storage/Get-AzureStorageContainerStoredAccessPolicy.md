---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 19dbbe53347a06030c175f45f722bfd287863d85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515936"
---
# <span data-ttu-id="3bbce-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3bbce-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="3bbce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3bbce-102">SYNOPSIS</span></span>
<span data-ttu-id="3bbce-103">Ottiene i criteri di accesso archiviati o i criteri per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3bbce-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bbce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bbce-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3bbce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bbce-105">DESCRIPTION</span></span>
<span data-ttu-id="3bbce-106">Il cmdlet **Get-AzureStorageContainerStoredAccessPolicy** elenca i criteri di accesso archiviati o i criteri per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3bbce-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="3bbce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bbce-107">EXAMPLES</span></span>

### <span data-ttu-id="3bbce-108">Esempio 1: ottenere un criterio di accesso archiviato in un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3bbce-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="3bbce-109">Questo comando consente di ottenere i criteri di accesso denominati Policy22 nel contenitore di archiviazione denominato Container07.</span><span class="sxs-lookup"><span data-stu-id="3bbce-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="3bbce-110">Esempio 2: ottenere tutti i criteri di accesso archiviati in un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3bbce-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="3bbce-111">Questo comando consente di ottenere tutti i criteri di accesso nel contenitore di archiviazione denominato Container07.</span><span class="sxs-lookup"><span data-stu-id="3bbce-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="3bbce-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3bbce-112">PARAMETERS</span></span>

### <span data-ttu-id="3bbce-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3bbce-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3bbce-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="3bbce-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3bbce-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="3bbce-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3bbce-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="3bbce-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3bbce-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3bbce-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3bbce-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="3bbce-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3bbce-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="3bbce-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3bbce-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="3bbce-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3bbce-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="3bbce-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3bbce-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="3bbce-122">The default value is 10.</span></span>

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

### <span data-ttu-id="3bbce-123">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="3bbce-123">-Container</span></span>
<span data-ttu-id="3bbce-124">Specifica il nome del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3bbce-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bbce-125">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3bbce-125">-Context</span></span>
<span data-ttu-id="3bbce-126">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3bbce-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="3bbce-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="3bbce-127">-Policy</span></span>
<span data-ttu-id="3bbce-128">Specifica i criteri di accesso archiviati di Azure.</span><span class="sxs-lookup"><span data-stu-id="3bbce-128">Specifies the Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bbce-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3bbce-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3bbce-130">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="3bbce-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3bbce-131">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="3bbce-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="3bbce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bbce-132">CommonParameters</span></span>
<span data-ttu-id="3bbce-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bbce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bbce-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bbce-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bbce-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3bbce-135">INPUTS</span></span>

### <span data-ttu-id="3bbce-136">Stringa</span><span class="sxs-lookup"><span data-stu-id="3bbce-136">String</span></span>

<span data-ttu-id="3bbce-137">Il parametro "container" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3bbce-137">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="3bbce-138">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3bbce-138">IStorageContext</span></span>

<span data-ttu-id="3bbce-139">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3bbce-139">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="3bbce-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bbce-140">OUTPUTS</span></span>

### <span data-ttu-id="3bbce-141">Microsoft. WindowsAzure. storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="3bbce-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="3bbce-142">Note</span><span class="sxs-lookup"><span data-stu-id="3bbce-142">NOTES</span></span>

## <span data-ttu-id="3bbce-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bbce-143">RELATED LINKS</span></span>

[<span data-ttu-id="3bbce-144">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3bbce-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="3bbce-145">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3bbce-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="3bbce-146">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3bbce-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


