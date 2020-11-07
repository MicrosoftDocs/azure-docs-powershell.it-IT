---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 0c77d2dedadd205a659bf296e02c09b98342dcc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688472"
---
# <span data-ttu-id="479d0-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="479d0-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="479d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="479d0-102">SYNOPSIS</span></span>
<span data-ttu-id="479d0-103">Aggiorna un criterio di accesso archiviato in una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="479d0-103">Updates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="479d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="479d0-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="479d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="479d0-105">DESCRIPTION</span></span>
<span data-ttu-id="479d0-106">Il cmdlet **set-AzureStorageShareStoredAccessPolicy** aggiorna i criteri di accesso archiviati in una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="479d0-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="479d0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="479d0-107">EXAMPLES</span></span>

### <span data-ttu-id="479d0-108">Esempio 1: aggiornare un criterio di accesso archiviato nella condivisione di archiviazione</span><span class="sxs-lookup"><span data-stu-id="479d0-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="479d0-109">Questo comando aggiorna un criterio di accesso archiviato con l'autorizzazione completa in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="479d0-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="479d0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="479d0-110">PARAMETERS</span></span>

### <span data-ttu-id="479d0-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="479d0-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="479d0-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="479d0-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="479d0-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="479d0-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="479d0-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="479d0-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="479d0-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="479d0-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="479d0-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="479d0-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="479d0-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="479d0-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="479d0-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="479d0-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="479d0-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="479d0-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="479d0-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="479d0-120">The default value is 10.</span></span>

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

### <span data-ttu-id="479d0-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="479d0-121">-Context</span></span>
<span data-ttu-id="479d0-122">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="479d0-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="479d0-123">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="479d0-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="479d0-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="479d0-124">-ExpiryTime</span></span>
<span data-ttu-id="479d0-125">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="479d0-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="479d0-126">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="479d0-126">-NoExpiryTime</span></span>
<span data-ttu-id="479d0-127">Indica che questo cmdlet cancella la proprietà **ExpiryTime** nei criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="479d0-127">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="479d0-128">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="479d0-128">-NoStartTime</span></span>
<span data-ttu-id="479d0-129">Indica che questo cmdlet cancella la proprietà **StartTime** nei criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="479d0-129">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="479d0-130">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="479d0-130">-Permission</span></span>
<span data-ttu-id="479d0-131">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla condivisione o ai file sotto di essa.</span><span class="sxs-lookup"><span data-stu-id="479d0-131">Specifies permissions in the stored access policy to access the share or files under it.</span></span>

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

### <span data-ttu-id="479d0-132">-Policy</span><span class="sxs-lookup"><span data-stu-id="479d0-132">-Policy</span></span>
<span data-ttu-id="479d0-133">Specifica un nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="479d0-133">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="479d0-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="479d0-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="479d0-135">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="479d0-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="479d0-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="479d0-136">-ShareName</span></span>
<span data-ttu-id="479d0-137">Specifica il nome della condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="479d0-137">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="479d0-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="479d0-138">-StartTime</span></span>
<span data-ttu-id="479d0-139">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="479d0-139">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="479d0-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="479d0-140">-Confirm</span></span>
<span data-ttu-id="479d0-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="479d0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="479d0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="479d0-142">-WhatIf</span></span>
<span data-ttu-id="479d0-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="479d0-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="479d0-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="479d0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="479d0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="479d0-145">CommonParameters</span></span>
<span data-ttu-id="479d0-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="479d0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="479d0-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="479d0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="479d0-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="479d0-148">INPUTS</span></span>

### <span data-ttu-id="479d0-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="479d0-149">IStorageContext</span></span>

<span data-ttu-id="479d0-150">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="479d0-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="479d0-151">Stringa</span><span class="sxs-lookup"><span data-stu-id="479d0-151">String</span></span>

<span data-ttu-id="479d0-152">Il parametro "ShareName" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="479d0-152">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="479d0-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="479d0-153">OUTPUTS</span></span>

### <span data-ttu-id="479d0-154">System. String</span><span class="sxs-lookup"><span data-stu-id="479d0-154">System.String</span></span>

## <span data-ttu-id="479d0-155">Note</span><span class="sxs-lookup"><span data-stu-id="479d0-155">NOTES</span></span>

## <span data-ttu-id="479d0-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="479d0-156">RELATED LINKS</span></span>

[<span data-ttu-id="479d0-157">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="479d0-157">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="479d0-158">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="479d0-158">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="479d0-159">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="479d0-159">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="479d0-160">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="479d0-160">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
