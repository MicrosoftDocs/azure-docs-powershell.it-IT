---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 3ac8cb302c65fd42fdd699588b71bc1b081cc9d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195711"
---
# <span data-ttu-id="d72fc-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="d72fc-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="d72fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d72fc-102">SYNOPSIS</span></span>
<span data-ttu-id="d72fc-103">Elimina una directory.</span><span class="sxs-lookup"><span data-stu-id="d72fc-103">Deletes a directory.</span></span>

## <span data-ttu-id="d72fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d72fc-104">SYNTAX</span></span>

### <span data-ttu-id="d72fc-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d72fc-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d72fc-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="d72fc-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d72fc-107">Directory</span><span class="sxs-lookup"><span data-stu-id="d72fc-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d72fc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d72fc-108">DESCRIPTION</span></span>
<span data-ttu-id="d72fc-109">Il cmdlet **Remove-AzStorageDirectory** elimina una directory.</span><span class="sxs-lookup"><span data-stu-id="d72fc-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="d72fc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d72fc-110">EXAMPLES</span></span>

### <span data-ttu-id="d72fc-111">Esempio 1: Eliminare una cartella</span><span class="sxs-lookup"><span data-stu-id="d72fc-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="d72fc-112">Questo comando elimina la cartella contosoWorkingFolder dalla condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="d72fc-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="d72fc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d72fc-113">PARAMETERS</span></span>

### <span data-ttu-id="d72fc-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d72fc-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d72fc-115">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="d72fc-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d72fc-116">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d72fc-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d72fc-117">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="d72fc-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d72fc-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d72fc-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d72fc-119">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="d72fc-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d72fc-120">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="d72fc-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d72fc-121">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="d72fc-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d72fc-122">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="d72fc-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d72fc-123">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="d72fc-123">The default value is 10.</span></span>

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

### <span data-ttu-id="d72fc-124">-Context</span><span class="sxs-lookup"><span data-stu-id="d72fc-124">-Context</span></span>
<span data-ttu-id="d72fc-125">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d72fc-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d72fc-126">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="d72fc-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d72fc-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72fc-127">-DefaultProfile</span></span>
<span data-ttu-id="d72fc-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d72fc-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d72fc-129">-Directory</span><span class="sxs-lookup"><span data-stu-id="d72fc-129">-Directory</span></span>
<span data-ttu-id="d72fc-130">Specifica una cartella come oggetto **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="d72fc-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="d72fc-131">Questo cmdlet rimuove la cartella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d72fc-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="d72fc-132">Per ottenere una directory, usare il cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="d72fc-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="d72fc-133">È anche possibile usare il cmdlet **Get-AzStorageFile** per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="d72fc-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="d72fc-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d72fc-134">-PassThru</span></span>
<span data-ttu-id="d72fc-135">Indica che, se il cmdlet ha esito positivo, restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="d72fc-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="d72fc-136">Se si specifica questo parametro e il cmdlet non riesce a causa di un valore inappropriato per il parametro _Path,_ il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="d72fc-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="d72fc-137">Se non si specifica questo parametro, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d72fc-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d72fc-138">-Path</span><span class="sxs-lookup"><span data-stu-id="d72fc-138">-Path</span></span>
<span data-ttu-id="d72fc-139">Specifica il percorso di una cartella.</span><span class="sxs-lookup"><span data-stu-id="d72fc-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="d72fc-140">Se la cartella specificata da questo parametro è vuota, questo cmdlet elimina la cartella.</span><span class="sxs-lookup"><span data-stu-id="d72fc-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="d72fc-141">Se la cartella non è vuota, questo cmdlet non apporta alcuna modifica e restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="d72fc-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72fc-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d72fc-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d72fc-143">Specifica la durata del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="d72fc-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d72fc-144">-Condividi</span><span class="sxs-lookup"><span data-stu-id="d72fc-144">-Share</span></span>
<span data-ttu-id="d72fc-145">Specifica un **oggetto CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="d72fc-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="d72fc-146">Questo cmdlet rimuove una cartella nella condivisione file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d72fc-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="d72fc-147">Per ottenere un **oggetto CloudFileShare,** usare il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="d72fc-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="d72fc-148">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d72fc-148">This object contains the storage context.</span></span>
<span data-ttu-id="d72fc-149">Se si specifica questo parametro, non specificare il *parametro Context.*</span><span class="sxs-lookup"><span data-stu-id="d72fc-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="d72fc-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d72fc-150">-ShareName</span></span>
<span data-ttu-id="d72fc-151">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="d72fc-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="d72fc-152">Questo cmdlet rimuove una cartella nella condivisione file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d72fc-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="d72fc-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d72fc-153">-Confirm</span></span>
<span data-ttu-id="d72fc-154">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d72fc-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d72fc-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72fc-155">-WhatIf</span></span>
<span data-ttu-id="d72fc-156">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d72fc-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d72fc-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d72fc-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d72fc-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72fc-158">CommonParameters</span></span>
<span data-ttu-id="d72fc-159">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d72fc-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72fc-160">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d72fc-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72fc-161">INPUT</span><span class="sxs-lookup"><span data-stu-id="d72fc-161">INPUTS</span></span>

### <span data-ttu-id="d72fc-162">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="d72fc-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="d72fc-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="d72fc-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="d72fc-164">System.String</span><span class="sxs-lookup"><span data-stu-id="d72fc-164">System.String</span></span>

### <span data-ttu-id="d72fc-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d72fc-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d72fc-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d72fc-166">OUTPUTS</span></span>

### <span data-ttu-id="d72fc-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="d72fc-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="d72fc-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="d72fc-168">NOTES</span></span>

## <span data-ttu-id="d72fc-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d72fc-169">RELATED LINKS</span></span>

[<span data-ttu-id="d72fc-170">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="d72fc-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="d72fc-171">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d72fc-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d72fc-172">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="d72fc-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
