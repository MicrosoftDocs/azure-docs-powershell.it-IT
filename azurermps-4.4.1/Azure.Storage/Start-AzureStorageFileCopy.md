---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: a92c1aa0520fdec3f74a49f79ca1c5de8072be37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518459"
---
# <span data-ttu-id="af81a-101">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="af81a-101">Start-AzureStorageFileCopy</span></span>

## <span data-ttu-id="af81a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af81a-102">SYNOPSIS</span></span>
<span data-ttu-id="af81a-103">Inizia a copiare un file di origine.</span><span class="sxs-lookup"><span data-stu-id="af81a-103">Starts to copy a source file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af81a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af81a-104">SYNTAX</span></span>

### <span data-ttu-id="af81a-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="af81a-105">ContainerName</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af81a-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="af81a-106">ContainerInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af81a-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="af81a-107">BlobInstanceFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af81a-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="af81a-108">BlobInstanceFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af81a-109">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="af81a-109">ShareName</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af81a-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="af81a-110">ShareInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af81a-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="af81a-111">FileInstanceToFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af81a-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="af81a-112">FileInstanceToFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af81a-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="af81a-113">UriToFilePath</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af81a-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="af81a-114">UriToFileInstance</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af81a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af81a-115">DESCRIPTION</span></span>
<span data-ttu-id="af81a-116">Il cmdlet **Start-AzureStorageFileCopy** avvia la copia di un file di origine in un file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af81a-116">The **Start-AzureStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="af81a-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af81a-117">EXAMPLES</span></span>

### <span data-ttu-id="af81a-118">Esempio 1: avviare l'operazione di copia da un file a un file usando il nome della condivisione e il nome file</span><span class="sxs-lookup"><span data-stu-id="af81a-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="af81a-119">Questo comando avvia un'operazione di copia da file a file.</span><span class="sxs-lookup"><span data-stu-id="af81a-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="af81a-120">Il comando specifica il nome della condivisione e il nome del file</span><span class="sxs-lookup"><span data-stu-id="af81a-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="af81a-121">Esempio 2: avviare l'operazione di copia da BLOB a file usando il nome del contenitore e il nome BLOB</span><span class="sxs-lookup"><span data-stu-id="af81a-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="af81a-122">Questo comando avvia un'operazione di copia da BLOB a file.</span><span class="sxs-lookup"><span data-stu-id="af81a-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="af81a-123">Il comando specifica il nome del contenitore e il nome BLOB</span><span class="sxs-lookup"><span data-stu-id="af81a-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="af81a-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af81a-124">PARAMETERS</span></span>

### <span data-ttu-id="af81a-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="af81a-125">-AbsoluteUri</span></span>
<span data-ttu-id="af81a-126">Specifica l'URI del file di origine.</span><span class="sxs-lookup"><span data-stu-id="af81a-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="af81a-127">Se la posizione di origine richiede una credenziale, è necessario specificarne una.</span><span class="sxs-lookup"><span data-stu-id="af81a-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="af81a-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="af81a-129">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="af81a-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="af81a-130">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="af81a-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="af81a-131">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="af81a-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="af81a-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="af81a-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="af81a-133">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="af81a-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="af81a-134">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="af81a-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="af81a-135">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="af81a-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="af81a-136">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="af81a-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="af81a-137">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="af81a-137">The default value is 10.</span></span>

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

