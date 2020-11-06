---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd885e79fb4daf1eec9dd8958283be28e52f920f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490917"
---
# <span data-ttu-id="9855d-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="9855d-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="9855d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9855d-102">SYNOPSIS</span></span>
<span data-ttu-id="9855d-103">Elimina una directory.</span><span class="sxs-lookup"><span data-stu-id="9855d-103">Deletes a directory.</span></span>

## <span data-ttu-id="9855d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9855d-104">SYNTAX</span></span>

### <span data-ttu-id="9855d-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9855d-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9855d-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="9855d-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9855d-107">Directory</span><span class="sxs-lookup"><span data-stu-id="9855d-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9855d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9855d-108">DESCRIPTION</span></span>
<span data-ttu-id="9855d-109">Il cmdlet **Remove-AzureStorageDirectory** Elimina una directory.</span><span class="sxs-lookup"><span data-stu-id="9855d-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="9855d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9855d-110">EXAMPLES</span></span>

### <span data-ttu-id="9855d-111">Esempio 1: eliminare una cartella</span><span class="sxs-lookup"><span data-stu-id="9855d-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="9855d-112">Questo comando Elimina la cartella denominata ContosoWorkingFolder dalla condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="9855d-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="9855d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9855d-113">PARAMETERS</span></span>

### <span data-ttu-id="9855d-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9855d-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9855d-115">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="9855d-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9855d-116">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="9855d-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9855d-117">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9855d-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9855d-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9855d-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9855d-119">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="9855d-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9855d-120">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="9855d-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9855d-121">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="9855d-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9855d-122">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="9855d-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9855d-123">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="9855d-123">The default value is 10.</span></span>

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

### <span data-ttu-id="9855d-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9855d-124">-Context</span></span>
<span data-ttu-id="9855d-125">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9855d-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9855d-126">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="9855d-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9855d-127">-Directory</span><span class="sxs-lookup"><span data-stu-id="9855d-127">-Directory</span></span>
<span data-ttu-id="9855d-128">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="9855d-128">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="9855d-129">Questo cmdlet rimuove la cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9855d-129">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="9855d-130">Per ottenere una directory, usare il cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="9855d-130">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="9855d-131">Puoi anche usare il cmdlet **Get-AzureStorageFile** per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="9855d-131">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="9855d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9855d-132">-PassThru</span></span>
<span data-ttu-id="9855d-133">Indica che, se il cmdlet ha esito positivo, restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="9855d-133">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="9855d-134">Se specifichi questo parametro e se il cmdlet non riesce a causa di un valore non appropriato per il parametro _path_ , il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9855d-134">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="9855d-135">Se non specifichi questo parametro, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9855d-135">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9855d-136">-Path</span><span class="sxs-lookup"><span data-stu-id="9855d-136">-Path</span></span>
<span data-ttu-id="9855d-137">Specifica il percorso di una cartella.</span><span class="sxs-lookup"><span data-stu-id="9855d-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="9855d-138">Se la cartella specificata da questo parametro è vuota, questo cmdlet elimina quella cartella.</span><span class="sxs-lookup"><span data-stu-id="9855d-138">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="9855d-139">Se la cartella non è vuota, questo cmdlet non apporta alcuna modifica e restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9855d-139">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Directory
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9855d-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9855d-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9855d-141">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="9855d-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9855d-142">-Condividi</span><span class="sxs-lookup"><span data-stu-id="9855d-142">-Share</span></span>
<span data-ttu-id="9855d-143">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="9855d-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="9855d-144">Questo cmdlet consente di rimuovere una cartella sotto la condivisione di file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9855d-144">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="9855d-145">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="9855d-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="9855d-146">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9855d-146">This object contains the storage context.</span></span>
<span data-ttu-id="9855d-147">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="9855d-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="9855d-148">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9855d-148">-ShareName</span></span>
<span data-ttu-id="9855d-149">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="9855d-149">Specifies the name of the file share.</span></span>
<span data-ttu-id="9855d-150">Questo cmdlet consente di rimuovere una cartella sotto la condivisione di file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9855d-150">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="9855d-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9855d-151">-Confirm</span></span>
<span data-ttu-id="9855d-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9855d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9855d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9855d-153">-WhatIf</span></span>
<span data-ttu-id="9855d-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9855d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9855d-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9855d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9855d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9855d-156">CommonParameters</span></span>
<span data-ttu-id="9855d-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9855d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9855d-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9855d-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9855d-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9855d-159">INPUTS</span></span>

## <span data-ttu-id="9855d-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9855d-160">OUTPUTS</span></span>

## <span data-ttu-id="9855d-161">Note</span><span class="sxs-lookup"><span data-stu-id="9855d-161">NOTES</span></span>

## <span data-ttu-id="9855d-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9855d-162">RELATED LINKS</span></span>

[<span data-ttu-id="9855d-163">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9855d-163">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="9855d-164">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9855d-164">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="9855d-165">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="9855d-165">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
