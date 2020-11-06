---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3dbc0f3c014290cb412751440590cbee1f6df685
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511424"
---
# <span data-ttu-id="02f7c-101">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02f7c-101">Remove-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="02f7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="02f7c-103">Rimuove un criterio di accesso archiviato da un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="02f7c-103">Removes a stored access policy from an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02f7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02f7c-104">SYNTAX</span></span>

```
Remove-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02f7c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02f7c-105">DESCRIPTION</span></span>
<span data-ttu-id="02f7c-106">Il cmdlet **Remove-AzureStorageContainerStoredAccessPolicy** rimuove un criterio di accesso archiviato da un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="02f7c-106">The **Remove-AzureStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="02f7c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02f7c-107">EXAMPLES</span></span>

### <span data-ttu-id="02f7c-108">Esempio 1: rimuovere un criterio di accesso archiviato da un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="02f7c-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="02f7c-109">Questo comando rimuove un criterio di accesso denominato Policy03 dal contenitore archiviato denominato concontainer.</span><span class="sxs-lookup"><span data-stu-id="02f7c-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="02f7c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02f7c-110">PARAMETERS</span></span>

### <span data-ttu-id="02f7c-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="02f7c-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="02f7c-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="02f7c-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="02f7c-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="02f7c-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="02f7c-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="02f7c-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="02f7c-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="02f7c-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="02f7c-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="02f7c-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="02f7c-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="02f7c-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="02f7c-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="02f7c-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="02f7c-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="02f7c-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="02f7c-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="02f7c-120">The default value is 10.</span></span>

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

### <span data-ttu-id="02f7c-121">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="02f7c-121">-Container</span></span>
<span data-ttu-id="02f7c-122">Specifica il nome del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="02f7c-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="02f7c-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="02f7c-123">-Context</span></span>
<span data-ttu-id="02f7c-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="02f7c-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="02f7c-125">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="02f7c-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="02f7c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02f7c-126">-PassThru</span></span>
<span data-ttu-id="02f7c-127">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="02f7c-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="02f7c-128">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="02f7c-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="02f7c-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="02f7c-129">-Policy</span></span>
<span data-ttu-id="02f7c-130">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02f7c-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="02f7c-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="02f7c-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="02f7c-132">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="02f7c-132">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="02f7c-133">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="02f7c-133">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="02f7c-134">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="02f7c-134">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="02f7c-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="02f7c-135">-Confirm</span></span>
<span data-ttu-id="02f7c-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02f7c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02f7c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f7c-137">-WhatIf</span></span>
<span data-ttu-id="02f7c-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02f7c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02f7c-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02f7c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02f7c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f7c-140">CommonParameters</span></span>
<span data-ttu-id="02f7c-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02f7c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f7c-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02f7c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f7c-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02f7c-143">INPUTS</span></span>

### <span data-ttu-id="02f7c-144">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="02f7c-144">IStorageContext</span></span>

<span data-ttu-id="02f7c-145">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="02f7c-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="02f7c-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02f7c-146">OUTPUTS</span></span>

### <span data-ttu-id="02f7c-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02f7c-147">System.Boolean</span></span>

## <span data-ttu-id="02f7c-148">Note</span><span class="sxs-lookup"><span data-stu-id="02f7c-148">NOTES</span></span>

## <span data-ttu-id="02f7c-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02f7c-149">RELATED LINKS</span></span>

[<span data-ttu-id="02f7c-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02f7c-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="02f7c-151">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02f7c-151">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="02f7c-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="02f7c-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="02f7c-153">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02f7c-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)
