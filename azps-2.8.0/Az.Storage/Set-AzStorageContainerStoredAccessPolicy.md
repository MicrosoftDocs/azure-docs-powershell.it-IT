---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: f6c83084d52848e3dff25e2d3f0a22255845a56c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673801"
---
# <span data-ttu-id="96cf5-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96cf5-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="96cf5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="96cf5-103">Imposta un criterio di accesso archiviato per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="96cf5-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="96cf5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96cf5-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96cf5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96cf5-105">DESCRIPTION</span></span>
<span data-ttu-id="96cf5-106">Il cmdlet **set-AzStorageContainerStoredAccessPolicy** imposta un criterio di accesso archiviato per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="96cf5-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="96cf5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96cf5-107">EXAMPLES</span></span>

### <span data-ttu-id="96cf5-108">Esempio 1: impostare un criterio di accesso archiviato in un contenitore di archiviazione con l'autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="96cf5-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="96cf5-109">Questo comando imposta un criterio di accesso denominato Policy06 per il contenitore di archiviazione denominato concontainer.</span><span class="sxs-lookup"><span data-stu-id="96cf5-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="96cf5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96cf5-110">PARAMETERS</span></span>

### <span data-ttu-id="96cf5-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="96cf5-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="96cf5-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="96cf5-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="96cf5-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="96cf5-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="96cf5-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="96cf5-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="96cf5-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="96cf5-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="96cf5-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="96cf5-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="96cf5-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="96cf5-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="96cf5-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="96cf5-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="96cf5-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="96cf5-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="96cf5-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="96cf5-120">The default value is 10.</span></span>

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

### <span data-ttu-id="96cf5-121">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="96cf5-121">-Container</span></span>
<span data-ttu-id="96cf5-122">Specifica il nome del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="96cf5-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="96cf5-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="96cf5-123">-Context</span></span>
<span data-ttu-id="96cf5-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="96cf5-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="96cf5-125">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="96cf5-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="96cf5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96cf5-126">-DefaultProfile</span></span>
<span data-ttu-id="96cf5-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96cf5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96cf5-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="96cf5-128">-ExpiryTime</span></span>
<span data-ttu-id="96cf5-129">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="96cf5-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cf5-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="96cf5-130">-NoExpiryTime</span></span>
<span data-ttu-id="96cf5-131">Indica che il criterio di accesso non ha una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="96cf5-131">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cf5-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="96cf5-132">-NoStartTime</span></span>
<span data-ttu-id="96cf5-133">Imposta l'ora di inizio da $Null.</span><span class="sxs-lookup"><span data-stu-id="96cf5-133">Sets the start time to be $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cf5-134">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="96cf5-134">-Permission</span></span>
<span data-ttu-id="96cf5-135">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere al contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="96cf5-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="96cf5-136">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="96cf5-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cf5-137">-Policy</span><span class="sxs-lookup"><span data-stu-id="96cf5-137">-Policy</span></span>
<span data-ttu-id="96cf5-138">Specifica il nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="96cf5-138">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cf5-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="96cf5-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="96cf5-140">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="96cf5-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="96cf5-141">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="96cf5-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="96cf5-142">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="96cf5-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="96cf5-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="96cf5-143">-StartTime</span></span>
<span data-ttu-id="96cf5-144">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="96cf5-144">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cf5-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="96cf5-145">-Confirm</span></span>
<span data-ttu-id="96cf5-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96cf5-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cf5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96cf5-147">-WhatIf</span></span>
<span data-ttu-id="96cf5-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96cf5-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96cf5-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96cf5-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cf5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96cf5-150">CommonParameters</span></span>
<span data-ttu-id="96cf5-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96cf5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96cf5-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96cf5-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96cf5-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96cf5-153">INPUTS</span></span>

### <span data-ttu-id="96cf5-154">System. String</span><span class="sxs-lookup"><span data-stu-id="96cf5-154">System.String</span></span>

### <span data-ttu-id="96cf5-155">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="96cf5-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="96cf5-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96cf5-156">OUTPUTS</span></span>

### <span data-ttu-id="96cf5-157">System. String</span><span class="sxs-lookup"><span data-stu-id="96cf5-157">System.String</span></span>

## <span data-ttu-id="96cf5-158">Note</span><span class="sxs-lookup"><span data-stu-id="96cf5-158">NOTES</span></span>

## <span data-ttu-id="96cf5-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96cf5-159">RELATED LINKS</span></span>

[<span data-ttu-id="96cf5-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96cf5-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="96cf5-161">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="96cf5-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="96cf5-162">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96cf5-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="96cf5-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96cf5-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
