---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 578c32a27f53f586ec8a8013533e42928df48d30
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332011"
---
# <span data-ttu-id="0462d-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0462d-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="0462d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0462d-102">SYNOPSIS</span></span>
<span data-ttu-id="0462d-103">Inizia a copiare un file di origine.</span><span class="sxs-lookup"><span data-stu-id="0462d-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="0462d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0462d-104">SYNTAX</span></span>

### <span data-ttu-id="0462d-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="0462d-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0462d-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0462d-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0462d-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="0462d-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0462d-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="0462d-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0462d-109">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="0462d-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0462d-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="0462d-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0462d-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="0462d-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0462d-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="0462d-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0462d-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="0462d-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0462d-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="0462d-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0462d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0462d-115">DESCRIPTION</span></span>
<span data-ttu-id="0462d-116">Il cmdlet **Start-AzStorageFileCopy** avvia la copia di un file di origine in un file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0462d-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="0462d-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0462d-117">EXAMPLES</span></span>

### <span data-ttu-id="0462d-118">Esempio 1: avviare l'operazione di copia da un file a un file usando il nome della condivisione e il nome file</span><span class="sxs-lookup"><span data-stu-id="0462d-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="0462d-119">Questo comando avvia un'operazione di copia da file a file.</span><span class="sxs-lookup"><span data-stu-id="0462d-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="0462d-120">Il comando specifica il nome della condivisione e il nome del file</span><span class="sxs-lookup"><span data-stu-id="0462d-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="0462d-121">Esempio 2: avviare l'operazione di copia da BLOB a file usando il nome del contenitore e il nome BLOB</span><span class="sxs-lookup"><span data-stu-id="0462d-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="0462d-122">Questo comando avvia un'operazione di copia da BLOB a file.</span><span class="sxs-lookup"><span data-stu-id="0462d-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="0462d-123">Il comando specifica il nome del contenitore e il nome BLOB</span><span class="sxs-lookup"><span data-stu-id="0462d-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="0462d-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0462d-124">PARAMETERS</span></span>

### <span data-ttu-id="0462d-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="0462d-125">-AbsoluteUri</span></span>
<span data-ttu-id="0462d-126">Specifica l'URI del file di origine.</span><span class="sxs-lookup"><span data-stu-id="0462d-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="0462d-127">Se la posizione di origine richiede una credenziale, è necessario specificarne una.</span><span class="sxs-lookup"><span data-stu-id="0462d-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="0462d-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0462d-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0462d-129">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="0462d-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0462d-130">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0462d-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0462d-131">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="0462d-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0462d-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0462d-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0462d-133">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="0462d-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0462d-134">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="0462d-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0462d-135">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="0462d-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0462d-136">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="0462d-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0462d-137">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="0462d-137">The default value is 10.</span></span>

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

### <span data-ttu-id="0462d-138">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0462d-138">-Context</span></span>
<span data-ttu-id="0462d-139">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0462d-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="0462d-140">Per ottenere un contesto, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0462d-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0462d-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0462d-141">-DefaultProfile</span></span>
<span data-ttu-id="0462d-142">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0462d-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0462d-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="0462d-143">-DestContext</span></span>
<span data-ttu-id="0462d-144">Specifica il contesto di archiviazione di Azure della destinazione.</span><span class="sxs-lookup"><span data-stu-id="0462d-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="0462d-145">Per ottenere un contesto, USA **New-AzStorageContext**.</span><span class="sxs-lookup"><span data-stu-id="0462d-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="0462d-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="0462d-146">-DestFile</span></span>
<span data-ttu-id="0462d-147">Specifica un oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="0462d-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="0462d-148">È possibile creare un file cloud o ottenerne uno usando il cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="0462d-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0462d-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="0462d-149">-DestFilePath</span></span>
<span data-ttu-id="0462d-150">Specifica il percorso del file di destinazione relativo alla condivisione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0462d-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="0462d-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="0462d-151">-DestShareName</span></span>
<span data-ttu-id="0462d-152">Specifica il nome della condivisione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0462d-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="0462d-153">-Force</span><span class="sxs-lookup"><span data-stu-id="0462d-153">-Force</span></span>
<span data-ttu-id="0462d-154">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0462d-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0462d-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0462d-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0462d-156">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="0462d-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0462d-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="0462d-157">-SrcBlob</span></span>
<span data-ttu-id="0462d-158">Specifica un oggetto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="0462d-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="0462d-159">È possibile creare un BLOB cloud o ottenerne uno usando il cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="0462d-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0462d-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="0462d-160">-SrcBlobName</span></span>
<span data-ttu-id="0462d-161">Specifica il nome del BLOB di origine.</span><span class="sxs-lookup"><span data-stu-id="0462d-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="0462d-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="0462d-162">-SrcContainer</span></span>
<span data-ttu-id="0462d-163">Specifica un oggetto contenitore BLOB cloud.</span><span class="sxs-lookup"><span data-stu-id="0462d-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="0462d-164">Puoi creare un oggetto contenitore BLOB di cloud o usare il cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="0462d-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0462d-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="0462d-165">-SrcContainerName</span></span>
<span data-ttu-id="0462d-166">Specifica il nome del contenitore di origine.</span><span class="sxs-lookup"><span data-stu-id="0462d-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="0462d-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="0462d-167">-SrcFile</span></span>
<span data-ttu-id="0462d-168">Specifica un oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="0462d-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="0462d-169">È possibile creare un file cloud o ottenerne uno utilizzando **Get-AzStorageFile**.</span><span class="sxs-lookup"><span data-stu-id="0462d-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0462d-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="0462d-170">-SrcFilePath</span></span>
<span data-ttu-id="0462d-171">Specifica il percorso del file di origine relativo alla directory di origine o alla condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="0462d-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="0462d-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="0462d-172">-SrcShare</span></span>
<span data-ttu-id="0462d-173">Specifica un oggetto condivisione file cloud.</span><span class="sxs-lookup"><span data-stu-id="0462d-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="0462d-174">È possibile creare una condivisione di file cloud o ottenerne una usando il cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="0462d-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: CloudFileShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0462d-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="0462d-175">-SrcShareName</span></span>
<span data-ttu-id="0462d-176">Specifica il nome della condivisione di origine.</span><span class="sxs-lookup"><span data-stu-id="0462d-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="0462d-177">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0462d-177">-Confirm</span></span>
<span data-ttu-id="0462d-178">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0462d-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0462d-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0462d-179">-WhatIf</span></span>
<span data-ttu-id="0462d-180">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0462d-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0462d-181">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0462d-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0462d-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0462d-182">CommonParameters</span></span>
<span data-ttu-id="0462d-183">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0462d-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0462d-184">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0462d-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0462d-185">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0462d-185">INPUTS</span></span>

### <span data-ttu-id="0462d-186">Microsoft. Azure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0462d-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="0462d-187">Microsoft. Azure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="0462d-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="0462d-188">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0462d-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0462d-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0462d-189">OUTPUTS</span></span>

### <span data-ttu-id="0462d-190">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="0462d-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="0462d-191">Note</span><span class="sxs-lookup"><span data-stu-id="0462d-191">NOTES</span></span>

## <span data-ttu-id="0462d-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0462d-192">RELATED LINKS</span></span>

[<span data-ttu-id="0462d-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0462d-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="0462d-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0462d-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="0462d-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="0462d-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="0462d-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="0462d-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="0462d-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="0462d-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="0462d-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0462d-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
