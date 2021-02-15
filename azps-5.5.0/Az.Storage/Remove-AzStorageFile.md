---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 99809e5115cb256b8e546334efce0e6e399be04f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195702"
---
# <span data-ttu-id="88e66-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="88e66-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="88e66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88e66-102">SYNOPSIS</span></span>
<span data-ttu-id="88e66-103">Elimina un file.</span><span class="sxs-lookup"><span data-stu-id="88e66-103">Deletes a file.</span></span>

## <span data-ttu-id="88e66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88e66-104">SYNTAX</span></span>

### <span data-ttu-id="88e66-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88e66-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88e66-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="88e66-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88e66-107">Directory</span><span class="sxs-lookup"><span data-stu-id="88e66-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88e66-108">File</span><span class="sxs-lookup"><span data-stu-id="88e66-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88e66-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="88e66-109">DESCRIPTION</span></span>
<span data-ttu-id="88e66-110">Il cmdlet **Remove-AzStorageFile** elimina un file.</span><span class="sxs-lookup"><span data-stu-id="88e66-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="88e66-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88e66-111">EXAMPLES</span></span>

### <span data-ttu-id="88e66-112">Esempio 1: Eliminare un file da una condivisione file</span><span class="sxs-lookup"><span data-stu-id="88e66-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="88e66-113">Questo comando elimina il file denominato ContosoFile22 dalla condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="88e66-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="88e66-114">Esempio 2: Ottenere un file da una condivisione file usando un oggetto condivisione file</span><span class="sxs-lookup"><span data-stu-id="88e66-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="88e66-115">Questo comando usa il cmdlet **Get-AzStorageShare** per ottenere la condivisione file denominata ContosoShare06, quindi passa l'oggetto al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="88e66-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="88e66-116">Il comando corrente elimina il file denominato ContosoFile22 da ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="88e66-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="88e66-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88e66-117">PARAMETERS</span></span>

### <span data-ttu-id="88e66-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="88e66-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="88e66-119">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="88e66-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="88e66-120">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="88e66-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="88e66-121">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="88e66-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="88e66-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="88e66-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="88e66-123">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="88e66-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="88e66-124">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="88e66-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="88e66-125">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="88e66-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="88e66-126">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="88e66-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="88e66-127">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="88e66-127">The default value is 10.</span></span>

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

### <span data-ttu-id="88e66-128">-Context</span><span class="sxs-lookup"><span data-stu-id="88e66-128">-Context</span></span>
<span data-ttu-id="88e66-129">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="88e66-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="88e66-130">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="88e66-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="88e66-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e66-131">-DefaultProfile</span></span>
<span data-ttu-id="88e66-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88e66-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e66-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="88e66-133">-Directory</span></span>
<span data-ttu-id="88e66-134">Specifica una cartella come oggetto **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="88e66-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="88e66-135">Questo cmdlet rimuove un file dalla cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="88e66-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="88e66-136">-File</span><span class="sxs-lookup"><span data-stu-id="88e66-136">-File</span></span>
<span data-ttu-id="88e66-137">Specifica un file come oggetto **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="88e66-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="88e66-138">Questo cmdlet rimuove il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="88e66-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="88e66-139">Per ottenere un **oggetto CloudFile,** usare il cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="88e66-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="88e66-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88e66-140">-PassThru</span></span>
<span data-ttu-id="88e66-141">Indica che questo cmdlet restituisce un valore **booleano** che riflette l'esito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="88e66-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="88e66-142">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="88e66-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="88e66-143">-Path</span><span class="sxs-lookup"><span data-stu-id="88e66-143">-Path</span></span>
<span data-ttu-id="88e66-144">Specifica il percorso di un file.</span><span class="sxs-lookup"><span data-stu-id="88e66-144">Specifies the path of a file.</span></span>
<span data-ttu-id="88e66-145">Questo cmdlet elimina il file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="88e66-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="88e66-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="88e66-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="88e66-147">Specifica la durata del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="88e66-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="88e66-148">-Condividi</span><span class="sxs-lookup"><span data-stu-id="88e66-148">-Share</span></span>
<span data-ttu-id="88e66-149">Specifica un **oggetto CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="88e66-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="88e66-150">Questo cmdlet rimuove il file nella condivisione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="88e66-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="88e66-151">Per ottenere un **oggetto CloudFileShare,** usare il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="88e66-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="88e66-152">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="88e66-152">This object contains the storage context.</span></span>
<span data-ttu-id="88e66-153">Se si specifica questo parametro, non specificare il *parametro Context.*</span><span class="sxs-lookup"><span data-stu-id="88e66-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="88e66-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="88e66-154">-ShareName</span></span>
<span data-ttu-id="88e66-155">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="88e66-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="88e66-156">Questo cmdlet rimuove il file nella condivisione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="88e66-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="88e66-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88e66-157">-Confirm</span></span>
<span data-ttu-id="88e66-158">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e66-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88e66-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88e66-159">-WhatIf</span></span>
<span data-ttu-id="88e66-160">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88e66-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88e66-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88e66-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88e66-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e66-162">CommonParameters</span></span>
<span data-ttu-id="88e66-163">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e66-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e66-164">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e66-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e66-165">INPUT</span><span class="sxs-lookup"><span data-stu-id="88e66-165">INPUTS</span></span>

### <span data-ttu-id="88e66-166">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="88e66-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="88e66-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="88e66-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="88e66-168">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="88e66-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="88e66-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="88e66-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="88e66-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88e66-170">OUTPUTS</span></span>

### <span data-ttu-id="88e66-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="88e66-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="88e66-172">NOTE</span><span class="sxs-lookup"><span data-stu-id="88e66-172">NOTES</span></span>

## <span data-ttu-id="88e66-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88e66-173">RELATED LINKS</span></span>

[<span data-ttu-id="88e66-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="88e66-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="88e66-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="88e66-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="88e66-176">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="88e66-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
