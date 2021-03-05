---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: c86a2d616334729df6b7fa57a25cc51750bbff1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981501"
---
# <span data-ttu-id="5fbf1-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="5fbf1-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="5fbf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fbf1-102">SYNOPSIS</span></span>
<span data-ttu-id="5fbf1-103">Ottiene lo stato di un'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="5fbf1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fbf1-104">SYNTAX</span></span>

### <span data-ttu-id="5fbf1-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="5fbf1-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5fbf1-106">File</span><span class="sxs-lookup"><span data-stu-id="5fbf1-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fbf1-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5fbf1-107">DESCRIPTION</span></span>
<span data-ttu-id="5fbf1-108">Il cmdlet **Get-AzStorageFileCopyState** ottiene lo stato di un'operazione di copia di file di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="5fbf1-109">Deve essere eseguita nel file di destinazione della copia.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="5fbf1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fbf1-110">EXAMPLES</span></span>

### <span data-ttu-id="5fbf1-111">Esempio 1: Ottenere lo stato di copia in base al nome file</span><span class="sxs-lookup"><span data-stu-id="5fbf1-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="5fbf1-112">Questo comando ottiene lo stato dell'operazione di copia per un file con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="5fbf1-113">Esempio 2: Avviare la copia e la pipeline per ottenere lo stato di copia</span><span class="sxs-lookup"><span data-stu-id="5fbf1-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="5fbf1-114">Il primo comando avvia la copia del file "contosofile" in "contosofile_copy" e restituisce l'output dell'oggetto file di data e ora.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="5fbf1-115">La seconda pipeline di comando l'oggetto file destiantion a Get-AzStorageFileCopyState, per ottenere lo stato di copia del file.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="5fbf1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fbf1-116">PARAMETERS</span></span>

### <span data-ttu-id="5fbf1-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5fbf1-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5fbf1-118">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5fbf1-119">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5fbf1-120">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5fbf1-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5fbf1-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5fbf1-122">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5fbf1-123">È possibile usare questo parametro per limitare la simultaneità per limitare l'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5fbf1-124">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5fbf1-125">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5fbf1-126">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-126">The default value is 10.</span></span>

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

### <span data-ttu-id="5fbf1-127">-Context</span><span class="sxs-lookup"><span data-stu-id="5fbf1-127">-Context</span></span>
<span data-ttu-id="5fbf1-128">Specifica un contesto di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="5fbf1-129">Per ottenere un contesto, usare il cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="5fbf1-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="5fbf1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fbf1-130">-DefaultProfile</span></span>
<span data-ttu-id="5fbf1-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fbf1-132">-File</span><span class="sxs-lookup"><span data-stu-id="5fbf1-132">-File</span></span>
<span data-ttu-id="5fbf1-133">Specifica un **oggetto CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="5fbf1-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="5fbf1-134">È possibile creare un file cloud o ottenerne uno usando il cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="5fbf1-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="5fbf1-135">-FilePath</span></span>
<span data-ttu-id="5fbf1-136">Specifica il percorso del file relativo a una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fbf1-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5fbf1-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5fbf1-138">Specifica la durata del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5fbf1-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="5fbf1-139">-ShareName</span></span>
<span data-ttu-id="5fbf1-140">Specifica il nome di una condivisione.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="5fbf1-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="5fbf1-141">-WaitForComplete</span></span>
<span data-ttu-id="5fbf1-142">Indica che questo cmdlet attende il completamento della copia.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="5fbf1-143">Se non si specifica questo parametro, questo cmdlet restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="5fbf1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fbf1-144">CommonParameters</span></span>
<span data-ttu-id="5fbf1-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fbf1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fbf1-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fbf1-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fbf1-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="5fbf1-147">INPUTS</span></span>

### <span data-ttu-id="5fbf1-148">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="5fbf1-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="5fbf1-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5fbf1-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5fbf1-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fbf1-150">OUTPUTS</span></span>

### <span data-ttu-id="5fbf1-151">Microsoft.Azure.Storage.File.CopyState</span><span class="sxs-lookup"><span data-stu-id="5fbf1-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="5fbf1-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="5fbf1-152">NOTES</span></span>

## <span data-ttu-id="5fbf1-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fbf1-153">RELATED LINKS</span></span>

[<span data-ttu-id="5fbf1-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="5fbf1-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="5fbf1-155">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5fbf1-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="5fbf1-156">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5fbf1-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="5fbf1-157">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5fbf1-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
