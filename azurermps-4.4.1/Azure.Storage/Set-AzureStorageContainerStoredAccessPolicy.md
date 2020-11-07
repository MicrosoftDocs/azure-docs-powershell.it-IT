---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 63fd207c9d3348e17718f6d4ad8dbd53a09752af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687752"
---
# <span data-ttu-id="fbbb5-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fbbb5-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="fbbb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbbb5-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbb5-103">Imposta un criterio di accesso archiviato per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-103">Sets a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbbb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbbb5-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbbb5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbbb5-105">DESCRIPTION</span></span>
<span data-ttu-id="fbbb5-106">Il cmdlet **set-AzureStorageContainerStoredAccessPolicy** imposta un criterio di accesso archiviato per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="fbbb5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbbb5-107">EXAMPLES</span></span>

### <span data-ttu-id="fbbb5-108">Esempio 1: impostare un criterio di accesso archiviato in un contenitore di archiviazione con l'autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="fbbb5-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="fbbb5-109">Questo comando imposta un criterio di accesso denominato Policy06 per il contenitore di archiviazione denominato concontainer.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="fbbb5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbbb5-110">PARAMETERS</span></span>

### <span data-ttu-id="fbbb5-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fbbb5-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fbbb5-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fbbb5-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fbbb5-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fbbb5-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fbbb5-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fbbb5-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fbbb5-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fbbb5-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fbbb5-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fbbb5-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-120">The default value is 10.</span></span>

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

### <span data-ttu-id="fbbb5-121">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="fbbb5-121">-Container</span></span>
<span data-ttu-id="fbbb5-122">Specifica il nome del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="fbbb5-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="fbbb5-123">-Context</span></span>
<span data-ttu-id="fbbb5-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fbbb5-125">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fbbb5-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fbbb5-126">-ExpiryTime</span></span>
<span data-ttu-id="fbbb5-127">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="fbbb5-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fbbb5-128">-NoExpiryTime</span></span>
<span data-ttu-id="fbbb5-129">Indica che il criterio di accesso non ha una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="fbbb5-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="fbbb5-130">-NoStartTime</span></span>
<span data-ttu-id="fbbb5-131">Imposta l'ora di inizio da $Null.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="fbbb5-132">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="fbbb5-132">-Permission</span></span>
<span data-ttu-id="fbbb5-133">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere al contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-133">Specifies permissions in the stored access policy to access the storage container.</span></span>

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

### <span data-ttu-id="fbbb5-134">-Policy</span><span class="sxs-lookup"><span data-stu-id="fbbb5-134">-Policy</span></span>
<span data-ttu-id="fbbb5-135">Specifica il nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-135">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="fbbb5-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fbbb5-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fbbb5-137">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fbbb5-138">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fbbb5-139">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fbbb5-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fbbb5-140">-StartTime</span></span>
<span data-ttu-id="fbbb5-141">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-141">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="fbbb5-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fbbb5-142">-Confirm</span></span>
<span data-ttu-id="fbbb5-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbbb5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbbb5-144">-WhatIf</span></span>
<span data-ttu-id="fbbb5-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbbb5-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbbb5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbb5-147">CommonParameters</span></span>
<span data-ttu-id="fbbb5-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbb5-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbbb5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbb5-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbbb5-150">INPUTS</span></span>

### <span data-ttu-id="fbbb5-151">Stringa</span><span class="sxs-lookup"><span data-stu-id="fbbb5-151">String</span></span>

<span data-ttu-id="fbbb5-152">Il parametro "container" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fbbb5-152">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="fbbb5-153">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fbbb5-153">IStorageContext</span></span>

<span data-ttu-id="fbbb5-154">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fbbb5-154">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="fbbb5-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbbb5-155">OUTPUTS</span></span>

### <span data-ttu-id="fbbb5-156">System. String</span><span class="sxs-lookup"><span data-stu-id="fbbb5-156">System.String</span></span>

## <span data-ttu-id="fbbb5-157">Note</span><span class="sxs-lookup"><span data-stu-id="fbbb5-157">NOTES</span></span>

## <span data-ttu-id="fbbb5-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbbb5-158">RELATED LINKS</span></span>

[<span data-ttu-id="fbbb5-159">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fbbb5-159">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="fbbb5-160">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fbbb5-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="fbbb5-161">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fbbb5-161">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="fbbb5-162">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fbbb5-162">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
