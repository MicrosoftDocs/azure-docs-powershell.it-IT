---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: db37ead04710a422983f00b461a69b1cb12f328f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676519"
---
# <span data-ttu-id="65b18-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65b18-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="65b18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65b18-102">SYNOPSIS</span></span>
<span data-ttu-id="65b18-103">Rimuove un criterio di accesso archiviato da una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="65b18-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="65b18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65b18-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65b18-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65b18-105">DESCRIPTION</span></span>
<span data-ttu-id="65b18-106">Il cmdlet **Remove-AzStorageShareStoredAccessPolicy** rimuove un criterio di accesso archiviato da una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="65b18-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="65b18-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65b18-107">EXAMPLES</span></span>

### <span data-ttu-id="65b18-108">Esempio 1: rimuovere un criterio di accesso archiviato da una condivisione di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="65b18-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="65b18-109">Questo comando rimuove un criterio di accesso archiviato denominato GeneralPolicy da ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="65b18-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="65b18-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65b18-110">PARAMETERS</span></span>

### <span data-ttu-id="65b18-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="65b18-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="65b18-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="65b18-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="65b18-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="65b18-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="65b18-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="65b18-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="65b18-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="65b18-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="65b18-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="65b18-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="65b18-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="65b18-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="65b18-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="65b18-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="65b18-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="65b18-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="65b18-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="65b18-120">The default value is 10.</span></span>

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

### <span data-ttu-id="65b18-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="65b18-121">-Context</span></span>
<span data-ttu-id="65b18-122">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="65b18-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="65b18-123">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="65b18-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="65b18-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b18-124">-DefaultProfile</span></span>
<span data-ttu-id="65b18-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65b18-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65b18-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65b18-126">-PassThru</span></span>
<span data-ttu-id="65b18-127">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="65b18-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="65b18-128">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="65b18-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="65b18-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="65b18-129">-Policy</span></span>
<span data-ttu-id="65b18-130">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65b18-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b18-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="65b18-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="65b18-132">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="65b18-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="65b18-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="65b18-133">-ShareName</span></span>
<span data-ttu-id="65b18-134">Specifica il nome della condivisione di archiviazione per cui questo cmdlet rimuove un criterio.</span><span class="sxs-lookup"><span data-stu-id="65b18-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b18-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65b18-135">-Confirm</span></span>
<span data-ttu-id="65b18-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65b18-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b18-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65b18-137">-WhatIf</span></span>
<span data-ttu-id="65b18-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65b18-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65b18-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65b18-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b18-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b18-140">CommonParameters</span></span>
<span data-ttu-id="65b18-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b18-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b18-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65b18-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b18-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65b18-143">INPUTS</span></span>

### <span data-ttu-id="65b18-144">System. String</span><span class="sxs-lookup"><span data-stu-id="65b18-144">System.String</span></span>

### <span data-ttu-id="65b18-145">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="65b18-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="65b18-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65b18-146">OUTPUTS</span></span>

### <span data-ttu-id="65b18-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65b18-147">System.Boolean</span></span>

## <span data-ttu-id="65b18-148">Note</span><span class="sxs-lookup"><span data-stu-id="65b18-148">NOTES</span></span>

## <span data-ttu-id="65b18-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65b18-149">RELATED LINKS</span></span>

[<span data-ttu-id="65b18-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65b18-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="65b18-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65b18-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="65b18-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="65b18-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="65b18-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65b18-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)