---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: a6ea7a2686d084b241e1ba3ff5c513c0d03128c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207771"
---
# <span data-ttu-id="4668e-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4668e-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="4668e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4668e-102">SYNOPSIS</span></span>
<span data-ttu-id="4668e-103">Rimuove il contenitore di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="4668e-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="4668e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4668e-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4668e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4668e-105">DESCRIPTION</span></span>
<span data-ttu-id="4668e-106">Il cmdlet **Remove-AzStorageContainer** rimuove il contenitore di archiviazione specificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="4668e-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="4668e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4668e-107">EXAMPLES</span></span>

### <span data-ttu-id="4668e-108">Esempio 1: Rimuovere un contenitore</span><span class="sxs-lookup"><span data-stu-id="4668e-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="4668e-109">Questo esempio rimuove un contenitore denominato MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="4668e-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="4668e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4668e-110">PARAMETERS</span></span>

### <span data-ttu-id="4668e-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4668e-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4668e-112">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="4668e-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4668e-113">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4668e-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4668e-114">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4668e-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4668e-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4668e-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4668e-116">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="4668e-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4668e-117">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="4668e-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4668e-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="4668e-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4668e-119">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="4668e-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4668e-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="4668e-120">The default value is 10.</span></span>

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

### <span data-ttu-id="4668e-121">-Context</span><span class="sxs-lookup"><span data-stu-id="4668e-121">-Context</span></span>
<span data-ttu-id="4668e-122">Specifica un contesto per il contenitore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4668e-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="4668e-123">È possibile usare il cmdlet New-AzStorageContext per crearlo.</span><span class="sxs-lookup"><span data-stu-id="4668e-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="4668e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4668e-124">-DefaultProfile</span></span>
<span data-ttu-id="4668e-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4668e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4668e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="4668e-126">-Force</span></span>
<span data-ttu-id="4668e-127">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="4668e-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4668e-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4668e-128">-Name</span></span>
<span data-ttu-id="4668e-129">Specifica il nome del contenitore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4668e-129">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="4668e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4668e-130">-PassThru</span></span>
<span data-ttu-id="4668e-131">Indica che questo cmdlet restituisce un valore **booleano** che riflette l'esito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4668e-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4668e-132">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4668e-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4668e-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4668e-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4668e-134">Specifica l'intervallo di timeout del lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="4668e-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="4668e-135">Se prima dell'elaborazione della richiesta da parte del servizio è trascorso l'intervallo specificato, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4668e-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="4668e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4668e-136">-Confirm</span></span>
<span data-ttu-id="4668e-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4668e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4668e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4668e-138">-WhatIf</span></span>
<span data-ttu-id="4668e-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4668e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4668e-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4668e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4668e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4668e-141">CommonParameters</span></span>
<span data-ttu-id="4668e-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4668e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4668e-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4668e-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4668e-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="4668e-144">INPUTS</span></span>

### <span data-ttu-id="4668e-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4668e-145">System.String</span></span>

### <span data-ttu-id="4668e-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4668e-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4668e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4668e-147">OUTPUTS</span></span>

### <span data-ttu-id="4668e-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4668e-148">System.Boolean</span></span>

## <span data-ttu-id="4668e-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="4668e-149">NOTES</span></span>

## <span data-ttu-id="4668e-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4668e-150">RELATED LINKS</span></span>

[<span data-ttu-id="4668e-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4668e-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="4668e-152">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4668e-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
