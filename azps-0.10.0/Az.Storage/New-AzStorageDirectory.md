---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 5582c6459d33096f0427c2b7f6ee237f3c258428
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862150"
---
# <span data-ttu-id="cd1aa-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="cd1aa-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="cd1aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="cd1aa-103">Crea una directory.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-103">Creates a directory.</span></span>

## <span data-ttu-id="cd1aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd1aa-104">SYNTAX</span></span>

### <span data-ttu-id="cd1aa-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd1aa-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="cd1aa-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="cd1aa-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd1aa-107">Directory</span><span class="sxs-lookup"><span data-stu-id="cd1aa-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd1aa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd1aa-108">DESCRIPTION</span></span>
<span data-ttu-id="cd1aa-109">Il cmdlet **New-AzStorageDirectory** crea una directory.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="cd1aa-110">Questo cmdlet restituisce un oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="cd1aa-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="cd1aa-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd1aa-111">EXAMPLES</span></span>

### <span data-ttu-id="cd1aa-112">Esempio 1: creare una cartella in una condivisione file</span><span class="sxs-lookup"><span data-stu-id="cd1aa-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="cd1aa-113">Questo comando crea una cartella denominata ContosoWorkingFolder nella condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="cd1aa-114">Esempio 2: creare una cartella in una condivisione file specificata in un oggetto condivisione file</span><span class="sxs-lookup"><span data-stu-id="cd1aa-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="cd1aa-115">Questo comando usa il cmdlet **Get-AzStorageShare** per ottenere la condivisione di file denominata ContosoShare06 e quindi la passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cd1aa-116">Il cmdlet corrente crea la cartella denominata ContosoWorkingFolder in ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="cd1aa-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd1aa-117">PARAMETERS</span></span>

### <span data-ttu-id="cd1aa-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cd1aa-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cd1aa-119">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cd1aa-120">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cd1aa-121">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cd1aa-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cd1aa-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cd1aa-123">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cd1aa-124">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cd1aa-125">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cd1aa-126">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cd1aa-127">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-127">The default value is 10.</span></span>

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

### <span data-ttu-id="cd1aa-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="cd1aa-128">-Context</span></span>
<span data-ttu-id="cd1aa-129">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cd1aa-130">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="cd1aa-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="cd1aa-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd1aa-131">-DefaultProfile</span></span>
<span data-ttu-id="cd1aa-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd1aa-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="cd1aa-133">-Directory</span></span>
<span data-ttu-id="cd1aa-134">Specifica una cartella come oggetto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="cd1aa-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="cd1aa-135">Questo cmdlet crea la cartella nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="cd1aa-136">Per ottenere una directory, usare il cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="cd1aa-137">Puoi anche usare il cmdlet Get-AzStorageFile per ottenere una directory.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="cd1aa-138">-Path</span><span class="sxs-lookup"><span data-stu-id="cd1aa-138">-Path</span></span>
<span data-ttu-id="cd1aa-139">Specifica il percorso di una cartella.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="cd1aa-140">Questo cmdlet crea una cartella per il percorso specificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="cd1aa-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cd1aa-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cd1aa-142">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="cd1aa-143">-Condividi</span><span class="sxs-lookup"><span data-stu-id="cd1aa-143">-Share</span></span>
<span data-ttu-id="cd1aa-144">Specifica un oggetto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="cd1aa-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="cd1aa-145">Questo cmdlet crea una cartella nella condivisione file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="cd1aa-146">Per ottenere un oggetto **CloudFileShare** , usa il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="cd1aa-147">Questo oggetto contiene il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-147">This object contains the storage context.</span></span>
<span data-ttu-id="cd1aa-148">Se specifichi questo parametro, non specificare il parametro *context* .</span><span class="sxs-lookup"><span data-stu-id="cd1aa-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="cd1aa-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cd1aa-149">-ShareName</span></span>
<span data-ttu-id="cd1aa-150">Specifica il nome della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="cd1aa-151">Questo cmdlet crea una cartella nella condivisione file specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="cd1aa-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd1aa-152">CommonParameters</span></span>
<span data-ttu-id="cd1aa-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd1aa-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd1aa-154">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd1aa-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd1aa-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd1aa-155">INPUTS</span></span>

### <span data-ttu-id="cd1aa-156">Microsoft. WindowsAz. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="cd1aa-156">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="cd1aa-157">Parametri: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd1aa-157">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="cd1aa-158">Microsoft. WindowsAz. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="cd1aa-158">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="cd1aa-159">Parameters: directory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd1aa-159">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="cd1aa-160">System. String</span><span class="sxs-lookup"><span data-stu-id="cd1aa-160">System.String</span></span>

### <span data-ttu-id="cd1aa-161">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd1aa-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cd1aa-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd1aa-162">OUTPUTS</span></span>

### <span data-ttu-id="cd1aa-163">Microsoft. WindowsAz. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="cd1aa-163">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="cd1aa-164">Note</span><span class="sxs-lookup"><span data-stu-id="cd1aa-164">NOTES</span></span>

## <span data-ttu-id="cd1aa-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd1aa-165">RELATED LINKS</span></span>

[<span data-ttu-id="cd1aa-166">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cd1aa-166">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="cd1aa-167">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd1aa-167">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="cd1aa-168">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd1aa-168">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="cd1aa-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="cd1aa-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="cd1aa-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="cd1aa-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
