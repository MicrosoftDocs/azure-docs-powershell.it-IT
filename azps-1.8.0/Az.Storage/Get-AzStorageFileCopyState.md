---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: 8620045690b69d0e9829e240e99766c73ed43b6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676618"
---
# <span data-ttu-id="29d49-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="29d49-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="29d49-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29d49-102">SYNOPSIS</span></span>
<span data-ttu-id="29d49-103">Ottiene lo stato di un'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="29d49-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="29d49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29d49-104">SYNTAX</span></span>

### <span data-ttu-id="29d49-105">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="29d49-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="29d49-106">File</span><span class="sxs-lookup"><span data-stu-id="29d49-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="29d49-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29d49-107">DESCRIPTION</span></span>
<span data-ttu-id="29d49-108">Il cmdlet **Get-AzStorageFileCopyState** ottiene lo stato di un'operazione di copia di un file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="29d49-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="29d49-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29d49-109">EXAMPLES</span></span>

### <span data-ttu-id="29d49-110">Esempio 1: ottenere lo stato di copia per nome file</span><span class="sxs-lookup"><span data-stu-id="29d49-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="29d49-111">Questo comando ottiene lo stato dell'operazione di copia per un file con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="29d49-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="29d49-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29d49-112">PARAMETERS</span></span>

### <span data-ttu-id="29d49-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="29d49-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="29d49-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="29d49-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="29d49-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="29d49-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="29d49-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="29d49-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="29d49-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="29d49-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="29d49-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="29d49-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="29d49-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="29d49-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="29d49-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="29d49-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="29d49-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="29d49-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="29d49-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="29d49-122">The default value is 10.</span></span>

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

### <span data-ttu-id="29d49-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="29d49-123">-Context</span></span>
<span data-ttu-id="29d49-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="29d49-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="29d49-125">Per ottenere un contesto, usa il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="29d49-125">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="29d49-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d49-126">-DefaultProfile</span></span>
<span data-ttu-id="29d49-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29d49-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29d49-128">-File</span><span class="sxs-lookup"><span data-stu-id="29d49-128">-File</span></span>
<span data-ttu-id="29d49-129">Specifica un oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="29d49-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="29d49-130">È possibile creare un file cloud o ottenerne uno usando il cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="29d49-130">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="29d49-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="29d49-131">-FilePath</span></span>
<span data-ttu-id="29d49-132">Specifica il percorso del file relativo a una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="29d49-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="29d49-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="29d49-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="29d49-134">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="29d49-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="29d49-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="29d49-135">-ShareName</span></span>
<span data-ttu-id="29d49-136">Specifica il nome di una condivisione.</span><span class="sxs-lookup"><span data-stu-id="29d49-136">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="29d49-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="29d49-137">-WaitForComplete</span></span>
<span data-ttu-id="29d49-138">Indica che questo cmdlet attende che la copia finisca.</span><span class="sxs-lookup"><span data-stu-id="29d49-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="29d49-139">Se non specifichi questo parametro, questo cmdlet restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="29d49-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="29d49-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d49-140">CommonParameters</span></span>
<span data-ttu-id="29d49-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d49-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d49-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29d49-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d49-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29d49-143">INPUTS</span></span>

### <span data-ttu-id="29d49-144">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="29d49-144">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="29d49-145">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="29d49-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="29d49-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29d49-146">OUTPUTS</span></span>

### <span data-ttu-id="29d49-147">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="29d49-147">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="29d49-148">Note</span><span class="sxs-lookup"><span data-stu-id="29d49-148">NOTES</span></span>

## <span data-ttu-id="29d49-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29d49-149">RELATED LINKS</span></span>

[<span data-ttu-id="29d49-150">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="29d49-150">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="29d49-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="29d49-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="29d49-152">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="29d49-152">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="29d49-153">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="29d49-153">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)