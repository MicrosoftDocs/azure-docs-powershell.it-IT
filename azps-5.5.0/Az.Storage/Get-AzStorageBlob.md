---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 44c14b1f5aa8426bfb78205fa66a53d7db7e3440
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190902"
---
# <span data-ttu-id="394de-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="394de-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="394de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="394de-102">SYNOPSIS</span></span>
<span data-ttu-id="394de-103">Elenca i BLOB in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="394de-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="394de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="394de-104">SYNTAX</span></span>

### <span data-ttu-id="394de-105">BLOBName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="394de-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="394de-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="394de-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="394de-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="394de-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="394de-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="394de-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="394de-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="394de-109">DESCRIPTION</span></span>
<span data-ttu-id="394de-110">Il cmdlet **Get-AzStorageBlob** elenca i BLOB nel contenitore specificato in un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="394de-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="394de-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="394de-111">EXAMPLES</span></span>

### <span data-ttu-id="394de-112">Esempio 1: Ottenere un BLOB in base al nome di blob</span><span class="sxs-lookup"><span data-stu-id="394de-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="394de-113">Questo comando usa un nome BLOB e un carattere jolly per ottenere un BLOB.</span><span class="sxs-lookup"><span data-stu-id="394de-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="394de-114">Esempio 2: Ottenere BLOB in un contenitore tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="394de-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="394de-115">Questo comando usa la pipeline per ottenere tutti i BLOB (inclusi i BLOB nello stato Eliminato) in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="394de-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="394de-116">Esempio 3: Ottenere i BLOB in base al prefisso del nome</span><span class="sxs-lookup"><span data-stu-id="394de-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="394de-117">Questo comando usa un prefisso del nome per ottenere BLOB.</span><span class="sxs-lookup"><span data-stu-id="394de-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="394de-118">Esempio 4: Elencare BLOB in più batch</span><span class="sxs-lookup"><span data-stu-id="394de-118">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="394de-119">Questo esempio usa i *parametri MaxCount* e *ContinuationToken* per elencare i BLOB di Archiviazione di Azure in più batch.</span><span class="sxs-lookup"><span data-stu-id="394de-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="394de-120">I primi quattro comandi assegnano valori alle variabili da usare nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="394de-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="394de-121">Il quinto comando specifica **un'istruzione Do-While** che usa il cmdlet **Get-AzStorageBlob** per ottenere BLOB.</span><span class="sxs-lookup"><span data-stu-id="394de-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="394de-122">L'istruzione include il token di continuazione archiviato nella $Token variabile.</span><span class="sxs-lookup"><span data-stu-id="394de-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="394de-123">$Token modifica il valore durante l'esecuzione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="394de-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="394de-124">Per altre informazioni, digitare `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="394de-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="394de-125">Il comando finale usa il **comando Eco** schermo per visualizzare il totale.</span><span class="sxs-lookup"><span data-stu-id="394de-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="394de-126">Esempio 5: Tutti i BLOB in un contenitore includono la versione BLOB</span><span class="sxs-lookup"><span data-stu-id="394de-126">Example 5: Get all blobs in a container include blob version</span></span>
```
PS C:\>Get-AzStorageBlob -Container "containername"  -IncludeVersion 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.2432658Z  
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False                                    
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.8598431Z *  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:35Z Hot                                     False      2020-07-03T16:19:35.2381110Z *
```

<span data-ttu-id="394de-127">Questo comando recupera tutti i BLOB in un contenitore include la versione BLOB.</span><span class="sxs-lookup"><span data-stu-id="394de-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="394de-128">Esempio 6: Ottenere una singola versione BLOB</span><span class="sxs-lookup"><span data-stu-id="394de-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="394de-129">Questo comando ottiene un singolo BLOB con VersionId.</span><span class="sxs-lookup"><span data-stu-id="394de-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="394de-130">Esempio 7: Ottenere un singolo snapshot BLOB</span><span class="sxs-lookup"><span data-stu-id="394de-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="394de-131">Questo comando ottiene un singolo snapshot BLOB con SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="394de-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="394de-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="394de-132">PARAMETERS</span></span>

### <span data-ttu-id="394de-133">-BLOB</span><span class="sxs-lookup"><span data-stu-id="394de-133">-Blob</span></span>
<span data-ttu-id="394de-134">Specifica un nome o un modello di nome, che può essere usato per una ricerca con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="394de-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="394de-135">Se non si specifica alcun nome BLOB, il cmdlet elenca tutti i BLOB nel contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="394de-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="394de-136">Se per questo parametro è specificato un valore, il cmdlet elenca tutti i BLOB con nomi corrispondenti a questo parametro.</span><span class="sxs-lookup"><span data-stu-id="394de-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="394de-137">Questo parametro supporta i caratteri jolly in qualsiasi punto della stringa.</span><span class="sxs-lookup"><span data-stu-id="394de-137">This parameter supports wildcards anywhere in the string.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SingleBlobSnapshotTime, SingleBlobVersionID
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394de-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="394de-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="394de-139">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="394de-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="394de-140">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="394de-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="394de-141">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="394de-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="394de-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="394de-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="394de-143">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="394de-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="394de-144">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="394de-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="394de-145">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="394de-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="394de-146">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="394de-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="394de-147">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="394de-147">The default value is 10.</span></span>

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

