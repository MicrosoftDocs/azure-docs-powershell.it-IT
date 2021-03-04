---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 4d2828351c4007e57fd8c7534e88aa3be5543199
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990749"
---
# <span data-ttu-id="38ed2-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38ed2-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="38ed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="38ed2-103">Rimuove un criterio di accesso archiviato da un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="38ed2-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="38ed2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38ed2-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38ed2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38ed2-105">DESCRIPTION</span></span>
<span data-ttu-id="38ed2-106">Il cmdlet **Remove-AzStorageContainerStoredAccessPolicy** rimuove un criterio di accesso archiviato da un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="38ed2-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="38ed2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38ed2-107">EXAMPLES</span></span>

### <span data-ttu-id="38ed2-108">Esempio 1: Rimuovere un criterio di accesso archiviato da un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="38ed2-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="38ed2-109">Questo comando rimuove un criterio di accesso denominato Policy03 dal contenitore archiviato denominato MyContainer.</span><span class="sxs-lookup"><span data-stu-id="38ed2-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="38ed2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38ed2-110">PARAMETERS</span></span>

### <span data-ttu-id="38ed2-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="38ed2-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="38ed2-112">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="38ed2-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="38ed2-113">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="38ed2-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="38ed2-114">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="38ed2-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="38ed2-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="38ed2-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="38ed2-116">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="38ed2-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="38ed2-117">È possibile usare questo parametro per limitare la simultaneità per limitare l'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="38ed2-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="38ed2-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="38ed2-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="38ed2-119">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="38ed2-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="38ed2-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="38ed2-120">The default value is 10.</span></span>

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

### <span data-ttu-id="38ed2-121">-Container</span><span class="sxs-lookup"><span data-stu-id="38ed2-121">-Container</span></span>
<span data-ttu-id="38ed2-122">Specifica il nome del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="38ed2-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="38ed2-123">-Context</span><span class="sxs-lookup"><span data-stu-id="38ed2-123">-Context</span></span>
<span data-ttu-id="38ed2-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="38ed2-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="38ed2-125">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="38ed2-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="38ed2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ed2-126">-DefaultProfile</span></span>
<span data-ttu-id="38ed2-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38ed2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ed2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38ed2-128">-PassThru</span></span>
<span data-ttu-id="38ed2-129">Indica che questo cmdlet restituisce un valore **booleano** che riflette il successo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="38ed2-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="38ed2-130">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="38ed2-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="38ed2-131">-Policy</span><span class="sxs-lookup"><span data-stu-id="38ed2-131">-Policy</span></span>
<span data-ttu-id="38ed2-132">Specifica il nome dei criteri di accesso archiviato rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38ed2-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="38ed2-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="38ed2-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="38ed2-134">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="38ed2-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="38ed2-135">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="38ed2-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="38ed2-136">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="38ed2-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="38ed2-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38ed2-137">-Confirm</span></span>
<span data-ttu-id="38ed2-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38ed2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ed2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ed2-139">-WhatIf</span></span>
<span data-ttu-id="38ed2-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38ed2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ed2-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38ed2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ed2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ed2-142">CommonParameters</span></span>
<span data-ttu-id="38ed2-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38ed2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ed2-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38ed2-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ed2-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="38ed2-145">INPUTS</span></span>

### <span data-ttu-id="38ed2-146">System.String</span><span class="sxs-lookup"><span data-stu-id="38ed2-146">System.String</span></span>

### <span data-ttu-id="38ed2-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="38ed2-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="38ed2-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38ed2-148">OUTPUTS</span></span>

### <span data-ttu-id="38ed2-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38ed2-149">System.Boolean</span></span>

## <span data-ttu-id="38ed2-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="38ed2-150">NOTES</span></span>

## <span data-ttu-id="38ed2-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38ed2-151">RELATED LINKS</span></span>

[<span data-ttu-id="38ed2-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38ed2-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="38ed2-153">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38ed2-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="38ed2-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="38ed2-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="38ed2-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38ed2-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
