---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 565267c6f35f52fd3a7a733477ed504d001cb70b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999220"
---
# <span data-ttu-id="9535d-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="9535d-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="9535d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9535d-102">SYNOPSIS</span></span>
<span data-ttu-id="9535d-103">Creare un file o una directory in un filesystem.</span><span class="sxs-lookup"><span data-stu-id="9535d-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="9535d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9535d-104">SYNTAX</span></span>

### <span data-ttu-id="9535d-105">File (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9535d-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9535d-106">Directory</span><span class="sxs-lookup"><span data-stu-id="9535d-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9535d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9535d-107">DESCRIPTION</span></span>
<span data-ttu-id="9535d-108">Il cmdlet **New-AzDataLakeGen2Item** crea un file o una directory in un Filesystem in un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9535d-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="9535d-109">Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9535d-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="9535d-110">Questo tipo di account può essere creato eseguire il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalZone $true".</span><span class="sxs-lookup"><span data-stu-id="9535d-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="9535d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9535d-111">EXAMPLES</span></span>

### <span data-ttu-id="9535d-112">Esempio 1: Creare una directory con autorizzazioni, Umask, proprietà e metadati specificati</span><span class="sxs-lookup"><span data-stu-id="9535d-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="9535d-113">Questo comando crea una directory con autorizzazioni, Umask, proprietà e metadati specificati</span><span class="sxs-lookup"><span data-stu-id="9535d-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="9535d-114">Esempio 2: Creare(caricare) un file data lake da un file di origine locale e il cmdlet viene eseguito in background</span><span class="sxs-lookup"><span data-stu-id="9535d-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="9535d-115">Questo comando crea(carica) un file data lake da un file di origine locale e il cmdlet viene eseguito in background.</span><span class="sxs-lookup"><span data-stu-id="9535d-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="9535d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9535d-116">PARAMETERS</span></span>

### <span data-ttu-id="9535d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9535d-117">-AsJob</span></span>
<span data-ttu-id="9535d-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9535d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9535d-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9535d-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9535d-120">La quantità totale di attività sincronizzate simultanee.</span><span class="sxs-lookup"><span data-stu-id="9535d-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="9535d-121">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="9535d-121">The default value is 10.</span></span>

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

### <span data-ttu-id="9535d-122">-Context</span><span class="sxs-lookup"><span data-stu-id="9535d-122">-Context</span></span>
<span data-ttu-id="9535d-123">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="9535d-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="9535d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9535d-124">-DefaultProfile</span></span>
<span data-ttu-id="9535d-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9535d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9535d-126">-Directory</span><span class="sxs-lookup"><span data-stu-id="9535d-126">-Directory</span></span>
<span data-ttu-id="9535d-127">Indica che il nuovo elemento è una directory e non un file.</span><span class="sxs-lookup"><span data-stu-id="9535d-127">Indicates that this new item is a directory and not a file.</span></span>

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

### <span data-ttu-id="9535d-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="9535d-128">-FileSystem</span></span>
<span data-ttu-id="9535d-129">Nome filesystem</span><span class="sxs-lookup"><span data-stu-id="9535d-129">FileSystem name</span></span>

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

### <span data-ttu-id="9535d-130">-Force</span><span class="sxs-lookup"><span data-stu-id="9535d-130">-Force</span></span>
<span data-ttu-id="9535d-131">Se il test viene superato, il nuovo elemento viene creato senza alcun prompt</span><span class="sxs-lookup"><span data-stu-id="9535d-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="9535d-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9535d-132">-Metadata</span></span>
<span data-ttu-id="9535d-133">Specifica i metadati per la directory o il file creato.</span><span class="sxs-lookup"><span data-stu-id="9535d-133">Specifies metadata for the created directory or file.</span></span>

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

### <span data-ttu-id="9535d-134">-Path</span><span class="sxs-lookup"><span data-stu-id="9535d-134">-Path</span></span>
<span data-ttu-id="9535d-135">Percorso nel file system specificato che deve essere creato.</span><span class="sxs-lookup"><span data-stu-id="9535d-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="9535d-136">Può essere un file o una directory nel formato 'directory/file.txt' o 'directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="9535d-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="9535d-137">-Permission</span><span class="sxs-lookup"><span data-stu-id="9535d-137">-Permission</span></span>
<span data-ttu-id="9535d-138">Imposta le autorizzazioni di accesso POSIX per il proprietario del file, il gruppo proprietario del file e altri utenti.</span><span class="sxs-lookup"><span data-stu-id="9535d-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="9535d-139">A ogni classe può essere concessa l'autorizzazione di lettura, scrittura o esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9535d-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="9535d-140">Symbolic (rwxrw-rw-) è supportato.</span><span class="sxs-lookup"><span data-stu-id="9535d-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="9535d-141">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="9535d-141">-Property</span></span>
<span data-ttu-id="9535d-142">Specifica le proprietà per la directory o il file creato.</span><span class="sxs-lookup"><span data-stu-id="9535d-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="9535d-143">Le proprietà supportate per il file sono: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="9535d-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="9535d-144">Le proprietà supportate per la directory sono: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="9535d-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="9535d-145">-Source</span><span class="sxs-lookup"><span data-stu-id="9535d-145">-Source</span></span>
<span data-ttu-id="9535d-146">Specificare il percorso del file di origine locale che verrà caricato in un file GEN2 della finestra dei dati.</span><span class="sxs-lookup"><span data-stu-id="9535d-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

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

### <span data-ttu-id="9535d-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="9535d-147">-Umask</span></span>
<span data-ttu-id="9535d-148">Quando si crea un nuovo elemento e la directory padre non ha un ACL predefinito, la umask limita le autorizzazioni per la creazione del file o della directory.</span><span class="sxs-lookup"><span data-stu-id="9535d-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="9535d-149">L'autorizzazione risultante viene concessa da p & ^u, dove p è l'autorizzazione e l'utente è il umask.</span><span class="sxs-lookup"><span data-stu-id="9535d-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="9535d-150">Symbolic (rwxrw-rw-) è supportato.</span><span class="sxs-lookup"><span data-stu-id="9535d-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="9535d-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9535d-151">-Confirm</span></span>
<span data-ttu-id="9535d-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9535d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9535d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9535d-153">-WhatIf</span></span>
<span data-ttu-id="9535d-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9535d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9535d-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9535d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9535d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9535d-156">CommonParameters</span></span>
<span data-ttu-id="9535d-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9535d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9535d-158">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9535d-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9535d-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="9535d-159">INPUTS</span></span>

### <span data-ttu-id="9535d-160">System.String</span><span class="sxs-lookup"><span data-stu-id="9535d-160">System.String</span></span>

### <span data-ttu-id="9535d-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9535d-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9535d-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9535d-162">OUTPUTS</span></span>

### <span data-ttu-id="9535d-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="9535d-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="9535d-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="9535d-164">NOTES</span></span>

## <span data-ttu-id="9535d-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9535d-165">RELATED LINKS</span></span>
