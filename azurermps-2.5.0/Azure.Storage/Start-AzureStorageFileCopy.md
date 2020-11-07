---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestoragefilecopy
schema: 2.0.0
ms.openlocfilehash: e12240ed399c458c176ab7e9439752ee6551f190
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866925"
---
# <span data-ttu-id="ecfa6-101">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ecfa6-101">Start-AzureStorageFileCopy</span></span>

## <span data-ttu-id="ecfa6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecfa6-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfa6-103">Inizia a copiare un file di origine.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-103">Starts to copy a source file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecfa6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecfa6-104">SYNTAX</span></span>

### <span data-ttu-id="ecfa6-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="ecfa6-105">ContainerName</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecfa6-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ecfa6-106">ContainerInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfa6-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="ecfa6-107">BlobInstanceFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfa6-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="ecfa6-108">BlobInstanceFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecfa6-109">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="ecfa6-109">ShareName</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecfa6-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="ecfa6-110">ShareInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfa6-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="ecfa6-111">FileInstanceToFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfa6-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="ecfa6-112">FileInstanceToFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecfa6-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="ecfa6-113">UriToFilePath</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfa6-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="ecfa6-114">UriToFileInstance</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecfa6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecfa6-115">DESCRIPTION</span></span>
<span data-ttu-id="ecfa6-116">Il cmdlet **Start-AzureStorageFileCopy** avvia la copia di un file di origine in un file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-116">The **Start-AzureStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="ecfa6-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecfa6-117">EXAMPLES</span></span>

### <span data-ttu-id="ecfa6-118">Esempio 1: avviare l'operazione di copia da un file a un file usando il nome della condivisione e il nome file</span><span class="sxs-lookup"><span data-stu-id="ecfa6-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="ecfa6-119">Questo comando avvia un'operazione di copia da file a file.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="ecfa6-120">Il comando specifica il nome della condivisione e il nome del file</span><span class="sxs-lookup"><span data-stu-id="ecfa6-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="ecfa6-121">Esempio 2: avviare l'operazione di copia da BLOB a file usando il nome del contenitore e il nome BLOB</span><span class="sxs-lookup"><span data-stu-id="ecfa6-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="ecfa6-122">Questo comando avvia un'operazione di copia da BLOB a file.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="ecfa6-123">Il comando specifica il nome del contenitore e il nome BLOB</span><span class="sxs-lookup"><span data-stu-id="ecfa6-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="ecfa6-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecfa6-124">PARAMETERS</span></span>

### <span data-ttu-id="ecfa6-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="ecfa6-125">-AbsoluteUri</span></span>
<span data-ttu-id="ecfa6-126">Specifica l'URI del file di origine.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="ecfa6-127">Se la posizione di origine richiede una credenziale, è necessario specificarne una.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: System.String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ecfa6-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ecfa6-129">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ecfa6-130">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ecfa6-131">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ecfa6-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ecfa6-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ecfa6-133">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ecfa6-134">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ecfa6-135">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ecfa6-136">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ecfa6-137">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-137">The default value is 10.</span></span>

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

