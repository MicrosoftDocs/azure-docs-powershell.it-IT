---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190558"
---
# <span data-ttu-id="2b5e6-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="2b5e6-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="2b5e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="2b5e6-103">Crea un file di risorse per l'utilizzo `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="2b5e6-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="2b5e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b5e6-104">SYNTAX</span></span>

### <span data-ttu-id="2b5e6-105">HttpUrl (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b5e6-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b5e6-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="2b5e6-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b5e6-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="2b5e6-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b5e6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b5e6-108">DESCRIPTION</span></span>
<span data-ttu-id="2b5e6-109">Crea un file di risorse per l'utilizzo `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="2b5e6-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="2b5e6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b5e6-110">EXAMPLES</span></span>

### <span data-ttu-id="2b5e6-111">Esempio 1: creare un file di risorse da un URL HTTP che punta a un singolo file</span><span class="sxs-lookup"><span data-stu-id="2b5e6-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="2b5e6-112">Crea un `PSResourceFile` riferimento a un URL http.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="2b5e6-113">Esempio 2: creare un file di risorse da un URL del contenitore di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="2b5e6-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="2b5e6-114">Crea un `PSResourceFile` riferimento a un URL del contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="2b5e6-115">Tutti i file nel contenitore verranno scaricati nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="2b5e6-116">Esempio 3: creare un file di risorse da un nome di contenitore di archiviazione automatico</span><span class="sxs-lookup"><span data-stu-id="2b5e6-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="2b5e6-117">Crea un `PSResourceFile` riferimento a un nome di contenitore di archiviazione automatico.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="2b5e6-118">Tutti i file nel contenitore verranno scaricati nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="2b5e6-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b5e6-119">PARAMETERS</span></span>

### <span data-ttu-id="2b5e6-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="2b5e6-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="2b5e6-121">Nome del contenitore di archiviazione nell'account di archiviazione automatica.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-121">The storage container name in the auto storage account.</span></span>

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

### <span data-ttu-id="2b5e6-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="2b5e6-122">-BlobPrefix</span></span>
<span data-ttu-id="2b5e6-123">Ottiene il prefisso BLOB da usare per il download di BLOB da un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="2b5e6-124">Verranno scaricati solo i BLOB i cui nomi iniziano con il prefisso specificato.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="2b5e6-125">Questo prefisso può essere un nome di file parziale o una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="2b5e6-126">Se non si specifica un prefisso, verranno scaricati tutti i file nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

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

### <span data-ttu-id="2b5e6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b5e6-127">-DefaultProfile</span></span>
<span data-ttu-id="2b5e6-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b5e6-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="2b5e6-129">-FileMode</span></span>
<span data-ttu-id="2b5e6-130">Ottiene l'attributo della modalità di autorizzazione file in formato ottale.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="2b5e6-131">Questa proprietà è applicabile solo se il file di risorse viene scaricato in un nodo Linux.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="2b5e6-132">Se questa proprietà non è specificata per un nodo Linux, il valore predefinito è 0770.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="2b5e6-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="2b5e6-133">-FilePath</span></span>
<span data-ttu-id="2b5e6-134">Posizione del nodo Compute a cui scaricare i file, relativo alla directory di lavoro dell'attività.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="2b5e6-135">Se il parametro HttpUrl è specificato, il filePath è obbligatorio e descrive il percorso in cui verrà scaricato il file, incluso il nome del documento.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="2b5e6-136">In caso contrario, se sono specificati i parametri AutoStorageContainerName o StorageContainerUrl, filePath è facoltativo ed è la directory in cui scaricare i file.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="2b5e6-137">Nel caso in cui FilePath viene usato come directory, qualsiasi struttura di directory già associata ai dati di input verrà mantenuta integralmente e accodata alla directory FilePath specificata.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="2b5e6-138">Il percorso relativo specificato non può uscire dalla directory di lavoro dell'attività, ad esempio usando "..".</span><span class="sxs-lookup"><span data-stu-id="2b5e6-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

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

### <span data-ttu-id="2b5e6-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="2b5e6-139">-HttpUrl</span></span>
<span data-ttu-id="2b5e6-140">URL del file da scaricare.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-140">The URL of the file to download.</span></span>
<span data-ttu-id="2b5e6-141">Se l'URL è archiviazione BLOB di Azure, deve essere leggibile usando l'accesso anonimo; in altri casi, il servizio batch non presenta alcuna credenziale durante il download del BLOB.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="2b5e6-142">Esistono due modi per ottenere un URL di questo tipo per un BLOB in Azure Storage: includere una firma di accesso condiviso (SAS) che concede le autorizzazioni di lettura per il BLOB o imposta l'ACL per il BLOB o il relativo contenitore per consentire l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

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

### <span data-ttu-id="2b5e6-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="2b5e6-143">-StorageContainerUrl</span></span>
<span data-ttu-id="2b5e6-144">URL del contenitore di BLOB nell'archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="2b5e6-145">Questo URL deve essere leggibile ed elencabile usando l'accesso anonimo; il servizio batch non presenta credenziali durante il download di BLOB dal contenitore.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="2b5e6-146">Esistono due modi per ottenere un URL di questo tipo per un contenitore in Azure Storage: includere una firma di accesso condiviso (SAS) che concede le autorizzazioni di lettura per il contenitore o imposta l'ACL per il contenitore per consentire l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

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

### <span data-ttu-id="2b5e6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b5e6-147">CommonParameters</span></span>
<span data-ttu-id="2b5e6-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b5e6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b5e6-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b5e6-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b5e6-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b5e6-150">INPUTS</span></span>

### <span data-ttu-id="2b5e6-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2b5e6-151">None</span></span>

## <span data-ttu-id="2b5e6-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b5e6-152">OUTPUTS</span></span>

### <span data-ttu-id="2b5e6-153">Microsoft.Azure.Commands.Batch. Models. PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="2b5e6-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="2b5e6-154">Note</span><span class="sxs-lookup"><span data-stu-id="2b5e6-154">NOTES</span></span>

## <span data-ttu-id="2b5e6-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b5e6-155">RELATED LINKS</span></span>

[<span data-ttu-id="2b5e6-156">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2b5e6-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)