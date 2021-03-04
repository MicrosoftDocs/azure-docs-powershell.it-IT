---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: fdcac32a925cad97c256af2db949a08268e0ac3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959326"
---
# <span data-ttu-id="ac1ce-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="ac1ce-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="ac1ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac1ce-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1ce-103">Aggiornare un file o una directory in base a proprietà, metadati, autorizzazioni, ACL e proprietario.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="ac1ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac1ce-104">SYNTAX</span></span>

### <span data-ttu-id="ac1ce-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac1ce-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac1ce-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="ac1ce-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac1ce-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ac1ce-107">DESCRIPTION</span></span>
<span data-ttu-id="ac1ce-108">Il cmdlet **Update-AzDataLakeGen2Item** aggiorna un file o una directory in base a proprietà, metadati, autorizzazioni, ACL e proprietario.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="ac1ce-109">Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="ac1ce-110">Questo tipo di account può essere creato eseguire il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalZone $true".</span><span class="sxs-lookup"><span data-stu-id="ac1ce-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="ac1ce-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac1ce-111">EXAMPLES</span></span>

### <span data-ttu-id="ac1ce-112">Esempio 1: Creare un oggetto ACL con una voce ACL 3 e aggiornare l'ACL a tutti gli elementi in un filesystem in modo ricorsivo</span><span class="sxs-lookup"><span data-stu-id="ac1ce-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Recurse | Update-AzDataLakeGen2Item -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser           
dir1/file1           False        1024            2020-03-23 09:29:18Z rwxrw-rw-    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="ac1ce-113">Questo comando crea prima di tutto un oggetto ACL con voce di acl 3 (parametro -InputObject per aggiungere una voce acl all'oggetto acl esistente), quindi recupera tutti gli elementi in un filesystem e aggiorna l'acl sugli elementi.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="ac1ce-114">Esempio 2: Aggiornare tutte le proprietà di un file e mostrarle</span><span class="sxs-lookup"><span data-stu-id="ac1ce-114">Example 2: Update all properties on a file, and show them</span></span>
```
PS C:\> $file = Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" `
                 -Acl $acl `
                 -Property @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="; "ContentEncoding" = "UDF8"; "CacheControl" = "READ"; "ContentDisposition" = "True"; "ContentLanguage" = "EN-US"} `
                 -Metadata  @{"tag1" = "value1"; "tag2" = "value2" } `
                 -Permission rw-rw-rwx `
                 -Owner '$superuser' `
                 -Group '$superuser'

PS C:\> $file

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser          

PS C:\> $file.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      rw-        
False        Other                      rw-        

PS C:\> $file.Permissions

Owner        : Execute, Write, Read
Group        : Write, Read
Other        : Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\> $file.Properties.Metadata

Key  Value 
---  ----- 
tag2 value2
tag1 value1

PS C:\> $file.Properties


LastModified          : 3/23/2020 9:57:33 AM +00:00
CreatedOn             : 3/23/2020 9:29:18 AM +00:00
Metadata              : {[tag2, value2], [tag1, value1]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 1024
ContentType           : image/jpeg
ETag                  : "0x8D7CF109B9878CC"
ContentHash           : {139, 189, 187, 176...}
ContentEncoding       : UDF8
ContentDisposition    : True
ContentLanguage       : EN-US
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="ac1ce-115">Questo comando aggiorna tutte le proprietà di un file (ACL, autorizzazione, proprietario, gruppo, metadati, proprietà possono essere aggiornate con qualsiasi associazione) e le mostra nella console di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="ac1ce-116">Esempio 3: Aggiungere una voce ACL a una directory</span><span class="sxs-lookup"><span data-stu-id="ac1ce-116">Example 3: Add an ACL entry to a directory</span></span>
```
## Get the origin ACL
PS C:\> $acl = (Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/').ACL

# Update permission of a new ACL entry (if ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry)
PS C:\> $acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rw- -InputObject $acl  

# set the new acl to the directory
PS C:\> update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/' -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="ac1ce-117">Questo comando recupera l'ACL da una directory, aggiorna/aggiunge una voce ACL e lo imposta di nuovo nella directory.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="ac1ce-118">Se la voce ACL con lo stesso AccessControlType/EntityId/DefaultScope non esiste, aggiungerà una nuova voce ACL, altrimenti aggiornare l'autorizzazione della voce ACL esistente.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="ac1ce-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac1ce-119">PARAMETERS</span></span>

### <span data-ttu-id="ac1ce-120">-Acl</span><span class="sxs-lookup"><span data-stu-id="ac1ce-120">-Acl</span></span>
<span data-ttu-id="ac1ce-121">Imposta i diritti di controllo di accesso POSIX su file e directory.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="ac1ce-122">Creare questo oggetto con New-AzDataLakeGen2ItemAclObject.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac1ce-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ac1ce-123">-Context</span></span>
<span data-ttu-id="ac1ce-124">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="ac1ce-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="ac1ce-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1ce-125">-DefaultProfile</span></span>
<span data-ttu-id="ac1ce-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac1ce-127">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="ac1ce-127">-FileSystem</span></span>
<span data-ttu-id="ac1ce-128">Nome filesystem</span><span class="sxs-lookup"><span data-stu-id="ac1ce-128">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac1ce-129">-Group</span><span class="sxs-lookup"><span data-stu-id="ac1ce-129">-Group</span></span>
<span data-ttu-id="ac1ce-130">Imposta il gruppo proprietario del BLOB.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="ac1ce-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac1ce-131">-InputObject</span></span>
<span data-ttu-id="ac1ce-132">Oggetto Elemento Gen2 di Azure Datalake da aggiornare</span><span class="sxs-lookup"><span data-stu-id="ac1ce-132">Azure Datalake Gen2 Item Object to update</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac1ce-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ac1ce-133">-Metadata</span></span>
<span data-ttu-id="ac1ce-134">Specifica i metadati per la directory o il file.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="ac1ce-135">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="ac1ce-135">-Owner</span></span>
<span data-ttu-id="ac1ce-136">Imposta il proprietario del BLOB.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="ac1ce-137">-Path</span><span class="sxs-lookup"><span data-stu-id="ac1ce-137">-Path</span></span>
<span data-ttu-id="ac1ce-138">Percorso nel file system specificato che deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="ac1ce-139">Può essere un file o una directory nel formato 'directory/file.txt' o 'directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="ac1ce-140">Se non si specifica questo parametro, la directory radice del Filesystem verrà aggiornato.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac1ce-141">-Permission</span><span class="sxs-lookup"><span data-stu-id="ac1ce-141">-Permission</span></span>
<span data-ttu-id="ac1ce-142">Imposta le autorizzazioni di accesso POSIX per il proprietario del file, il gruppo proprietario del file e altri utenti.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="ac1ce-143">A ogni classe può essere concessa l'autorizzazione di lettura, scrittura o esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="ac1ce-144">Symbolic (rwxrw-rw-) è supportato.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="ac1ce-145">Non valido in combinazione con Acl.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="ac1ce-146">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="ac1ce-146">-Property</span></span>
<span data-ttu-id="ac1ce-147">Specifica le proprietà per la directory o il file.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="ac1ce-148">Le proprietà supportate per il file sono: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="ac1ce-149">Le proprietà supportate per la directory sono: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="ac1ce-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac1ce-150">-Confirm</span></span>
<span data-ttu-id="ac1ce-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac1ce-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac1ce-152">-WhatIf</span></span>
<span data-ttu-id="ac1ce-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac1ce-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac1ce-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1ce-155">CommonParameters</span></span>
<span data-ttu-id="ac1ce-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac1ce-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1ce-157">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac1ce-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1ce-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="ac1ce-158">INPUTS</span></span>

### <span data-ttu-id="ac1ce-159">System.String</span><span class="sxs-lookup"><span data-stu-id="ac1ce-159">System.String</span></span>

### <span data-ttu-id="ac1ce-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="ac1ce-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="ac1ce-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ac1ce-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ac1ce-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac1ce-162">OUTPUTS</span></span>

### <span data-ttu-id="ac1ce-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="ac1ce-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="ac1ce-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="ac1ce-164">NOTES</span></span>

## <span data-ttu-id="ac1ce-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac1ce-165">RELATED LINKS</span></span>