### <span data-ttu-id="394de-148">-Container</span><span class="sxs-lookup"><span data-stu-id="394de-148">-Container</span></span>
<span data-ttu-id="394de-149">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="394de-149">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="394de-150">-Context</span><span class="sxs-lookup"><span data-stu-id="394de-150">-Context</span></span>
<span data-ttu-id="394de-151">Specifica l'account di archiviazione di Azure da cui si vuole ottenere un elenco di BLOB.</span><span class="sxs-lookup"><span data-stu-id="394de-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="394de-152">È possibile usare il cmdlet New-AzStorageContext per creare un contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="394de-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="394de-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="394de-153">-ContinuationToken</span></span>
<span data-ttu-id="394de-154">Specifica un token di continuazione per l'elenco BLOB.</span><span class="sxs-lookup"><span data-stu-id="394de-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="394de-155">Usare questo parametro e il *parametro MaxCount* per elencare i BLOB in più batch.</span><span class="sxs-lookup"><span data-stu-id="394de-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394de-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="394de-156">-DefaultProfile</span></span>
<span data-ttu-id="394de-157">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="394de-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="394de-158">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="394de-158">-IncludeDeleted</span></span>
<span data-ttu-id="394de-159">Includere BLOB eliminati, per impostazione predefinita il BLOB di get non includerà BLOB eliminati.</span><span class="sxs-lookup"><span data-stu-id="394de-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="394de-160">-IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="394de-160">-IncludeVersion</span></span>
<span data-ttu-id="394de-161">Le versioni DEI BLOB verranno elencate solo se questo parametro è presente e per impostazione predefinita get BLOB non include le versioni BLOB.</span><span class="sxs-lookup"><span data-stu-id="394de-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394de-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="394de-162">-MaxCount</span></span>
<span data-ttu-id="394de-163">Specifica il numero massimo di oggetti restituiti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="394de-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="394de-164">-Prefix</span><span class="sxs-lookup"><span data-stu-id="394de-164">-Prefix</span></span>
<span data-ttu-id="394de-165">Specifica un prefisso per i nomi DEI BLOB da ottenere.</span><span class="sxs-lookup"><span data-stu-id="394de-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="394de-166">Questo parametro non supporta l'uso di espressioni regolari o caratteri jolly per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="394de-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="394de-167">Questo significa che se il contenitore include solo BLOB denominati "My", "MyBlob1" e "MyBlob2" e si specifica "-Prefix My\*", il cmdlet non restituisce BLOB.</span><span class="sxs-lookup"><span data-stu-id="394de-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="394de-168">Tuttavia, se si specifica "-Prefix My", il cmdlet restituisce "My", "MyBlob1" e "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="394de-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394de-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="394de-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="394de-170">Specifica l'intervallo di timeout del lato servizio, in secondi, per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="394de-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="394de-171">Se prima dell'elaborazione della richiesta da parte del servizio è trascorso l'intervallo specificato, il servizio di archiviazione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="394de-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="394de-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="394de-172">-SnapshotTime</span></span>
<span data-ttu-id="394de-173">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="394de-173">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: SingleBlobSnapshotTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394de-174">-VersionId</span><span class="sxs-lookup"><span data-stu-id="394de-174">-VersionId</span></span>
<span data-ttu-id="394de-175">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="394de-175">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: SingleBlobVersionID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394de-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="394de-176">CommonParameters</span></span>
<span data-ttu-id="394de-177">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="394de-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="394de-178">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="394de-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="394de-179">INPUT</span><span class="sxs-lookup"><span data-stu-id="394de-179">INPUTS</span></span>

### <span data-ttu-id="394de-180">System.String</span><span class="sxs-lookup"><span data-stu-id="394de-180">System.String</span></span>

### <span data-ttu-id="394de-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="394de-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="394de-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="394de-182">OUTPUTS</span></span>

### <span data-ttu-id="394de-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="394de-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="394de-184">NOTE</span><span class="sxs-lookup"><span data-stu-id="394de-184">NOTES</span></span>

## <span data-ttu-id="394de-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="394de-185">RELATED LINKS</span></span>

[<span data-ttu-id="394de-186">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="394de-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="394de-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="394de-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="394de-188">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="394de-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


