---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: 6f1d2c966ebd80d350b77401fee00aaf547cd932
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862106"
---
# <span data-ttu-id="df7e8-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="df7e8-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="df7e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df7e8-102">SYNOPSIS</span></span>
<span data-ttu-id="df7e8-103">Rimuove il contenitore di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="df7e8-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="df7e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df7e8-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df7e8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df7e8-105">DESCRIPTION</span></span>
<span data-ttu-id="df7e8-106">Il cmdlet **Remove-AzStorageContainer** rimuove il contenitore di archiviazione specificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="df7e8-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="df7e8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df7e8-107">EXAMPLES</span></span>

### <span data-ttu-id="df7e8-108">Esempio 1: rimuovere un contenitore</span><span class="sxs-lookup"><span data-stu-id="df7e8-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="df7e8-109">In questo esempio viene rimosso un contenitore denominato MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="df7e8-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="df7e8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df7e8-110">PARAMETERS</span></span>

### <span data-ttu-id="df7e8-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="df7e8-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="df7e8-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="df7e8-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="df7e8-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="df7e8-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="df7e8-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="df7e8-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="df7e8-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="df7e8-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="df7e8-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="df7e8-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="df7e8-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="df7e8-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="df7e8-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="df7e8-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="df7e8-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="df7e8-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="df7e8-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="df7e8-120">The default value is 10.</span></span>

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

### <span data-ttu-id="df7e8-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="df7e8-121">-Context</span></span>
<span data-ttu-id="df7e8-122">Specifica un contesto per il contenitore che si vuole rimuovere.</span><span class="sxs-lookup"><span data-stu-id="df7e8-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="df7e8-123">Puoi usare il cmdlet New-AzStorageContext per crearlo.</span><span class="sxs-lookup"><span data-stu-id="df7e8-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="df7e8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7e8-124">-DefaultProfile</span></span>
<span data-ttu-id="df7e8-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df7e8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df7e8-126">-Force</span><span class="sxs-lookup"><span data-stu-id="df7e8-126">-Force</span></span>
<span data-ttu-id="df7e8-127">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="df7e8-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="df7e8-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="df7e8-128">-Name</span></span>
<span data-ttu-id="df7e8-129">Specifica il nome del contenitore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="df7e8-129">Specifies the name of the container to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df7e8-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df7e8-130">-PassThru</span></span>
<span data-ttu-id="df7e8-131">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="df7e8-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="df7e8-132">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="df7e8-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="df7e8-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="df7e8-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="df7e8-134">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="df7e8-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="df7e8-135">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="df7e8-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="df7e8-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="df7e8-136">-Confirm</span></span>
<span data-ttu-id="df7e8-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df7e8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df7e8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df7e8-138">-WhatIf</span></span>
<span data-ttu-id="df7e8-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df7e8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df7e8-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df7e8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df7e8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7e8-141">CommonParameters</span></span>
<span data-ttu-id="df7e8-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df7e8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7e8-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df7e8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7e8-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df7e8-144">INPUTS</span></span>

### <span data-ttu-id="df7e8-145">System. String</span><span class="sxs-lookup"><span data-stu-id="df7e8-145">System.String</span></span>

### <span data-ttu-id="df7e8-146">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="df7e8-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="df7e8-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df7e8-147">OUTPUTS</span></span>

### <span data-ttu-id="df7e8-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df7e8-148">System.Boolean</span></span>

## <span data-ttu-id="df7e8-149">Note</span><span class="sxs-lookup"><span data-stu-id="df7e8-149">NOTES</span></span>

## <span data-ttu-id="df7e8-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df7e8-150">RELATED LINKS</span></span>

[<span data-ttu-id="df7e8-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="df7e8-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="df7e8-152">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="df7e8-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
