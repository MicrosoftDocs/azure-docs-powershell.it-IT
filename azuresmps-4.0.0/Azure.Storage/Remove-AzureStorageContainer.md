---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ccaa0ef1ce2a29851d6e90235e4564df3bde876
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490785"
---
# <span data-ttu-id="8bd4b-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8bd4b-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="8bd4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8bd4b-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd4b-103">Rimuove il contenitore di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="8bd4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bd4b-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bd4b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bd4b-105">DESCRIPTION</span></span>
<span data-ttu-id="8bd4b-106">Il cmdlet **Remove-AzureStorageContainer** rimuove il contenitore di archiviazione specificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="8bd4b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bd4b-107">EXAMPLES</span></span>

### <span data-ttu-id="8bd4b-108">Esempio 1: rimuovere un contenitore</span><span class="sxs-lookup"><span data-stu-id="8bd4b-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="8bd4b-109">In questo esempio viene rimosso un contenitore denominato MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="8bd4b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8bd4b-110">PARAMETERS</span></span>

### <span data-ttu-id="8bd4b-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8bd4b-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8bd4b-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8bd4b-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8bd4b-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8bd4b-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8bd4b-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8bd4b-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8bd4b-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8bd4b-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8bd4b-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8bd4b-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-120">The default value is 10.</span></span>

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

### <span data-ttu-id="8bd4b-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8bd4b-121">-Context</span></span>
<span data-ttu-id="8bd4b-122">Specifica un contesto per il contenitore che si vuole rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="8bd4b-123">Puoi usare il cmdlet New-AzureStorageContext per crearlo.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="8bd4b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8bd4b-124">-Force</span></span>
<span data-ttu-id="8bd4b-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8bd4b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bd4b-126">-Name</span></span>
<span data-ttu-id="8bd4b-127">Specifica il nome del contenitore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-127">Specifies the name of the container to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd4b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bd4b-128">-PassThru</span></span>
<span data-ttu-id="8bd4b-129">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8bd4b-130">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8bd4b-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8bd4b-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8bd4b-132">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="8bd4b-133">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="8bd4b-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8bd4b-134">-Confirm</span></span>
<span data-ttu-id="8bd4b-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bd4b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bd4b-136">-WhatIf</span></span>
<span data-ttu-id="8bd4b-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bd4b-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bd4b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd4b-139">CommonParameters</span></span>
<span data-ttu-id="8bd4b-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd4b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd4b-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bd4b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd4b-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8bd4b-142">INPUTS</span></span>

## <span data-ttu-id="8bd4b-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bd4b-143">OUTPUTS</span></span>

## <span data-ttu-id="8bd4b-144">Note</span><span class="sxs-lookup"><span data-stu-id="8bd4b-144">NOTES</span></span>

## <span data-ttu-id="8bd4b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bd4b-145">RELATED LINKS</span></span>

[<span data-ttu-id="8bd4b-146">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8bd4b-146">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="8bd4b-147">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8bd4b-147">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)
