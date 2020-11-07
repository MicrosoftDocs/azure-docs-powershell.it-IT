---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 9a57f736ada870ac9cc8d65e27104050ba395e2b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862013"
---
# <span data-ttu-id="7138b-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7138b-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="7138b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7138b-102">SYNOPSIS</span></span>
<span data-ttu-id="7138b-103">Aggiorna un criterio di accesso archiviato in una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7138b-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="7138b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7138b-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7138b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7138b-105">DESCRIPTION</span></span>
<span data-ttu-id="7138b-106">Il cmdlet **set-AzStorageShareStoredAccessPolicy** aggiorna i criteri di accesso archiviati in una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7138b-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="7138b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7138b-107">EXAMPLES</span></span>

### <span data-ttu-id="7138b-108">Esempio 1: aggiornare un criterio di accesso archiviato nella condivisione di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7138b-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="7138b-109">Questo comando aggiorna un criterio di accesso archiviato con l'autorizzazione completa in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="7138b-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="7138b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7138b-110">PARAMETERS</span></span>

### <span data-ttu-id="7138b-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7138b-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7138b-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="7138b-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7138b-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="7138b-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7138b-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="7138b-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7138b-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7138b-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7138b-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="7138b-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7138b-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="7138b-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7138b-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="7138b-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7138b-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="7138b-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7138b-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="7138b-120">The default value is 10.</span></span>

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

### <span data-ttu-id="7138b-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7138b-121">-Context</span></span>
<span data-ttu-id="7138b-122">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7138b-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7138b-123">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="7138b-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7138b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7138b-124">-DefaultProfile</span></span>
<span data-ttu-id="7138b-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7138b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7138b-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7138b-126">-ExpiryTime</span></span>
<span data-ttu-id="7138b-127">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="7138b-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="7138b-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7138b-128">-NoExpiryTime</span></span>
<span data-ttu-id="7138b-129">Indica che questo cmdlet cancella la proprietà **ExpiryTime** nei criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="7138b-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="7138b-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="7138b-130">-NoStartTime</span></span>
<span data-ttu-id="7138b-131">Indica che questo cmdlet cancella la proprietà **StartTime** nei criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="7138b-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="7138b-132">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="7138b-132">-Permission</span></span>
<span data-ttu-id="7138b-133">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla condivisione o ai file sotto di essa.</span><span class="sxs-lookup"><span data-stu-id="7138b-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="7138b-134">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="7138b-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="7138b-135">-Policy</span><span class="sxs-lookup"><span data-stu-id="7138b-135">-Policy</span></span>
<span data-ttu-id="7138b-136">Specifica un nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="7138b-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="7138b-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7138b-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7138b-138">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="7138b-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7138b-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7138b-139">-ShareName</span></span>
<span data-ttu-id="7138b-140">Specifica il nome della condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7138b-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="7138b-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7138b-141">-StartTime</span></span>
<span data-ttu-id="7138b-142">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="7138b-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="7138b-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7138b-143">-Confirm</span></span>
<span data-ttu-id="7138b-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7138b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7138b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7138b-145">-WhatIf</span></span>
<span data-ttu-id="7138b-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7138b-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7138b-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7138b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7138b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7138b-148">CommonParameters</span></span>
<span data-ttu-id="7138b-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7138b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7138b-150">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7138b-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7138b-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7138b-151">INPUTS</span></span>

### <span data-ttu-id="7138b-152">System. String</span><span class="sxs-lookup"><span data-stu-id="7138b-152">System.String</span></span>

### <span data-ttu-id="7138b-153">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7138b-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7138b-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7138b-154">OUTPUTS</span></span>

### <span data-ttu-id="7138b-155">System. String</span><span class="sxs-lookup"><span data-stu-id="7138b-155">System.String</span></span>

## <span data-ttu-id="7138b-156">Note</span><span class="sxs-lookup"><span data-stu-id="7138b-156">NOTES</span></span>

## <span data-ttu-id="7138b-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7138b-157">RELATED LINKS</span></span>

[<span data-ttu-id="7138b-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7138b-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="7138b-159">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7138b-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="7138b-160">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7138b-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="7138b-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7138b-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
