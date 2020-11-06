---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24b4ddfa86027885b5094b164f24da36e9604900
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491313"
---
# <span data-ttu-id="ebae0-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="ebae0-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="ebae0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ebae0-102">SYNOPSIS</span></span>
<span data-ttu-id="ebae0-103">Elimina un file.</span><span class="sxs-lookup"><span data-stu-id="ebae0-103">Deletes a file.</span></span>

## <span data-ttu-id="ebae0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ebae0-104">SYNTAX</span></span>

### <span data-ttu-id="ebae0-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ebae0-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebae0-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="ebae0-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebae0-107">Directory</span><span class="sxs-lookup"><span data-stu-id="ebae0-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebae0-108">File</span><span class="sxs-lookup"><span data-stu-id="ebae0-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebae0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebae0-109">DESCRIPTION</span></span>
<span data-ttu-id="ebae0-110">Il cmdlet **Remove-AzureStorageFile** Elimina un file.</span><span class="sxs-lookup"><span data-stu-id="ebae0-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="ebae0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ebae0-111">EXAMPLES</span></span>

### <span data-ttu-id="ebae0-112">Esempio 1: eliminare un file da una condivisione file</span><span class="sxs-lookup"><span data-stu-id="ebae0-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="ebae0-113">Questo comando Elimina il file denominato ContosoFile22 dalla condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="ebae0-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="ebae0-114">Esempio 2: ottenere un file da una condivisione file tramite un oggetto condivisione file</span><span class="sxs-lookup"><span data-stu-id="ebae0-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="ebae0-115">Questo comando usa il cmdlet **Get-AzureStorageShare** per ottenere la condivisione di file denominata ContosoShare06 e quindi passa tale oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="ebae0-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ebae0-116">Il comando corrente Elimina il file denominato ContosoFile22 da ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="ebae0-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="ebae0-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ebae0-117">PARAMETERS</span></span>

### <span data-ttu-id="ebae0-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ebae0-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ebae0-119">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="ebae0-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ebae0-120">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ebae0-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ebae0-121">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ebae0-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ebae0-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ebae0-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ebae0-123">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="ebae0-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ebae0-124">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="ebae0-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ebae0-125">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="ebae0-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ebae0-126">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ebae0-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ebae0-127">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="ebae0-127">The default value is 10.</span></span>

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

### <span data-ttu-id="ebae0-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ebae0-128">-Context</span></span>
<span data-ttu-id="ebae0-129">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ebae0-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ebae0-130">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="ebae0-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebae0-131">-Directory</span><span class="sxs-lookup"><span data-stu-id="ebae0-131">-Directory</span></span>
<span data-ttu-id="ebae0-132">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="ebae0-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="ebae0-133">Questo cmdlet consente di rimuovere un file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ebae0-133">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebae0-134">-File</span><span class="sxs-lookup"><span data-stu-id="ebae0-134">-File</span></span>
<span data-ttu-id="ebae0-135">Specifica un file come oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="ebae0-135">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="ebae0-136">Questo cmdlet consente di rimuovere il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ebae0-136">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="ebae0-137">Per ottenere un oggetto **CloudFile** , usa il cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="ebae0-137">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebae0-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebae0-138">-PassThru</span></span>
<span data-ttu-id="ebae0-139">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ebae0-139">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ebae0-140">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ebae0-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ebae0-141">-Path</span><span class="sxs-lookup"><span data-stu-id="ebae0-141">-Path</span></span>
<span data-ttu-id="ebae0-142">Specifica il percorso di un file.</span><span class="sxs-lookup"><span data-stu-id="ebae0-142">Specifies the path of a file.</span></span>
<span data-ttu-id="ebae0-143">Questo cmdlet elimina il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ebae0-143">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebae0-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ebae0-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ebae0-145">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="ebae0-145">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ebae0-146">-Condividi</span><span class="sxs-lookup"><span data-stu-id="ebae0-146">-Share</span></span>
<span data-ttu-id="ebae0-147">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="ebae0-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="ebae0-148">Questo cmdlet consente di rimuovere il file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="ebae0-148">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="ebae0-149">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="ebae0-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="ebae0-150">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ebae0-150">This object contains the storage context.</span></span>
<span data-ttu-id="ebae0-151">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="ebae0-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebae0-152">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ebae0-152">-ShareName</span></span>
<span data-ttu-id="ebae0-153">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="ebae0-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="ebae0-154">Questo cmdlet consente di rimuovere il file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="ebae0-154">This cmdlet removes the file in the share this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebae0-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ebae0-155">-Confirm</span></span>
<span data-ttu-id="ebae0-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebae0-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebae0-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebae0-157">-WhatIf</span></span>
<span data-ttu-id="ebae0-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebae0-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebae0-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebae0-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebae0-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebae0-160">CommonParameters</span></span>
<span data-ttu-id="ebae0-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebae0-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebae0-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebae0-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebae0-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ebae0-163">INPUTS</span></span>

## <span data-ttu-id="ebae0-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ebae0-164">OUTPUTS</span></span>

## <span data-ttu-id="ebae0-165">Note</span><span class="sxs-lookup"><span data-stu-id="ebae0-165">NOTES</span></span>

## <span data-ttu-id="ebae0-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ebae0-166">RELATED LINKS</span></span>

[<span data-ttu-id="ebae0-167">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="ebae0-167">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="ebae0-168">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="ebae0-168">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="ebae0-169">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ebae0-169">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)