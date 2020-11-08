---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
ms.openlocfilehash: 72c3f13749088763348c60ebd27f4d024219c55e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190038"
---
# <span data-ttu-id="4156d-101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4156d-101">Get-AzStorageFileHandle</span></span>

## <span data-ttu-id="4156d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4156d-102">SYNOPSIS</span></span>
<span data-ttu-id="4156d-103">Elenca gli handle di file di una condivisione file, una directory di file o un file.</span><span class="sxs-lookup"><span data-stu-id="4156d-103">Lists file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="4156d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4156d-104">SYNTAX</span></span>

### <span data-ttu-id="4156d-105">ShareName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4156d-105">ShareName (Default)</span></span>
```
Get-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4156d-106">Condividi</span><span class="sxs-lookup"><span data-stu-id="4156d-106">Share</span></span>
```
Get-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4156d-107">Directory</span><span class="sxs-lookup"><span data-stu-id="4156d-107">Directory</span></span>
```
Get-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4156d-108">File</span><span class="sxs-lookup"><span data-stu-id="4156d-108">File</span></span>
```
Get-AzStorageFileHandle [-File] <CloudFile> [-Recursive] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="4156d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4156d-109">DESCRIPTION</span></span>
<span data-ttu-id="4156d-110">Il cmdlet **Get-AzStorageFileHandle** elenca gli handle di file di una condivisione file o di un file o di una directory.</span><span class="sxs-lookup"><span data-stu-id="4156d-110">The **Get-AzStorageFileHandle** cmdlet lists file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="4156d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4156d-111">EXAMPLES</span></span>

### <span data-ttu-id="4156d-112">Esempio 1: elenca tutti gli handle di file in una condivisione file ricorsivamente e ordina in base a ClientIp e OpenTime</span><span class="sxs-lookup"><span data-stu-id="4156d-112">Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Recursive | Sort-Object ClientIP,OpenTime 

HandleId    Path                  ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----                  --------       ---------- --------             ----------------- ------               --------             ---------          
28506980357                       104.46.105.229 49805      2019-07-29 08:37:36Z                   0                    0                    9297571480349046273
28506980537 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28506980538 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28582543365                       104.46.119.170 51675      2019-07-30 09:29:32Z                   0                    0                    9477733061320772929
28582543375 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
28582543376 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
```

<span data-ttu-id="4156d-113">Questo comando elenca gli handle di file in una condivisione file e ordina l'output per ClientIp, quindi per OpenTime.</span><span class="sxs-lookup"><span data-stu-id="4156d-113">This command lists file handles on a file share, and sort the output by ClientIp, then by OpenTime.</span></span>

### <span data-ttu-id="4156d-114">Esempio 2: elencare i primi 2 handle di file in una directory di file ricorsivamente</span><span class="sxs-lookup"><span data-stu-id="4156d-114">Example 2: List first 2 file handles on a file directory recursively</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
```

<span data-ttu-id="4156d-115">Questo comando elenca i primi 2 handle di file in una directory di file in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="4156d-115">This command lists first 2 file handles on a file directory recursively .</span></span>

### <span data-ttu-id="4156d-116">Esempio 3: elencare i quadratini di file da 3 a 6 in un file</span><span class="sxs-lookup"><span data-stu-id="4156d-116">Example 3: List the 3rd to the 6th file handles on a file</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -skip 2 -First 4 

