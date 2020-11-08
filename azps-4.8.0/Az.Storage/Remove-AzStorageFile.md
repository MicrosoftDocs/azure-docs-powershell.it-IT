---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 99809e5115cb256b8e546334efce0e6e399be04f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191134"
---
# <span data-ttu-id="cb16d-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cb16d-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="cb16d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb16d-102">SYNOPSIS</span></span>
<span data-ttu-id="cb16d-103">Elimina un file.</span><span class="sxs-lookup"><span data-stu-id="cb16d-103">Deletes a file.</span></span>

## <span data-ttu-id="cb16d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb16d-104">SYNTAX</span></span>

### <span data-ttu-id="cb16d-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cb16d-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb16d-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="cb16d-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb16d-107">Directory</span><span class="sxs-lookup"><span data-stu-id="cb16d-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb16d-108">File</span><span class="sxs-lookup"><span data-stu-id="cb16d-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb16d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb16d-109">DESCRIPTION</span></span>
<span data-ttu-id="cb16d-110">Il cmdlet **Remove-AzStorageFile** Elimina un file.</span><span class="sxs-lookup"><span data-stu-id="cb16d-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="cb16d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb16d-111">EXAMPLES</span></span>

### <span data-ttu-id="cb16d-112">Esempio 1: eliminare un file da una condivisione file</span><span class="sxs-lookup"><span data-stu-id="cb16d-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="cb16d-113">Questo comando Elimina il file denominato ContosoFile22 dalla condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="cb16d-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="cb16d-114">Esempio 2: ottenere un file da una condivisione file tramite un oggetto condivisione file</span><span class="sxs-lookup"><span data-stu-id="cb16d-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="cb16d-115">Questo comando usa il cmdlet **Get-AzStorageShare** per ottenere la condivisione di file denominata ContosoShare06 e quindi passa tale oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="cb16d-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cb16d-116">Il comando corrente Elimina il file denominato ContosoFile22 da ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="cb16d-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="cb16d-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb16d-117">PARAMETERS</span></span>

### <span data-ttu-id="cb16d-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cb16d-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cb16d-119">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="cb16d-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cb16d-120">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="cb16d-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cb16d-121">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="cb16d-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cb16d-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cb16d-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cb16d-123">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="cb16d-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cb16d-124">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="cb16d-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cb16d-125">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="cb16d-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cb16d-126">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="cb16d-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cb16d-127">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="cb16d-127">The default value is 10.</span></span>

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

### <span data-ttu-id="cb16d-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="cb16d-128">-Context</span></span>
<span data-ttu-id="cb16d-129">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cb16d-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cb16d-130">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="cb16d-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="cb16d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb16d-131">-DefaultProfile</span></span>
<span data-ttu-id="cb16d-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb16d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb16d-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="cb16d-133">-Directory</span></span>
<span data-ttu-id="cb16d-134">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="cb16d-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="cb16d-135">Questo cmdlet consente di rimuovere un file nella cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cb16d-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb16d-136">-File</span><span class="sxs-lookup"><span data-stu-id="cb16d-136">-File</span></span>
<span data-ttu-id="cb16d-137">Specifica un file come oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="cb16d-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="cb16d-138">Questo cmdlet consente di rimuovere il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cb16d-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="cb16d-139">Per ottenere un oggetto **CloudFile** , usa il cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="cb16d-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb16d-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb16d-140">-PassThru</span></span>
<span data-ttu-id="cb16d-141">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="cb16d-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="cb16d-142">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cb16d-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="cb16d-143">-Path</span><span class="sxs-lookup"><span data-stu-id="cb16d-143">-Path</span></span>
<span data-ttu-id="cb16d-144">Specifica il percorso di un file.</span><span class="sxs-lookup"><span data-stu-id="cb16d-144">Specifies the path of a file.</span></span>
<span data-ttu-id="cb16d-145">Questo cmdlet elimina il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cb16d-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb16d-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cb16d-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cb16d-147">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="cb16d-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="cb16d-148">-Condividi</span><span class="sxs-lookup"><span data-stu-id="cb16d-148">-Share</span></span>
<span data-ttu-id="cb16d-149">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="cb16d-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="cb16d-150">Questo cmdlet consente di rimuovere il file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="cb16d-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="cb16d-151">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="cb16d-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="cb16d-152">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cb16d-152">This object contains the storage context.</span></span>
<span data-ttu-id="cb16d-153">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="cb16d-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="cb16d-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cb16d-154">-ShareName</span></span>
<span data-ttu-id="cb16d-155">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="cb16d-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="cb16d-156">Questo cmdlet consente di rimuovere il file nel parametro Share this specificato.</span><span class="sxs-lookup"><span data-stu-id="cb16d-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="cb16d-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cb16d-157">-Confirm</span></span>
<span data-ttu-id="cb16d-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb16d-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb16d-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb16d-159">-WhatIf</span></span>
<span data-ttu-id="cb16d-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb16d-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb16d-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb16d-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb16d-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb16d-162">CommonParameters</span></span>
<span data-ttu-id="cb16d-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb16d-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb16d-164">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb16d-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb16d-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb16d-165">INPUTS</span></span>

### <span data-ttu-id="cb16d-166">Microsoft. Azure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="cb16d-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="cb16d-167">Microsoft. Azure. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="cb16d-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="cb16d-168">Microsoft. Azure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="cb16d-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="cb16d-169">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb16d-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cb16d-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb16d-170">OUTPUTS</span></span>

### <span data-ttu-id="cb16d-171">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="cb16d-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="cb16d-172">Note</span><span class="sxs-lookup"><span data-stu-id="cb16d-172">NOTES</span></span>

## <span data-ttu-id="cb16d-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb16d-173">RELATED LINKS</span></span>

[<span data-ttu-id="cb16d-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cb16d-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="cb16d-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="cb16d-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="cb16d-176">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb16d-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)