### <span data-ttu-id="af81a-138">-Contesto</span><span class="sxs-lookup"><span data-stu-id="af81a-138">-Context</span></span>
<span data-ttu-id="af81a-139">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="af81a-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="af81a-140">Per ottenere un contesto, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="af81a-140">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-141">-DestContext</span><span class="sxs-lookup"><span data-stu-id="af81a-141">-DestContext</span></span>
<span data-ttu-id="af81a-142">Specifica il contesto di archiviazione di Azure della destinazione.</span><span class="sxs-lookup"><span data-stu-id="af81a-142">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="af81a-143">Per ottenere un contesto, USA **New-AzureStorageContext**.</span><span class="sxs-lookup"><span data-stu-id="af81a-143">To obtain a context, use **New-AzureStorageContext**.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-144">-DestFile</span><span class="sxs-lookup"><span data-stu-id="af81a-144">-DestFile</span></span>
<span data-ttu-id="af81a-145">Specifica un oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="af81a-145">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="af81a-146">È possibile creare un file cloud o ottenerne uno usando il cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="af81a-146">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-147">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="af81a-147">-DestFilePath</span></span>
<span data-ttu-id="af81a-148">Specifica il percorso del file di destinazione relativo alla condivisione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af81a-148">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-149">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="af81a-149">-DestShareName</span></span>
<span data-ttu-id="af81a-150">Specifica il nome della condivisione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af81a-150">Specifies the name of the destination share.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-151">-Force</span><span class="sxs-lookup"><span data-stu-id="af81a-151">-Force</span></span>
<span data-ttu-id="af81a-152">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="af81a-152">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af81a-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="af81a-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="af81a-154">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="af81a-154">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="af81a-155">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="af81a-155">-SrcBlob</span></span>
<span data-ttu-id="af81a-156">Specifica un oggetto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="af81a-156">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="af81a-157">È possibile creare un BLOB cloud o ottenerne uno usando il cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="af81a-157">You can create a cloud blob or obtain one by using the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-158">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="af81a-158">-SrcBlobName</span></span>
<span data-ttu-id="af81a-159">Specifica il nome del BLOB di origine.</span><span class="sxs-lookup"><span data-stu-id="af81a-159">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-160">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="af81a-160">-SrcContainer</span></span>
<span data-ttu-id="af81a-161">Specifica un oggetto contenitore BLOB cloud.</span><span class="sxs-lookup"><span data-stu-id="af81a-161">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="af81a-162">Puoi creare un oggetto contenitore BLOB di cloud o usare il cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="af81a-162">You can create cloud blob container object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-163">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="af81a-163">-SrcContainerName</span></span>
<span data-ttu-id="af81a-164">Specifica il nome del contenitore di origine.</span><span class="sxs-lookup"><span data-stu-id="af81a-164">Specifies the name of the source container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-165">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="af81a-165">-SrcFile</span></span>
<span data-ttu-id="af81a-166">Specifica un oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="af81a-166">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="af81a-167">È possibile creare un file cloud o ottenerne uno utilizzando **Get-AzureStorageFile**.</span><span class="sxs-lookup"><span data-stu-id="af81a-167">You can create a cloud file or obtain one by using **Get-AzureStorageFile**.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-168">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="af81a-168">-SrcFilePath</span></span>
<span data-ttu-id="af81a-169">Specifica il percorso del file di origine relativo alla directory di origine o alla condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="af81a-169">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-170">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="af81a-170">-SrcShare</span></span>
<span data-ttu-id="af81a-171">Specifica un oggetto condivisione file cloud.</span><span class="sxs-lookup"><span data-stu-id="af81a-171">Specifies a cloud file share object.</span></span>
<span data-ttu-id="af81a-172">È possibile creare una condivisione di file cloud o ottenerne una usando il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="af81a-172">You can create a cloud file share or obtain one by using the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-173">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="af81a-173">-SrcShareName</span></span>
<span data-ttu-id="af81a-174">Specifica il nome della condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="af81a-174">Specifies the name of the source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-175">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af81a-175">-Confirm</span></span>
<span data-ttu-id="af81a-176">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af81a-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af81a-177">-WhatIf</span></span>
<span data-ttu-id="af81a-178">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af81a-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af81a-179">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af81a-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af81a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af81a-180">CommonParameters</span></span>
<span data-ttu-id="af81a-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af81a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af81a-182">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af81a-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af81a-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af81a-183">INPUTS</span></span>

### <span data-ttu-id="af81a-184">CloudBlob</span><span class="sxs-lookup"><span data-stu-id="af81a-184">CloudBlob</span></span>

<span data-ttu-id="af81a-185">Il parametro ' SrcBlob ' accetta il valore di tipo ' CloudBlob ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="af81a-185">Parameter 'SrcBlob' accepts value of type 'CloudBlob' from the pipeline</span></span>

### <span data-ttu-id="af81a-186">CloudFile</span><span class="sxs-lookup"><span data-stu-id="af81a-186">CloudFile</span></span>

<span data-ttu-id="af81a-187">Il parametro ' SrcFile ' accetta il valore di tipo ' CloudFile ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="af81a-187">Parameter 'SrcFile' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="af81a-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af81a-188">OUTPUTS</span></span>

## <span data-ttu-id="af81a-189">Note</span><span class="sxs-lookup"><span data-stu-id="af81a-189">NOTES</span></span>

## <span data-ttu-id="af81a-190">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af81a-190">RELATED LINKS</span></span>

[<span data-ttu-id="af81a-191">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="af81a-191">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="af81a-192">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="af81a-192">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="af81a-193">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="af81a-193">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="af81a-194">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="af81a-194">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="af81a-195">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="af81a-195">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="af81a-196">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="af81a-196">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