### <span data-ttu-id="ecfa6-138">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ecfa6-138">-Context</span></span>
<span data-ttu-id="ecfa6-139">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="ecfa6-140">Per ottenere un contesto, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-140">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfa6-141">-DefaultProfile</span></span>
<span data-ttu-id="ecfa6-142">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="ecfa6-143">-DestContext</span></span>
<span data-ttu-id="ecfa6-144">Specifica il contesto di archiviazione di Azure della destinazione.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="ecfa6-145">Per ottenere un contesto, USA **New-AzureStorageContext**.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-145">To obtain a context, use **New-AzureStorageContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="ecfa6-146">-DestFile</span></span>
<span data-ttu-id="ecfa6-147">Specifica un oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="ecfa6-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="ecfa6-148">È possibile creare un file cloud o ottenerne uno usando il cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-148">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="ecfa6-149">-DestFilePath</span></span>
<span data-ttu-id="ecfa6-150">Specifica il percorso del file di destinazione relativo alla condivisione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-150">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="ecfa6-151">-DestShareName</span></span>
<span data-ttu-id="ecfa6-152">Specifica il nome della condivisione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-152">Specifies the name of the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-153">-Force</span><span class="sxs-lookup"><span data-stu-id="ecfa6-153">-Force</span></span>
<span data-ttu-id="ecfa6-154">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ecfa6-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ecfa6-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ecfa6-156">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ecfa6-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="ecfa6-157">-SrcBlob</span></span>
<span data-ttu-id="ecfa6-158">Specifica un oggetto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="ecfa6-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="ecfa6-159">È possibile creare un BLOB cloud o ottenerne uno usando il cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-159">You can create a cloud blob or obtain one by using the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="ecfa6-160">-SrcBlobName</span></span>
<span data-ttu-id="ecfa6-161">Specifica il nome del BLOB di origine.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-161">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="ecfa6-162">-SrcContainer</span></span>
<span data-ttu-id="ecfa6-163">Specifica un oggetto contenitore BLOB cloud.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="ecfa6-164">Puoi creare un oggetto contenitore BLOB di cloud o usare il cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-164">You can create cloud blob container object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="ecfa6-165">-SrcContainerName</span></span>
<span data-ttu-id="ecfa6-166">Specifica il nome del contenitore di origine.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-166">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="ecfa6-167">-SrcFile</span></span>
<span data-ttu-id="ecfa6-168">Specifica un oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="ecfa6-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="ecfa6-169">È possibile creare un file cloud o ottenerne uno utilizzando **Get-AzureStorageFile**.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-169">You can create a cloud file or obtain one by using **Get-AzureStorageFile**.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="ecfa6-170">-SrcFilePath</span></span>
<span data-ttu-id="ecfa6-171">Specifica il percorso del file di origine relativo alla directory di origine o alla condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="ecfa6-172">-SrcShare</span></span>
<span data-ttu-id="ecfa6-173">Specifica un oggetto condivisione file cloud.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="ecfa6-174">È possibile creare una condivisione di file cloud o ottenerne una usando il cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-174">You can create a cloud file share or obtain one by using the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="ecfa6-175">-SrcShareName</span></span>
<span data-ttu-id="ecfa6-176">Specifica il nome della condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-176">Specifies the name of the source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfa6-177">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ecfa6-177">-Confirm</span></span>
<span data-ttu-id="ecfa6-178">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecfa6-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecfa6-179">-WhatIf</span></span>
<span data-ttu-id="ecfa6-180">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecfa6-181">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecfa6-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfa6-182">CommonParameters</span></span>
<span data-ttu-id="ecfa6-183">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfa6-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfa6-184">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecfa6-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfa6-185">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecfa6-185">INPUTS</span></span>

### <span data-ttu-id="ecfa6-186">Microsoft. WindowsAzure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ecfa6-186">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ecfa6-187">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="ecfa6-187">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="ecfa6-188">Parametri: SrcFile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ecfa6-188">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="ecfa6-189">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ecfa6-189">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ecfa6-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecfa6-190">OUTPUTS</span></span>

### <span data-ttu-id="ecfa6-191">System. void</span><span class="sxs-lookup"><span data-stu-id="ecfa6-191">System.Void</span></span>

## <span data-ttu-id="ecfa6-192">Note</span><span class="sxs-lookup"><span data-stu-id="ecfa6-192">NOTES</span></span>

## <span data-ttu-id="ecfa6-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecfa6-193">RELATED LINKS</span></span>

[<span data-ttu-id="ecfa6-194">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ecfa6-194">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="ecfa6-195">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ecfa6-195">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="ecfa6-196">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="ecfa6-196">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="ecfa6-197">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="ecfa6-197">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="ecfa6-198">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="ecfa6-198">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="ecfa6-199">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ecfa6-199">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
