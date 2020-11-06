---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
ms.openlocfilehash: 4752612120da1f89729299c41df1b7af78580f92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509471"
---
# <span data-ttu-id="75237-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="75237-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="75237-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75237-102">SYNOPSIS</span></span>
<span data-ttu-id="75237-103">Elimina un file.</span><span class="sxs-lookup"><span data-stu-id="75237-103">Deletes a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75237-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75237-104">SYNTAX</span></span>

### <span data-ttu-id="75237-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75237-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75237-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="75237-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75237-107">Directory</span><span class="sxs-lookup"><span data-stu-id="75237-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75237-108">File</span><span class="sxs-lookup"><span data-stu-id="75237-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75237-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75237-109">DESCRIPTION</span></span>
<span data-ttu-id="75237-110">Il cmdlet **Remove-AzureStorageFile** Elimina un file.</span><span class="sxs-lookup"><span data-stu-id="75237-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="75237-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75237-111">EXAMPLES</span></span>

### <span data-ttu-id="75237-112">Esempio 1: eliminare un file da una condivisione file</span><span class="sxs-lookup"><span data-stu-id="75237-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="75237-113">Questo comando Elimina il file denominato ContosoFile22 dalla condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="75237-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="75237-114">Esempio 2: ottenere un file da una condivisione file tramite un oggetto condivisione file</span><span class="sxs-lookup"><span data-stu-id="75237-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="75237-115">Questo comando usa il cmdlet **Get-AzureStorageShare** per ottenere la condivisione di file denominata ContosoShare06 e quindi passa tale oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="75237-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="75237-116">Il comando corrente Elimina il file denominato ContosoFile22 da ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="75237-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="75237-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75237-117">PARAMETERS</span></span>

### <span data-ttu-id="75237-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="75237-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="75237-119">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="75237-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="75237-120">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="75237-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="75237-121">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="75237-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="75237-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="75237-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="75237-123">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="75237-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="75237-124">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="75237-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="75237-125">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="75237-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="75237-126">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="75237-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="75237-127">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="75237-127">The default value is 10.</span></span>

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

### <span data-ttu-id="75237-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="75237-128">-Context</span></span>
<span data-ttu-id="75237-129">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="75237-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="75237-130">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="75237-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="75237-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75237-131">-DefaultProfile</span></span>
<span data-ttu-id="75237-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75237-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75237-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="75237-133">-Directory</span></span>
<span data-ttu-id="75237-134">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="75237-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="75237-135">Questo cmdlet consente di rimuovere un file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="75237-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75237-136">-File</span><span class="sxs-lookup"><span data-stu-id="75237-136">-File</span></span>
<span data-ttu-id="75237-137">Specifica un file come oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="75237-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="75237-138">Questo cmdlet consente di rimuovere il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="75237-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="75237-139">Per ottenere un oggetto **CloudFile** , usa il cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="75237-139">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75237-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75237-140">-PassThru</span></span>
<span data-ttu-id="75237-141">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="75237-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="75237-142">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="75237-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="75237-143">-Path</span><span class="sxs-lookup"><span data-stu-id="75237-143">-Path</span></span>
<span data-ttu-id="75237-144">Specifica il percorso di un file.</span><span class="sxs-lookup"><span data-stu-id="75237-144">Specifies the path of a file.</span></span>
<span data-ttu-id="75237-145">Questo cmdlet elimina il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="75237-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75237-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="75237-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="75237-147">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="75237-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="75237-148">-Condividi</span><span class="sxs-lookup"><span data-stu-id="75237-148">-Share</span></span>
<span data-ttu-id="75237-149">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="75237-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="75237-150">Questo cmdlet consente di rimuovere il file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="75237-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="75237-151">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="75237-151">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="75237-152">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="75237-152">This object contains the storage context.</span></span>
<span data-ttu-id="75237-153">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="75237-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="75237-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="75237-154">-ShareName</span></span>
<span data-ttu-id="75237-155">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="75237-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="75237-156">Questo cmdlet consente di rimuovere il file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="75237-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75237-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="75237-157">-Confirm</span></span>
<span data-ttu-id="75237-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75237-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75237-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75237-159">-WhatIf</span></span>
<span data-ttu-id="75237-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75237-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75237-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75237-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75237-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75237-162">CommonParameters</span></span>
<span data-ttu-id="75237-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75237-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75237-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75237-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75237-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75237-165">INPUTS</span></span>

### <span data-ttu-id="75237-166">Microsoft. WindowsAzure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="75237-166">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="75237-167">Parametri: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="75237-167">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="75237-168">Microsoft. WindowsAzure. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="75237-168">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="75237-169">Parameters: directory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="75237-169">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="75237-170">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="75237-170">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="75237-171">Parameters: file (ByValue)</span><span class="sxs-lookup"><span data-stu-id="75237-171">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="75237-172">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="75237-172">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="75237-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75237-173">OUTPUTS</span></span>

### <span data-ttu-id="75237-174">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="75237-174">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="75237-175">Note</span><span class="sxs-lookup"><span data-stu-id="75237-175">NOTES</span></span>

## <span data-ttu-id="75237-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75237-176">RELATED LINKS</span></span>

[<span data-ttu-id="75237-177">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="75237-177">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="75237-178">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="75237-178">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="75237-179">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="75237-179">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
