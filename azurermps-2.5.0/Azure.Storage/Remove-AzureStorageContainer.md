---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainer
schema: 2.0.0
ms.openlocfilehash: 24eba8b6aeedb2f240fbd7da16b1b7a76ee9d759
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866932"
---
# <span data-ttu-id="00ead-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="00ead-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="00ead-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00ead-102">SYNOPSIS</span></span>
<span data-ttu-id="00ead-103">Rimuove il contenitore di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="00ead-103">Removes the specified storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00ead-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00ead-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00ead-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00ead-105">DESCRIPTION</span></span>
<span data-ttu-id="00ead-106">Il cmdlet **Remove-AzureStorageContainer** rimuove il contenitore di archiviazione specificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="00ead-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="00ead-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00ead-107">EXAMPLES</span></span>

### <span data-ttu-id="00ead-108">Esempio 1: rimuovere un contenitore</span><span class="sxs-lookup"><span data-stu-id="00ead-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="00ead-109">In questo esempio viene rimosso un contenitore denominato MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="00ead-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="00ead-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00ead-110">PARAMETERS</span></span>

### <span data-ttu-id="00ead-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="00ead-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="00ead-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="00ead-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="00ead-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="00ead-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="00ead-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="00ead-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="00ead-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="00ead-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="00ead-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="00ead-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="00ead-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="00ead-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="00ead-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="00ead-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="00ead-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="00ead-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="00ead-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="00ead-120">The default value is 10.</span></span>

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

### <span data-ttu-id="00ead-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="00ead-121">-Context</span></span>
<span data-ttu-id="00ead-122">Specifica un contesto per il contenitore che si vuole rimuovere.</span><span class="sxs-lookup"><span data-stu-id="00ead-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="00ead-123">Puoi usare il cmdlet New-AzureStorageContext per crearlo.</span><span class="sxs-lookup"><span data-stu-id="00ead-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="00ead-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ead-124">-DefaultProfile</span></span>
<span data-ttu-id="00ead-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00ead-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00ead-126">-Force</span><span class="sxs-lookup"><span data-stu-id="00ead-126">-Force</span></span>
<span data-ttu-id="00ead-127">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="00ead-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00ead-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="00ead-128">-Name</span></span>
<span data-ttu-id="00ead-129">Specifica il nome del contenitore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="00ead-129">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="00ead-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00ead-130">-PassThru</span></span>
<span data-ttu-id="00ead-131">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="00ead-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="00ead-132">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="00ead-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="00ead-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="00ead-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="00ead-134">Specifica l'intervallo di timeout lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="00ead-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="00ead-135">Se l'intervallo specificato trascorre prima che il servizio elabora la richiesta, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="00ead-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="00ead-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="00ead-136">-Confirm</span></span>
<span data-ttu-id="00ead-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00ead-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00ead-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00ead-138">-WhatIf</span></span>
<span data-ttu-id="00ead-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00ead-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00ead-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00ead-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00ead-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ead-141">CommonParameters</span></span>
<span data-ttu-id="00ead-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ead-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ead-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00ead-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ead-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00ead-144">INPUTS</span></span>

### <span data-ttu-id="00ead-145">System. String</span><span class="sxs-lookup"><span data-stu-id="00ead-145">System.String</span></span>

### <span data-ttu-id="00ead-146">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="00ead-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="00ead-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00ead-147">OUTPUTS</span></span>

### <span data-ttu-id="00ead-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="00ead-148">System.Boolean</span></span>

## <span data-ttu-id="00ead-149">Note</span><span class="sxs-lookup"><span data-stu-id="00ead-149">NOTES</span></span>

## <span data-ttu-id="00ead-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00ead-150">RELATED LINKS</span></span>

[<span data-ttu-id="00ead-151">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="00ead-151">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="00ead-152">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="00ead-152">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)
