---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: f8df4d49f0181b7cf8abf2581a522f953f3f2df7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007341"
---
# <span data-ttu-id="f55c2-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="f55c2-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="f55c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f55c2-102">SYNOPSIS</span></span>
<span data-ttu-id="f55c2-103">Crea un file di risorse per l'utilizzo da parte di `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="f55c2-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="f55c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f55c2-104">SYNTAX</span></span>

### <span data-ttu-id="f55c2-105">HttpUrl (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f55c2-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f55c2-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="f55c2-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f55c2-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="f55c2-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f55c2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f55c2-108">DESCRIPTION</span></span>
<span data-ttu-id="f55c2-109">Crea un file di risorse per l'utilizzo da parte di `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="f55c2-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="f55c2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f55c2-110">EXAMPLES</span></span>

### <span data-ttu-id="f55c2-111">Esempio 1: Creare un file di risorse da un URL HTTP che punta a un singolo file</span><span class="sxs-lookup"><span data-stu-id="f55c2-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="f55c2-112">Crea un `PSResourceFile` riferimento a un URL HTTP.</span><span class="sxs-lookup"><span data-stu-id="f55c2-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="f55c2-113">Esempio 2: Creare un file di risorse da un URL del contenitore di Archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="f55c2-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="f55c2-114">Crea un riferimento `PSResourceFile` a un URL del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f55c2-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="f55c2-115">Tutti i file nel contenitore verranno scaricati nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="f55c2-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="f55c2-116">Esempio 3: Creare un file di risorse da un nome di contenitore archiviazione automatica</span><span class="sxs-lookup"><span data-stu-id="f55c2-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="f55c2-117">Crea un riferimento `PSResourceFile` a un nome di contenitore Archiviazione automatica.</span><span class="sxs-lookup"><span data-stu-id="f55c2-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="f55c2-118">Tutti i file nel contenitore verranno scaricati nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="f55c2-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="f55c2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f55c2-119">PARAMETERS</span></span>

### <span data-ttu-id="f55c2-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="f55c2-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="f55c2-121">Nome del contenitore di archiviazione nell'account di archiviazione automatico.</span><span class="sxs-lookup"><span data-stu-id="f55c2-121">The storage container name in the auto storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55c2-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="f55c2-122">-BlobPrefix</span></span>
<span data-ttu-id="f55c2-123">Ottiene il prefisso BLOB da usare per il download di BLOB da un contenitore di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f55c2-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="f55c2-124">Verranno scaricati solo i BLOB i cui nomi iniziano con il prefisso specificato.</span><span class="sxs-lookup"><span data-stu-id="f55c2-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="f55c2-125">Il prefisso può essere un nome file parziale o una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="f55c2-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="f55c2-126">Se non si specificato un prefisso, verranno scaricati tutti i file nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="f55c2-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55c2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55c2-127">-DefaultProfile</span></span>
<span data-ttu-id="f55c2-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f55c2-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55c2-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="f55c2-129">-FileMode</span></span>
<span data-ttu-id="f55c2-130">Ottiene l'attributo della modalità di autorizzazione file in formato ottale.</span><span class="sxs-lookup"><span data-stu-id="f55c2-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="f55c2-131">Questa proprietà è applicabile solo se il file di risorse viene scaricato in un nodo Linux.</span><span class="sxs-lookup"><span data-stu-id="f55c2-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="f55c2-132">Se questa proprietà non è specificata per un nodo Linux, il valore predefinito è 0770.</span><span class="sxs-lookup"><span data-stu-id="f55c2-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55c2-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="f55c2-133">-FilePath</span></span>
<span data-ttu-id="f55c2-134">Posizione nel nodo di elaborazione in cui scaricare i file, rispetto alla directory di lavoro dell'attività.</span><span class="sxs-lookup"><span data-stu-id="f55c2-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="f55c2-135">Se si specifica il parametro HttpUrl, filePath è obbligatorio e descrive il percorso in cui verrà scaricato il file, incluso il nome file.</span><span class="sxs-lookup"><span data-stu-id="f55c2-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="f55c2-136">In caso contrario, se vengono specificati i parametri AutoStorageContainerName o StorageContainerUrl, FilePath è facoltativo ed è la directory in cui scaricare i file.</span><span class="sxs-lookup"><span data-stu-id="f55c2-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="f55c2-137">Nel caso in cui FilePath viene usato come directory, tutte le strutture di directory già associate ai dati di input verranno conservate completamente e aggiunte alla directory FilePath specificata.</span><span class="sxs-lookup"><span data-stu-id="f55c2-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="f55c2-138">Il percorso relativo specificato non può uscire dalla directory di lavoro dell'attività (ad esempio usando '..').</span><span class="sxs-lookup"><span data-stu-id="f55c2-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55c2-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="f55c2-139">-HttpUrl</span></span>
<span data-ttu-id="f55c2-140">URL del file da scaricare.</span><span class="sxs-lookup"><span data-stu-id="f55c2-140">The URL of the file to download.</span></span>
<span data-ttu-id="f55c2-141">Se l'URL è Archiviazione BLOB Azure, deve essere leggibile con l'accesso anonimo; il servizio batch non presenta le credenziali durante il download del BLOB.</span><span class="sxs-lookup"><span data-stu-id="f55c2-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="f55c2-142">Esistono due modi per ottenere un URL di questo tipo per un BLOB in Archiviazione di Azure: includere una firma di accesso condiviso che concede autorizzazioni di lettura per il BLOB oppure impostare l'ACL per il BLOB o il contenitore per consentire l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="f55c2-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55c2-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="f55c2-143">-StorageContainerUrl</span></span>
<span data-ttu-id="f55c2-144">URL del contenitore BLOB all'interno di Archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="f55c2-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="f55c2-145">Questo URL deve essere leggibile ed elencabile utilizzando l'accesso anonimo; il servizio batch non presenta le credenziali durante il download di BLOB dal contenitore.</span><span class="sxs-lookup"><span data-stu-id="f55c2-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="f55c2-146">Esistono due modi per ottenere un URL di questo tipo per un contenitore in Archiviazione di Azure: includere una firma di accesso condiviso che concede autorizzazioni di lettura per il contenitore oppure impostare l'ACL per il contenitore in modo da consentire l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="f55c2-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55c2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55c2-147">CommonParameters</span></span>
<span data-ttu-id="f55c2-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f55c2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55c2-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f55c2-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55c2-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="f55c2-150">INPUTS</span></span>

### <span data-ttu-id="f55c2-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f55c2-151">None</span></span>

## <span data-ttu-id="f55c2-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f55c2-152">OUTPUTS</span></span>

### <span data-ttu-id="f55c2-153">Microsoft.Azure.Commands.Batch. Models.PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="f55c2-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="f55c2-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="f55c2-154">NOTES</span></span>

## <span data-ttu-id="f55c2-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f55c2-155">RELATED LINKS</span></span>

[<span data-ttu-id="f55c2-156">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f55c2-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)