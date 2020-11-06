---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bdded3834806e33f4605f626b78fe06bc370bf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507172"
---
# <span data-ttu-id="efc59-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="efc59-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="efc59-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="efc59-102">SYNOPSIS</span></span>
<span data-ttu-id="efc59-103">Imposta un criterio di accesso archiviato per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="efc59-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="efc59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efc59-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc59-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efc59-105">DESCRIPTION</span></span>
<span data-ttu-id="efc59-106">Il cmdlet **set-AzureStorageContainerStoredAccessPolicy** imposta un criterio di accesso archiviato per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="efc59-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="efc59-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efc59-107">EXAMPLES</span></span>

### <span data-ttu-id="efc59-108">Esempio 1: impostare un criterio di accesso archiviato in un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="efc59-108">Example 1: Set a stored access policy in a storage container</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06"
```

<span data-ttu-id="efc59-109">Questo comando imposta un criterio di accesso denominato Policy06 per il contenitore di archiviazione denominato concontainer.</span><span class="sxs-lookup"><span data-stu-id="efc59-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="efc59-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efc59-110">PARAMETERS</span></span>

### <span data-ttu-id="efc59-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="efc59-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="efc59-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="efc59-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="efc59-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="efc59-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="efc59-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="efc59-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="efc59-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="efc59-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="efc59-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="efc59-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="efc59-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="efc59-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="efc59-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="efc59-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="efc59-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="efc59-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="efc59-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="efc59-120">The default value is 10.</span></span>

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

### <span data-ttu-id="efc59-121">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="efc59-121">-Container</span></span>
<span data-ttu-id="efc59-122">Specifica il nome del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="efc59-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="efc59-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="efc59-123">-Context</span></span>
<span data-ttu-id="efc59-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="efc59-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="efc59-125">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="efc59-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="efc59-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="efc59-126">-ExpiryTime</span></span>
<span data-ttu-id="efc59-127">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="efc59-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc59-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="efc59-128">-NoExpiryTime</span></span>
<span data-ttu-id="efc59-129">Indica che il criterio di accesso non ha una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="efc59-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="efc59-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="efc59-130">-NoStartTime</span></span>
<span data-ttu-id="efc59-131">Imposta l'ora di inizio da $Null.</span><span class="sxs-lookup"><span data-stu-id="efc59-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="efc59-132">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="efc59-132">-Permission</span></span>
<span data-ttu-id="efc59-133">Specifica il livello di accesso pubblico al contenitore.</span><span class="sxs-lookup"><span data-stu-id="efc59-133">Specifies the level of public access to this container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc59-134">-Policy</span><span class="sxs-lookup"><span data-stu-id="efc59-134">-Policy</span></span>
<span data-ttu-id="efc59-135">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="efc59-135">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc59-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="efc59-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="efc59-137">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="efc59-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="efc59-138">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="efc59-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="efc59-139">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="efc59-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="efc59-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="efc59-140">-StartTime</span></span>
<span data-ttu-id="efc59-141">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="efc59-141">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc59-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="efc59-142">-Confirm</span></span>
<span data-ttu-id="efc59-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efc59-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc59-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc59-144">-WhatIf</span></span>
<span data-ttu-id="efc59-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efc59-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efc59-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efc59-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc59-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc59-147">CommonParameters</span></span>
<span data-ttu-id="efc59-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc59-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc59-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc59-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc59-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="efc59-150">INPUTS</span></span>

## <span data-ttu-id="efc59-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efc59-151">OUTPUTS</span></span>

## <span data-ttu-id="efc59-152">Note</span><span class="sxs-lookup"><span data-stu-id="efc59-152">NOTES</span></span>

## <span data-ttu-id="efc59-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efc59-153">RELATED LINKS</span></span>

[<span data-ttu-id="efc59-154">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="efc59-154">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="efc59-155">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="efc59-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="efc59-156">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="efc59-156">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="efc59-157">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="efc59-157">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
