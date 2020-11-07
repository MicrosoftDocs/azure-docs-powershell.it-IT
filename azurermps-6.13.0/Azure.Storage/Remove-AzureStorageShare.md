---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
ms.openlocfilehash: 43a1a18675a662e30e88dd2d96f2fc901ffab8dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686985"
---
# <span data-ttu-id="bfa8b-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bfa8b-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="bfa8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bfa8b-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa8b-103">Elimina una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfa8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfa8b-104">SYNTAX</span></span>

### <span data-ttu-id="bfa8b-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bfa8b-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfa8b-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="bfa8b-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bfa8b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfa8b-107">DESCRIPTION</span></span>
<span data-ttu-id="bfa8b-108">Il cmdlet **Remove-AzureStorageShare** Elimina una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="bfa8b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfa8b-109">EXAMPLES</span></span>

### <span data-ttu-id="bfa8b-110">Esempio 1: rimuovere una condivisione file</span><span class="sxs-lookup"><span data-stu-id="bfa8b-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="bfa8b-111">Questo comando rimuove la condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="bfa8b-112">Esempio 2: rimuovere una condivisione file e tutti gli snapshot</span><span class="sxs-lookup"><span data-stu-id="bfa8b-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="bfa8b-113">Questo comando rimuove la condivisione file denominata ContosoShare06 e tutti gli snapshot.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="bfa8b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bfa8b-114">PARAMETERS</span></span>

### <span data-ttu-id="bfa8b-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bfa8b-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bfa8b-116">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bfa8b-117">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bfa8b-118">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bfa8b-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bfa8b-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bfa8b-120">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bfa8b-121">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bfa8b-122">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bfa8b-123">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bfa8b-124">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-124">The default value is 10.</span></span>

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

### <span data-ttu-id="bfa8b-125">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bfa8b-125">-Context</span></span>
<span data-ttu-id="bfa8b-126">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bfa8b-127">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa8b-127">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="bfa8b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa8b-128">-DefaultProfile</span></span>
<span data-ttu-id="bfa8b-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfa8b-130">-Force</span><span class="sxs-lookup"><span data-stu-id="bfa8b-130">-Force</span></span>
<span data-ttu-id="bfa8b-131">Forza per rimuovere la condivisione con tutti gli snapshot e tutto il contenuto.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="bfa8b-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="bfa8b-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="bfa8b-133">Rimuovere la condivisione di file con tutti gli snapshot</span><span class="sxs-lookup"><span data-stu-id="bfa8b-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="bfa8b-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfa8b-134">-Name</span></span>
<span data-ttu-id="bfa8b-135">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="bfa8b-136">Questo cmdlet elimina la condivisione di file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="bfa8b-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfa8b-137">-PassThru</span></span>
<span data-ttu-id="bfa8b-138">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="bfa8b-139">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="bfa8b-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bfa8b-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bfa8b-141">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bfa8b-142">-Condividi</span><span class="sxs-lookup"><span data-stu-id="bfa8b-142">-Share</span></span>
<span data-ttu-id="bfa8b-143">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="bfa8b-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="bfa8b-144">Questo cmdlet rimuove l'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="bfa8b-145">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="bfa8b-146">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-146">This object contains the storage context.</span></span>
<span data-ttu-id="bfa8b-147">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="bfa8b-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa8b-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bfa8b-148">-Confirm</span></span>
<span data-ttu-id="bfa8b-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfa8b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfa8b-150">-WhatIf</span></span>
<span data-ttu-id="bfa8b-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfa8b-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfa8b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa8b-153">CommonParameters</span></span>
<span data-ttu-id="bfa8b-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa8b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa8b-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfa8b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa8b-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bfa8b-156">INPUTS</span></span>

### <span data-ttu-id="bfa8b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="bfa8b-157">System.String</span></span>

### <span data-ttu-id="bfa8b-158">Microsoft. WindowsAzure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="bfa8b-158">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="bfa8b-159">Parametri: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bfa8b-159">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="bfa8b-160">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bfa8b-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bfa8b-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfa8b-161">OUTPUTS</span></span>

### <span data-ttu-id="bfa8b-162">Microsoft. WindowsAzure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="bfa8b-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="bfa8b-163">Note</span><span class="sxs-lookup"><span data-stu-id="bfa8b-163">NOTES</span></span>

## <span data-ttu-id="bfa8b-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfa8b-164">RELATED LINKS</span></span>

[<span data-ttu-id="bfa8b-165">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bfa8b-165">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="bfa8b-166">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bfa8b-166">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="bfa8b-167">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bfa8b-167">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)