HandleId    Path               ClientIp       ClientPort OpenTime             LastReconnectTime FileId              ParentId             SessionId          
--------    ----               --------       ---------- --------             ----------------- ------              --------             ---------          
24055513248 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513249 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513252 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
24055513253 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
```

<span data-ttu-id="4156d-117">Questo comando elenca il 3 ° al 6 ° handle di file in un file.</span><span class="sxs-lookup"><span data-stu-id="4156d-117">This command lists the 3rd to the 6th file handles on a file.</span></span>

## <span data-ttu-id="4156d-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4156d-118">PARAMETERS</span></span>

### <span data-ttu-id="4156d-119">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4156d-119">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4156d-120">Il tempo di esecuzione massimo lato client per ogni richiesta in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="4156d-120">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="4156d-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4156d-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4156d-122">La quantità totale di attività asincrone simultanee.</span><span class="sxs-lookup"><span data-stu-id="4156d-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="4156d-123">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="4156d-123">The default value is 10.</span></span>

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

### <span data-ttu-id="4156d-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4156d-124">-Context</span></span>
<span data-ttu-id="4156d-125">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="4156d-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="4156d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4156d-126">-DefaultProfile</span></span>
<span data-ttu-id="4156d-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4156d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4156d-128">-Directory</span><span class="sxs-lookup"><span data-stu-id="4156d-128">-Directory</span></span>
<span data-ttu-id="4156d-129">L'oggetto CloudFileDirectory ha indicato la cartella di base in cui verranno elencati i file e le directory.</span><span class="sxs-lookup"><span data-stu-id="4156d-129">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="4156d-130">-File</span><span class="sxs-lookup"><span data-stu-id="4156d-130">-File</span></span>
<span data-ttu-id="4156d-131">L'oggetto CloudFile ha indicato il file per elencare gli handle di file.</span><span class="sxs-lookup"><span data-stu-id="4156d-131">CloudFile object indicated the file to list File Handles.</span></span>

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

### <span data-ttu-id="4156d-132">-Path</span><span class="sxs-lookup"><span data-stu-id="4156d-132">-Path</span></span>
<span data-ttu-id="4156d-133">Percorso di un file/directory esistente.</span><span class="sxs-lookup"><span data-stu-id="4156d-133">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4156d-134">-Ricorsiva</span><span class="sxs-lookup"><span data-stu-id="4156d-134">-Recursive</span></span>
<span data-ttu-id="4156d-135">Handle di elenco in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="4156d-135">List handles Recursively.</span></span>
<span data-ttu-id="4156d-136">Funziona solo nella directory di file.</span><span class="sxs-lookup"><span data-stu-id="4156d-136">Only works on File Directory.</span></span>

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

### <span data-ttu-id="4156d-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4156d-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4156d-138">Timeout del server per ogni richiesta in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="4156d-138">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="4156d-139">-Condividi</span><span class="sxs-lookup"><span data-stu-id="4156d-139">-Share</span></span>
<span data-ttu-id="4156d-140">L'oggetto CloudFileShare indica la condivisione in cui verranno elencati i file e le directory.</span><span class="sxs-lookup"><span data-stu-id="4156d-140">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="4156d-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4156d-141">-ShareName</span></span>
<span data-ttu-id="4156d-142">Nome della condivisione file in cui verranno elencati i file e le directory.</span><span class="sxs-lookup"><span data-stu-id="4156d-142">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="4156d-143">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="4156d-143">-IncludeTotalCount</span></span>
<span data-ttu-id="4156d-144">Indica il numero di oggetti nel set di dati (un numero intero) seguito dagli oggetti.</span><span class="sxs-lookup"><span data-stu-id="4156d-144">Reports the number of objects in the data set (an integer) followed by the objects.</span></span> <span data-ttu-id="4156d-145">Se il cmdlet non riesce a determinare il conteggio totale, restituisce "numero totale sconosciuto".</span><span class="sxs-lookup"><span data-stu-id="4156d-145">If the cmdlet cannot determine the total count, it returns 'Unknown total count'.</span></span>
<span data-ttu-id="4156d-146">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="4156d-146">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="4156d-147">-Skip</span><span class="sxs-lookup"><span data-stu-id="4156d-147">-Skip</span></span>
<span data-ttu-id="4156d-148">Ignora i primi oggetti "n" e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="4156d-148">Ignores the first 'n' objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4156d-149">-Primo</span><span class="sxs-lookup"><span data-stu-id="4156d-149">-First</span></span>
<span data-ttu-id="4156d-150">Ottiene solo i primi oggetti "n".</span><span class="sxs-lookup"><span data-stu-id="4156d-150">Gets only the first 'n' objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4156d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4156d-151">CommonParameters</span></span>
<span data-ttu-id="4156d-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4156d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4156d-153">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4156d-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4156d-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4156d-154">INPUTS</span></span>

### <span data-ttu-id="4156d-155">Microsoft. Azure. storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4156d-155">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="4156d-156">Microsoft. Azure. storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="4156d-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="4156d-157">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4156d-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4156d-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4156d-158">OUTPUTS</span></span>

### <span data-ttu-id="4156d-159">Microsoft. Azure. storage. file. FileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="4156d-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span></span>

## <span data-ttu-id="4156d-160">Note</span><span class="sxs-lookup"><span data-stu-id="4156d-160">NOTES</span></span>

## <span data-ttu-id="4156d-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4156d-161">RELATED LINKS</span></span>