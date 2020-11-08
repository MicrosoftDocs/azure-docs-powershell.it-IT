---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 84f6ae7f80eb7af3c4fccad08b0d9d2a20b0caeb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033633"
---
# <span data-ttu-id="0910f-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0910f-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="0910f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0910f-102">SYNOPSIS</span></span>
<span data-ttu-id="0910f-103">Crea una directory.</span><span class="sxs-lookup"><span data-stu-id="0910f-103">Creates a directory.</span></span>

## <span data-ttu-id="0910f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0910f-104">SYNTAX</span></span>

### <span data-ttu-id="0910f-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0910f-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0910f-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="0910f-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0910f-107">Directory</span><span class="sxs-lookup"><span data-stu-id="0910f-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="0910f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0910f-108">DESCRIPTION</span></span>
<span data-ttu-id="0910f-109">Il cmdlet **New-AzStorageDirectory** crea una directory.</span><span class="sxs-lookup"><span data-stu-id="0910f-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="0910f-110">Questo cmdlet restituisce un oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="0910f-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="0910f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0910f-111">EXAMPLES</span></span>

### <span data-ttu-id="0910f-112">Esempio 1: creare una cartella in una condivisione file</span><span class="sxs-lookup"><span data-stu-id="0910f-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="0910f-113">Questo comando crea una cartella denominata ContosoWorkingFolder nella condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="0910f-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="0910f-114">Esempio 2: creare una cartella in una condivisione file specificata in un oggetto condivisione file</span><span class="sxs-lookup"><span data-stu-id="0910f-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="0910f-115">Questo comando usa il cmdlet **Get-AzStorageShare** per ottenere la condivisione di file denominata ContosoShare06 e quindi la passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="0910f-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0910f-116">Il cmdlet corrente crea la cartella denominata ContosoWorkingFolder in ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="0910f-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="0910f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0910f-117">PARAMETERS</span></span>

### <span data-ttu-id="0910f-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0910f-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0910f-119">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="0910f-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0910f-120">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0910f-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0910f-121">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="0910f-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0910f-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0910f-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0910f-123">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="0910f-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0910f-124">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="0910f-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0910f-125">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="0910f-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0910f-126">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="0910f-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0910f-127">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="0910f-127">The default value is 10.</span></span>

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

### <span data-ttu-id="0910f-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0910f-128">-Context</span></span>
<span data-ttu-id="0910f-129">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0910f-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0910f-130">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="0910f-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="0910f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0910f-131">-DefaultProfile</span></span>
<span data-ttu-id="0910f-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0910f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0910f-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="0910f-133">-Directory</span></span>
<span data-ttu-id="0910f-134">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="0910f-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="0910f-135">Questo cmdlet crea la cartella nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0910f-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="0910f-136">Per ottenere una directory, usare il cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="0910f-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="0910f-137">Puoi anche usare il cmdlet Get-AzStorageFile per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="0910f-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="0910f-138">-Path</span><span class="sxs-lookup"><span data-stu-id="0910f-138">-Path</span></span>
<span data-ttu-id="0910f-139">Specifica il percorso di una cartella.</span><span class="sxs-lookup"><span data-stu-id="0910f-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="0910f-140">Questo cmdlet crea una cartella per il percorso specificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0910f-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0910f-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0910f-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0910f-142">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="0910f-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0910f-143">-Condividi</span><span class="sxs-lookup"><span data-stu-id="0910f-143">-Share</span></span>
<span data-ttu-id="0910f-144">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="0910f-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="0910f-145">Questo cmdlet crea una cartella nella condivisione file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0910f-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="0910f-146">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="0910f-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="0910f-147">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0910f-147">This object contains the storage context.</span></span>
<span data-ttu-id="0910f-148">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="0910f-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="0910f-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="0910f-149">-ShareName</span></span>
<span data-ttu-id="0910f-150">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="0910f-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="0910f-151">Questo cmdlet crea una cartella nella condivisione file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0910f-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="0910f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0910f-152">CommonParameters</span></span>
<span data-ttu-id="0910f-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0910f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0910f-154">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0910f-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0910f-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0910f-155">INPUTS</span></span>

### <span data-ttu-id="0910f-156">Microsoft. Azure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="0910f-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="0910f-157">Microsoft. Azure. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="0910f-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="0910f-158">System. String</span><span class="sxs-lookup"><span data-stu-id="0910f-158">System.String</span></span>

### <span data-ttu-id="0910f-159">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0910f-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0910f-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0910f-160">OUTPUTS</span></span>

### <span data-ttu-id="0910f-161">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="0910f-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="0910f-162">Note</span><span class="sxs-lookup"><span data-stu-id="0910f-162">NOTES</span></span>

## <span data-ttu-id="0910f-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0910f-163">RELATED LINKS</span></span>

[<span data-ttu-id="0910f-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="0910f-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="0910f-165">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="0910f-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="0910f-166">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0910f-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0910f-167">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0910f-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="0910f-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0910f-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
