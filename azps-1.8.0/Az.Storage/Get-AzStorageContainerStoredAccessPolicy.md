---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 620667bdc8e3c8b70ce7e0bcd8636f46504193a2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676623"
---
# <span data-ttu-id="209e2-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="209e2-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="209e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="209e2-102">SYNOPSIS</span></span>
<span data-ttu-id="209e2-103">Ottiene i criteri di accesso archiviati o i criteri per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="209e2-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="209e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="209e2-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="209e2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="209e2-105">DESCRIPTION</span></span>
<span data-ttu-id="209e2-106">Il cmdlet **Get-AzStorageContainerStoredAccessPolicy** elenca i criteri di accesso archiviati o i criteri per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="209e2-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="209e2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="209e2-107">EXAMPLES</span></span>

### <span data-ttu-id="209e2-108">Esempio 1: ottenere un criterio di accesso archiviato in un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="209e2-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="209e2-109">Questo comando consente di ottenere i criteri di accesso denominati Policy22 nel contenitore di archiviazione denominato Container07.</span><span class="sxs-lookup"><span data-stu-id="209e2-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="209e2-110">Esempio 2: ottenere tutti i criteri di accesso archiviati in un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="209e2-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="209e2-111">Questo comando consente di ottenere tutti i criteri di accesso nel contenitore di archiviazione denominato Container07.</span><span class="sxs-lookup"><span data-stu-id="209e2-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="209e2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="209e2-112">PARAMETERS</span></span>

### <span data-ttu-id="209e2-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="209e2-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="209e2-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="209e2-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="209e2-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="209e2-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="209e2-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="209e2-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="209e2-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="209e2-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="209e2-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="209e2-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="209e2-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="209e2-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="209e2-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="209e2-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="209e2-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="209e2-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="209e2-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="209e2-122">The default value is 10.</span></span>

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

### <span data-ttu-id="209e2-123">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="209e2-123">-Container</span></span>
<span data-ttu-id="209e2-124">Specifica il nome del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="209e2-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="209e2-125">-Contesto</span><span class="sxs-lookup"><span data-stu-id="209e2-125">-Context</span></span>
<span data-ttu-id="209e2-126">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="209e2-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="209e2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="209e2-127">-DefaultProfile</span></span>
<span data-ttu-id="209e2-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="209e2-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="209e2-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="209e2-129">-Policy</span></span>
<span data-ttu-id="209e2-130">Specifica i criteri di accesso archiviati di Azure.</span><span class="sxs-lookup"><span data-stu-id="209e2-130">Specifies the Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209e2-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="209e2-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="209e2-132">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="209e2-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="209e2-133">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="209e2-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="209e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="209e2-134">CommonParameters</span></span>
<span data-ttu-id="209e2-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="209e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="209e2-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="209e2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="209e2-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="209e2-137">INPUTS</span></span>

### <span data-ttu-id="209e2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="209e2-138">System.String</span></span>

### <span data-ttu-id="209e2-139">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="209e2-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="209e2-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="209e2-140">OUTPUTS</span></span>

### <span data-ttu-id="209e2-141">Microsoft. WindowsAzure. storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="209e2-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="209e2-142">Note</span><span class="sxs-lookup"><span data-stu-id="209e2-142">NOTES</span></span>

## <span data-ttu-id="209e2-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="209e2-143">RELATED LINKS</span></span>

[<span data-ttu-id="209e2-144">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="209e2-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="209e2-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="209e2-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="209e2-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="209e2-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)

