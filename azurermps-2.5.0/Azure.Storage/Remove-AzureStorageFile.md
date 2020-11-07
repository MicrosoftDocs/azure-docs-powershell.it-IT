---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragefile
schema: 2.0.0
ms.openlocfilehash: cfb5a3255a91c7a7206ba0729c20e4d0c68c3ea2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866933"
---
# <span data-ttu-id="6a0f5-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="6a0f5-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="6a0f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="6a0f5-103">Elimina un file.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-103">Deletes a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a0f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a0f5-104">SYNTAX</span></span>

### <span data-ttu-id="6a0f5-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a0f5-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a0f5-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="6a0f5-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a0f5-107">Directory</span><span class="sxs-lookup"><span data-stu-id="6a0f5-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a0f5-108">File</span><span class="sxs-lookup"><span data-stu-id="6a0f5-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a0f5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a0f5-109">DESCRIPTION</span></span>
<span data-ttu-id="6a0f5-110">Il cmdlet **Remove-AzureStorageFile** Elimina un file.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="6a0f5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a0f5-111">EXAMPLES</span></span>

### <span data-ttu-id="6a0f5-112">Esempio 1: eliminare un file da una condivisione file</span><span class="sxs-lookup"><span data-stu-id="6a0f5-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="6a0f5-113">Questo comando Elimina il file denominato ContosoFile22 dalla condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="6a0f5-114">Esempio 2: ottenere un file da una condivisione file tramite un oggetto condivisione file</span><span class="sxs-lookup"><span data-stu-id="6a0f5-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="6a0f5-115">Questo comando usa il cmdlet **Get-AzureStorageShare** per ottenere la condivisione di file denominata ContosoShare06 e quindi passa tale oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6a0f5-116">Il comando corrente Elimina il file denominato ContosoFile22 da ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="6a0f5-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a0f5-117">PARAMETERS</span></span>

### <span data-ttu-id="6a0f5-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6a0f5-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6a0f5-119">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6a0f5-120">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6a0f5-121">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6a0f5-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6a0f5-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6a0f5-123">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6a0f5-124">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6a0f5-125">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6a0f5-126">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6a0f5-127">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-127">The default value is 10.</span></span>

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

### <span data-ttu-id="6a0f5-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="6a0f5-128">-Context</span></span>
<span data-ttu-id="6a0f5-129">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6a0f5-130">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="6a0f5-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="6a0f5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a0f5-131">-DefaultProfile</span></span>
<span data-ttu-id="6a0f5-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a0f5-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="6a0f5-133">-Directory</span></span>
<span data-ttu-id="6a0f5-134">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="6a0f5-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="6a0f5-135">Questo cmdlet consente di rimuovere un file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="6a0f5-136">-File</span><span class="sxs-lookup"><span data-stu-id="6a0f5-136">-File</span></span>
<span data-ttu-id="6a0f5-137">Specifica un file come oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="6a0f5-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="6a0f5-138">Questo cmdlet consente di rimuovere il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="6a0f5-139">Per ottenere un oggetto **CloudFile** , usa il cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-139">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="6a0f5-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a0f5-140">-PassThru</span></span>
<span data-ttu-id="6a0f5-141">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6a0f5-142">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6a0f5-143">-Path</span><span class="sxs-lookup"><span data-stu-id="6a0f5-143">-Path</span></span>
<span data-ttu-id="6a0f5-144">Specifica il percorso di un file.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-144">Specifies the path of a file.</span></span>
<span data-ttu-id="6a0f5-145">Questo cmdlet elimina il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="6a0f5-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6a0f5-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6a0f5-147">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="6a0f5-148">-Condividi</span><span class="sxs-lookup"><span data-stu-id="6a0f5-148">-Share</span></span>
<span data-ttu-id="6a0f5-149">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="6a0f5-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="6a0f5-150">Questo cmdlet consente di rimuovere il file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="6a0f5-151">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-151">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="6a0f5-152">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-152">This object contains the storage context.</span></span>
<span data-ttu-id="6a0f5-153">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="6a0f5-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="6a0f5-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="6a0f5-154">-ShareName</span></span>
<span data-ttu-id="6a0f5-155">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="6a0f5-156">Questo cmdlet consente di rimuovere il file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="6a0f5-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a0f5-157">-Confirm</span></span>
<span data-ttu-id="6a0f5-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a0f5-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a0f5-159">-WhatIf</span></span>
<span data-ttu-id="6a0f5-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a0f5-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a0f5-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a0f5-162">CommonParameters</span></span>
<span data-ttu-id="6a0f5-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a0f5-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a0f5-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a0f5-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a0f5-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a0f5-165">INPUTS</span></span>

### <span data-ttu-id="6a0f5-166">Microsoft. WindowsAzure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="6a0f5-166">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="6a0f5-167">Parametri: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6a0f5-167">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="6a0f5-168">Microsoft. WindowsAzure. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="6a0f5-168">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="6a0f5-169">Parameters: directory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6a0f5-169">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="6a0f5-170">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="6a0f5-170">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="6a0f5-171">Parameters: file (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6a0f5-171">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="6a0f5-172">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6a0f5-172">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6a0f5-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a0f5-173">OUTPUTS</span></span>

### <span data-ttu-id="6a0f5-174">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="6a0f5-174">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="6a0f5-175">Note</span><span class="sxs-lookup"><span data-stu-id="6a0f5-175">NOTES</span></span>

## <span data-ttu-id="6a0f5-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a0f5-176">RELATED LINKS</span></span>

[<span data-ttu-id="6a0f5-177">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="6a0f5-177">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="6a0f5-178">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="6a0f5-178">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="6a0f5-179">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6a0f5-179">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
