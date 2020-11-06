---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e2a6e00832ea57f3d5608b30791c37e5cde5be5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490782"
---
# <span data-ttu-id="4bdbe-101">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4bdbe-101">Remove-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="4bdbe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4bdbe-102">SYNOPSIS</span></span>
<span data-ttu-id="4bdbe-103">Rimuove un criterio di accesso archiviato da un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="4bdbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bdbe-104">SYNTAX</span></span>

```
Remove-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bdbe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bdbe-105">DESCRIPTION</span></span>
<span data-ttu-id="4bdbe-106">Il cmdlet **Remove-AzureStorageContainerStoredAccessPolicy** rimuove un criterio di accesso archiviato da un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-106">The **Remove-AzureStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="4bdbe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bdbe-107">EXAMPLES</span></span>

### <span data-ttu-id="4bdbe-108">Esempio 1: rimuovere un criterio di accesso archiviato da un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4bdbe-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="4bdbe-109">Questo comando rimuove un criterio di accesso denominato Policy03 dal contenitore archiviato denominato concontainer.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="4bdbe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4bdbe-110">PARAMETERS</span></span>

### <span data-ttu-id="4bdbe-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4bdbe-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4bdbe-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4bdbe-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4bdbe-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4bdbe-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4bdbe-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4bdbe-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4bdbe-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4bdbe-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4bdbe-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4bdbe-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-120">The default value is 10.</span></span>

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

### <span data-ttu-id="4bdbe-121">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="4bdbe-121">-Container</span></span>
<span data-ttu-id="4bdbe-122">Specifica il nome del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bdbe-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4bdbe-123">-Context</span></span>
<span data-ttu-id="4bdbe-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4bdbe-125">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4bdbe-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4bdbe-126">-PassThru</span></span>
<span data-ttu-id="4bdbe-127">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4bdbe-128">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-128">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdbe-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="4bdbe-129">-Policy</span></span>
<span data-ttu-id="4bdbe-130">Specifica i criteri di accesso archiviati, che includono le autorizzazioni per il token SAS.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-130">Specifies the stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bdbe-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4bdbe-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4bdbe-132">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-132">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4bdbe-133">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-133">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4bdbe-134">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-134">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4bdbe-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4bdbe-135">-Confirm</span></span>
<span data-ttu-id="4bdbe-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdbe-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bdbe-137">-WhatIf</span></span>
<span data-ttu-id="4bdbe-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bdbe-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdbe-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bdbe-140">CommonParameters</span></span>
<span data-ttu-id="4bdbe-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bdbe-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bdbe-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bdbe-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bdbe-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4bdbe-143">INPUTS</span></span>

## <span data-ttu-id="4bdbe-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bdbe-144">OUTPUTS</span></span>

## <span data-ttu-id="4bdbe-145">Note</span><span class="sxs-lookup"><span data-stu-id="4bdbe-145">NOTES</span></span>

## <span data-ttu-id="4bdbe-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bdbe-146">RELATED LINKS</span></span>

[<span data-ttu-id="4bdbe-147">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4bdbe-147">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="4bdbe-148">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4bdbe-148">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="4bdbe-149">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4bdbe-149">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4bdbe-150">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4bdbe-150">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)
