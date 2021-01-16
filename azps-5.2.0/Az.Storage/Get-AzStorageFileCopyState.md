---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324979"
---
# <span data-ttu-id="e9d09-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="e9d09-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="e9d09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9d09-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d09-103">Ottiene lo stato di un'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="e9d09-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="e9d09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9d09-104">SYNTAX</span></span>

### <span data-ttu-id="e9d09-105">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="e9d09-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e9d09-106">File</span><span class="sxs-lookup"><span data-stu-id="e9d09-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9d09-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9d09-107">DESCRIPTION</span></span>
<span data-ttu-id="e9d09-108">Il cmdlet **Get-AzStorageFileCopyState** ottiene lo stato di un'operazione di copia di un file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e9d09-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="e9d09-109">Dovrebbe essere eseguito nel file di destinazione della copia.</span><span class="sxs-lookup"><span data-stu-id="e9d09-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="e9d09-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9d09-110">EXAMPLES</span></span>

### <span data-ttu-id="e9d09-111">Esempio 1: ottenere lo stato di copia per nome file</span><span class="sxs-lookup"><span data-stu-id="e9d09-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="e9d09-112">Questo comando ottiene lo stato dell'operazione di copia per un file con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="e9d09-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="e9d09-113">Esempio 2: avviare la copia e la pipeline per ottenere lo stato di copia</span><span class="sxs-lookup"><span data-stu-id="e9d09-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="e9d09-114">Il primo comando avvia la copia del file "contosofile" in "contosofile_copy" e l'output dell'oggetto file destiantion.</span><span class="sxs-lookup"><span data-stu-id="e9d09-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="e9d09-115">Il secondo comando pipeline l'oggetto file destiantion per Get-AzStorageFileCopyState, per ottenere lo stato di copia del file.</span><span class="sxs-lookup"><span data-stu-id="e9d09-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="e9d09-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9d09-116">PARAMETERS</span></span>

### <span data-ttu-id="e9d09-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e9d09-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e9d09-118">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="e9d09-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e9d09-119">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e9d09-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e9d09-120">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e9d09-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e9d09-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e9d09-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e9d09-122">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="e9d09-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e9d09-123">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="e9d09-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e9d09-124">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="e9d09-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e9d09-125">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="e9d09-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e9d09-126">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="e9d09-126">The default value is 10.</span></span>

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

### <span data-ttu-id="e9d09-127">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e9d09-127">-Context</span></span>
<span data-ttu-id="e9d09-128">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e9d09-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e9d09-129">Per ottenere un contesto, usa il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d09-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e9d09-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d09-130">-DefaultProfile</span></span>
<span data-ttu-id="e9d09-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9d09-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9d09-132">-File</span><span class="sxs-lookup"><span data-stu-id="e9d09-132">-File</span></span>
<span data-ttu-id="e9d09-133">Specifica un oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="e9d09-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="e9d09-134">È possibile creare un file cloud o ottenerne uno usando il cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="e9d09-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="e9d09-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e9d09-135">-FilePath</span></span>
<span data-ttu-id="e9d09-136">Specifica il percorso del file relativo a una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e9d09-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="e9d09-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e9d09-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e9d09-138">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="e9d09-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e9d09-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e9d09-139">-ShareName</span></span>
<span data-ttu-id="e9d09-140">Specifica il nome di una condivisione.</span><span class="sxs-lookup"><span data-stu-id="e9d09-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="e9d09-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="e9d09-141">-WaitForComplete</span></span>
<span data-ttu-id="e9d09-142">Indica che questo cmdlet attende che la copia finisca.</span><span class="sxs-lookup"><span data-stu-id="e9d09-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="e9d09-143">Se non specifichi questo parametro, questo cmdlet restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="e9d09-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="e9d09-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d09-144">CommonParameters</span></span>
<span data-ttu-id="e9d09-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9d09-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d09-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9d09-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d09-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9d09-147">INPUTS</span></span>

### <span data-ttu-id="e9d09-148">Microsoft. Azure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="e9d09-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="e9d09-149">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9d09-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e9d09-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9d09-150">OUTPUTS</span></span>

### <span data-ttu-id="e9d09-151">Microsoft. Azure. storage. file. CopyState</span><span class="sxs-lookup"><span data-stu-id="e9d09-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="e9d09-152">Note</span><span class="sxs-lookup"><span data-stu-id="e9d09-152">NOTES</span></span>

## <span data-ttu-id="e9d09-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9d09-153">RELATED LINKS</span></span>

[<span data-ttu-id="e9d09-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="e9d09-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="e9d09-155">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9d09-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="e9d09-156">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e9d09-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="e9d09-157">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e9d09-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
