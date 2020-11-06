---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: cb39d9800271d68f8ac78ebffc9ed3345209177c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510196"
---
# <span data-ttu-id="bdbc9-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bdbc9-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="bdbc9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bdbc9-102">SYNOPSIS</span></span>
<span data-ttu-id="bdbc9-103">Rimuove un criterio di accesso archiviato da una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-103">Removes a stored access policy from a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdbc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdbc9-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdbc9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdbc9-105">DESCRIPTION</span></span>
<span data-ttu-id="bdbc9-106">Il cmdlet **Remove-AzureStorageShareStoredAccessPolicy** rimuove un criterio di accesso archiviato da una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="bdbc9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdbc9-107">EXAMPLES</span></span>

### <span data-ttu-id="bdbc9-108">Esempio 1: rimuovere un criterio di accesso archiviato da una condivisione di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="bdbc9-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="bdbc9-109">Questo comando rimuove un criterio di accesso archiviato denominato GeneralPolicy da ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="bdbc9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bdbc9-110">PARAMETERS</span></span>

### <span data-ttu-id="bdbc9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bdbc9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bdbc9-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bdbc9-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bdbc9-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bdbc9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bdbc9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bdbc9-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bdbc9-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bdbc9-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bdbc9-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bdbc9-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-120">The default value is 10.</span></span>

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

### <span data-ttu-id="bdbc9-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bdbc9-121">-Context</span></span>
<span data-ttu-id="bdbc9-122">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bdbc9-123">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="bdbc9-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="bdbc9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdbc9-124">-PassThru</span></span>
<span data-ttu-id="bdbc9-125">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-125">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="bdbc9-126">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-126">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="bdbc9-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="bdbc9-127">-Policy</span></span>
<span data-ttu-id="bdbc9-128">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-128">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bdbc9-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bdbc9-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bdbc9-130">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bdbc9-131">-ShareName</span><span class="sxs-lookup"><span data-stu-id="bdbc9-131">-ShareName</span></span>
<span data-ttu-id="bdbc9-132">Specifica il nome della condivisione di archiviazione per cui questo cmdlet rimuove un criterio.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-132">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="bdbc9-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bdbc9-133">-Confirm</span></span>
<span data-ttu-id="bdbc9-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdbc9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdbc9-135">-WhatIf</span></span>
<span data-ttu-id="bdbc9-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdbc9-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdbc9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdbc9-138">CommonParameters</span></span>
<span data-ttu-id="bdbc9-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdbc9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdbc9-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdbc9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdbc9-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bdbc9-141">INPUTS</span></span>

### <span data-ttu-id="bdbc9-142">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bdbc9-142">IStorageContext</span></span>

<span data-ttu-id="bdbc9-143">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bdbc9-143">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="bdbc9-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdbc9-144">OUTPUTS</span></span>

### <span data-ttu-id="bdbc9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bdbc9-145">System.Boolean</span></span>

## <span data-ttu-id="bdbc9-146">Note</span><span class="sxs-lookup"><span data-stu-id="bdbc9-146">NOTES</span></span>

## <span data-ttu-id="bdbc9-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdbc9-147">RELATED LINKS</span></span>

[<span data-ttu-id="bdbc9-148">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bdbc9-148">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="bdbc9-149">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bdbc9-149">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="bdbc9-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bdbc9-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="bdbc9-151">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bdbc9-151">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
