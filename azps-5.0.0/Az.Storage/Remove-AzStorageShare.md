---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: d51980303d4cb0bcd3ba7ec9e4f976634d37c689
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193758"
---
# <span data-ttu-id="c2ba7-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c2ba7-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="c2ba7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ba7-103">Elimina una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-103">Deletes a file share.</span></span>

## <span data-ttu-id="c2ba7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2ba7-104">SYNTAX</span></span>

### <span data-ttu-id="c2ba7-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2ba7-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2ba7-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="c2ba7-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2ba7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2ba7-107">DESCRIPTION</span></span>
<span data-ttu-id="c2ba7-108">Il cmdlet **Remove-AzStorageShare** Elimina una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="c2ba7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2ba7-109">EXAMPLES</span></span>

### <span data-ttu-id="c2ba7-110">Esempio 1: rimuovere una condivisione file</span><span class="sxs-lookup"><span data-stu-id="c2ba7-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="c2ba7-111">Questo comando rimuove la condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="c2ba7-112">Esempio 2: rimuovere una condivisione file e tutti gli snapshot</span><span class="sxs-lookup"><span data-stu-id="c2ba7-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="c2ba7-113">Questo comando rimuove la condivisione file denominata ContosoShare06 e tutti gli snapshot.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="c2ba7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2ba7-114">PARAMETERS</span></span>

### <span data-ttu-id="c2ba7-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c2ba7-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c2ba7-116">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c2ba7-117">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c2ba7-118">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c2ba7-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c2ba7-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c2ba7-120">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c2ba7-121">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c2ba7-122">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c2ba7-123">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c2ba7-124">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-124">The default value is 10.</span></span>

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

### <span data-ttu-id="c2ba7-125">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c2ba7-125">-Context</span></span>
<span data-ttu-id="c2ba7-126">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c2ba7-127">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="c2ba7-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ba7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ba7-128">-DefaultProfile</span></span>
<span data-ttu-id="c2ba7-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2ba7-130">-Force</span><span class="sxs-lookup"><span data-stu-id="c2ba7-130">-Force</span></span>
<span data-ttu-id="c2ba7-131">Forza per rimuovere la condivisione con tutti gli snapshot e tutto il contenuto.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="c2ba7-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="c2ba7-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="c2ba7-133">Rimuovere la condivisione di file con tutti gli snapshot</span><span class="sxs-lookup"><span data-stu-id="c2ba7-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="c2ba7-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2ba7-134">-Name</span></span>
<span data-ttu-id="c2ba7-135">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="c2ba7-136">Questo cmdlet elimina la condivisione di file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ba7-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2ba7-137">-PassThru</span></span>
<span data-ttu-id="c2ba7-138">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c2ba7-139">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c2ba7-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c2ba7-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c2ba7-141">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c2ba7-142">-Condividi</span><span class="sxs-lookup"><span data-stu-id="c2ba7-142">-Share</span></span>
<span data-ttu-id="c2ba7-143">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="c2ba7-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="c2ba7-144">Questo cmdlet rimuove l'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="c2ba7-145">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="c2ba7-146">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-146">This object contains the storage context.</span></span>
<span data-ttu-id="c2ba7-147">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="c2ba7-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ba7-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2ba7-148">-Confirm</span></span>
<span data-ttu-id="c2ba7-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ba7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ba7-150">-WhatIf</span></span>
<span data-ttu-id="c2ba7-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2ba7-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ba7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ba7-153">CommonParameters</span></span>
<span data-ttu-id="c2ba7-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ba7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ba7-155">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2ba7-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ba7-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2ba7-156">INPUTS</span></span>

### <span data-ttu-id="c2ba7-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c2ba7-157">System.String</span></span>

### <span data-ttu-id="c2ba7-158">Microsoft. Azure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="c2ba7-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="c2ba7-159">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c2ba7-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c2ba7-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2ba7-160">OUTPUTS</span></span>

### <span data-ttu-id="c2ba7-161">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="c2ba7-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="c2ba7-162">Note</span><span class="sxs-lookup"><span data-stu-id="c2ba7-162">NOTES</span></span>

## <span data-ttu-id="c2ba7-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2ba7-163">RELATED LINKS</span></span>

[<span data-ttu-id="c2ba7-164">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c2ba7-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="c2ba7-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c2ba7-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c2ba7-166">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c2ba7-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)
