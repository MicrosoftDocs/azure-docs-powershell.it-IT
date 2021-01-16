---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349531"
---
# <span data-ttu-id="64180-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="64180-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="64180-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64180-102">SYNOPSIS</span></span>
<span data-ttu-id="64180-103">Creare un file o una directory in un filesystem.</span><span class="sxs-lookup"><span data-stu-id="64180-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="64180-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64180-104">SYNTAX</span></span>

### <span data-ttu-id="64180-105">File (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64180-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64180-106">Directory</span><span class="sxs-lookup"><span data-stu-id="64180-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64180-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64180-107">DESCRIPTION</span></span>
<span data-ttu-id="64180-108">Il cmdlet **New-AzDataLakeGen2Item** crea un file o una directory in un filesystem in un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="64180-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="64180-109">Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="64180-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="64180-110">Questo tipo di account può essere creato eseguendo il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="64180-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="64180-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64180-111">EXAMPLES</span></span>

### <span data-ttu-id="64180-112">Esempio 1: creare una directory con autorizzazioni, umask, proprietà e metadati specificati</span><span class="sxs-lookup"><span data-stu-id="64180-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="64180-113">Questo comando crea una directory con autorizzazioni, umask, proprietà e metadati specificati</span><span class="sxs-lookup"><span data-stu-id="64180-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="64180-114">Esempio 2: creare (caricare) un file di data Lake da un file di origine locale e il cmdlet viene eseguito in background</span><span class="sxs-lookup"><span data-stu-id="64180-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="64180-115">Questo comando Crea (caricare) un file di data Lake da un file di origine locale e il cmdlet viene eseguito in background.</span><span class="sxs-lookup"><span data-stu-id="64180-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="64180-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64180-116">PARAMETERS</span></span>

### <span data-ttu-id="64180-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64180-117">-AsJob</span></span>
<span data-ttu-id="64180-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="64180-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64180-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="64180-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="64180-120">La quantità totale di attività asincrone simultanee.</span><span class="sxs-lookup"><span data-stu-id="64180-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="64180-121">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="64180-121">The default value is 10.</span></span>

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

### <span data-ttu-id="64180-122">-Contesto</span><span class="sxs-lookup"><span data-stu-id="64180-122">-Context</span></span>
<span data-ttu-id="64180-123">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="64180-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="64180-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64180-124">-DefaultProfile</span></span>
<span data-ttu-id="64180-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64180-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64180-126">-Directory</span><span class="sxs-lookup"><span data-stu-id="64180-126">-Directory</span></span>
<span data-ttu-id="64180-127">Indica che il nuovo elemento è una directory e non un file.</span><span class="sxs-lookup"><span data-stu-id="64180-127">Indicates that this new item is a directory and not a file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Directory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64180-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="64180-128">-FileSystem</span></span>
<span data-ttu-id="64180-129">Nome FileSystem</span><span class="sxs-lookup"><span data-stu-id="64180-129">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64180-130">-Force</span><span class="sxs-lookup"><span data-stu-id="64180-130">-Force</span></span>
<span data-ttu-id="64180-131">Se passato, viene creato un nuovo elemento senza alcuna richiesta</span><span class="sxs-lookup"><span data-stu-id="64180-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="64180-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="64180-132">-Metadata</span></span>
<span data-ttu-id="64180-133">Specifica i metadati per la directory o il file creato.</span><span class="sxs-lookup"><span data-stu-id="64180-133">Specifies metadata for the created directory or file.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64180-134">-Path</span><span class="sxs-lookup"><span data-stu-id="64180-134">-Path</span></span>
<span data-ttu-id="64180-135">Il percorso nel filesystem specificato che deve essere creato.</span><span class="sxs-lookup"><span data-stu-id="64180-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="64180-136">Può essere un file o una directory nel formato ' directory/file.txt' o ' directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="64180-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64180-137">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="64180-137">-Permission</span></span>
<span data-ttu-id="64180-138">Imposta le autorizzazioni di accesso POSIX per il proprietario del file, il gruppo proprietario file e altri.</span><span class="sxs-lookup"><span data-stu-id="64180-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="64180-139">A ogni classe può essere concessa l'autorizzazione di lettura, scrittura o esecuzione.</span><span class="sxs-lookup"><span data-stu-id="64180-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="64180-140">Il simbolo (rwxrw-RW-) è supportato.</span><span class="sxs-lookup"><span data-stu-id="64180-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="64180-141">-Property</span><span class="sxs-lookup"><span data-stu-id="64180-141">-Property</span></span>
<span data-ttu-id="64180-142">Specifica le proprietà per la directory o il file creato.</span><span class="sxs-lookup"><span data-stu-id="64180-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="64180-143">Le proprietà supportate per file sono: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="64180-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="64180-144">Le proprietà supportate per la directory sono: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="64180-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64180-145">-Origine</span><span class="sxs-lookup"><span data-stu-id="64180-145">-Source</span></span>
<span data-ttu-id="64180-146">Specifica il percorso del file di origine locale che verrà caricato in un file datalake Gen2.</span><span class="sxs-lookup"><span data-stu-id="64180-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64180-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="64180-147">-Umask</span></span>
<span data-ttu-id="64180-148">Quando si crea un nuovo elemento e la directory padre non ha un ACL predefinito, umask limita le autorizzazioni del file o della directory da creare.</span><span class="sxs-lookup"><span data-stu-id="64180-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="64180-149">L'autorizzazione risultante viene fornita da p & ^ u, dove p è l'autorizzazione e si è umask.</span><span class="sxs-lookup"><span data-stu-id="64180-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="64180-150">Il simbolo (rwxrw-RW-) è supportato.</span><span class="sxs-lookup"><span data-stu-id="64180-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="64180-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64180-151">-Confirm</span></span>
<span data-ttu-id="64180-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64180-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64180-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64180-153">-WhatIf</span></span>
<span data-ttu-id="64180-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64180-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64180-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64180-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64180-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64180-156">CommonParameters</span></span>
<span data-ttu-id="64180-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64180-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64180-158">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64180-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64180-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64180-159">INPUTS</span></span>

### <span data-ttu-id="64180-160">System. String</span><span class="sxs-lookup"><span data-stu-id="64180-160">System.String</span></span>

### <span data-ttu-id="64180-161">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="64180-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="64180-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64180-162">OUTPUTS</span></span>

### <span data-ttu-id="64180-163">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="64180-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="64180-164">Note</span><span class="sxs-lookup"><span data-stu-id="64180-164">NOTES</span></span>

## <span data-ttu-id="64180-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64180-165">RELATED LINKS</span></span>
