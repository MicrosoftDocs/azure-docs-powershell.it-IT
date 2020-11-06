---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileCopyState.md
ms.openlocfilehash: bd88b82a358e10de8a738382e29bdb785f89c1e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515928"
---
# <span data-ttu-id="d30c7-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="d30c7-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="d30c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d30c7-102">SYNOPSIS</span></span>
<span data-ttu-id="d30c7-103">Ottiene lo stato di un'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="d30c7-103">Gets the state of a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d30c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d30c7-104">SYNTAX</span></span>

### <span data-ttu-id="d30c7-105">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="d30c7-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d30c7-106">File</span><span class="sxs-lookup"><span data-stu-id="d30c7-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d30c7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d30c7-107">DESCRIPTION</span></span>
<span data-ttu-id="d30c7-108">Il cmdlet **Get-AzureStorageFileCopyState** ottiene lo stato di un'operazione di copia di un file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d30c7-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="d30c7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d30c7-109">EXAMPLES</span></span>

### <span data-ttu-id="d30c7-110">Esempio 1: ottenere lo stato di copia per nome file</span><span class="sxs-lookup"><span data-stu-id="d30c7-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="d30c7-111">Questo comando ottiene lo stato dell'operazione di copia per un file con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="d30c7-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="d30c7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d30c7-112">PARAMETERS</span></span>

### <span data-ttu-id="d30c7-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d30c7-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d30c7-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="d30c7-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d30c7-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d30c7-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d30c7-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="d30c7-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d30c7-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d30c7-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d30c7-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="d30c7-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d30c7-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="d30c7-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d30c7-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="d30c7-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d30c7-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="d30c7-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d30c7-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="d30c7-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d30c7-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d30c7-123">-Context</span></span>
<span data-ttu-id="d30c7-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d30c7-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="d30c7-125">Per ottenere un contesto, usa il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="d30c7-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d30c7-126">-File</span><span class="sxs-lookup"><span data-stu-id="d30c7-126">-File</span></span>
<span data-ttu-id="d30c7-127">Specifica un oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="d30c7-127">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="d30c7-128">È possibile creare un file cloud o ottenerne uno usando il cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="d30c7-128">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="d30c7-129">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d30c7-129">-FilePath</span></span>
<span data-ttu-id="d30c7-130">Specifica il percorso del file relativo a una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d30c7-130">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30c7-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d30c7-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d30c7-132">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="d30c7-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d30c7-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d30c7-133">-ShareName</span></span>
<span data-ttu-id="d30c7-134">Specifica il nome di una condivisione.</span><span class="sxs-lookup"><span data-stu-id="d30c7-134">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="d30c7-135">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="d30c7-135">-WaitForComplete</span></span>
<span data-ttu-id="d30c7-136">Indica che questo cmdlet attende che la copia finisca.</span><span class="sxs-lookup"><span data-stu-id="d30c7-136">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="d30c7-137">Se non specifichi questo parametro, questo cmdlet restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="d30c7-137">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="d30c7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d30c7-138">CommonParameters</span></span>
<span data-ttu-id="d30c7-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d30c7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d30c7-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d30c7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d30c7-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d30c7-141">INPUTS</span></span>

### <span data-ttu-id="d30c7-142">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d30c7-142">IStorageContext</span></span>

<span data-ttu-id="d30c7-143">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d30c7-143">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="d30c7-144">CloudFile</span><span class="sxs-lookup"><span data-stu-id="d30c7-144">CloudFile</span></span>

<span data-ttu-id="d30c7-145">Il parametro "file" accetta il valore di tipo "CloudFile" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d30c7-145">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="d30c7-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d30c7-146">OUTPUTS</span></span>

## <span data-ttu-id="d30c7-147">Note</span><span class="sxs-lookup"><span data-stu-id="d30c7-147">NOTES</span></span>

## <span data-ttu-id="d30c7-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d30c7-148">RELATED LINKS</span></span>

[<span data-ttu-id="d30c7-149">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="d30c7-149">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="d30c7-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d30c7-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d30c7-151">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d30c7-151">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="d30c7-152">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d30c7-152">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
