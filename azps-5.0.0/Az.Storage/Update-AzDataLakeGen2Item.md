---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200078"
---
# <span data-ttu-id="a4454-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a4454-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="a4454-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4454-102">SYNOPSIS</span></span>
<span data-ttu-id="a4454-103">Aggiornare un file o una directory su proprietà, metadati, autorizzazioni, ACL e proprietario.</span><span class="sxs-lookup"><span data-stu-id="a4454-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="a4454-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4454-104">SYNTAX</span></span>

### <span data-ttu-id="a4454-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4454-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4454-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="a4454-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4454-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4454-107">DESCRIPTION</span></span>
<span data-ttu-id="a4454-108">Il cmdlet **Update-AzDataLakeGen2Item** aggiorna un file o una directory su proprietà, metadati, autorizzazioni, ACL e proprietario.</span><span class="sxs-lookup"><span data-stu-id="a4454-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="a4454-109">Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a4454-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="a4454-110">Questo tipo di account può essere creato eseguendo il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="a4454-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="a4454-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4454-111">EXAMPLES</span></span>

### <span data-ttu-id="a4454-112">Esempio 1: creare un oggetto ACL con 3 voci ACL e aggiornare l'ACL a tutti gli elementi in un filesystem in modo ricorsivo</span><span class="sxs-lookup"><span data-stu-id="a4454-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
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

<span data-ttu-id="a4454-113">Questo comando crea prima di tutto un oggetto ACL con 3 voci ACL (parametro Use-InputObject per aggiungere la voce ACL all'oggetto ACL esistente), quindi Ottieni tutti gli elementi in un filesystem e aggiorna ACL sugli elementi.</span><span class="sxs-lookup"><span data-stu-id="a4454-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="a4454-114">Esempio 2: aggiornare tutte le proprietà di un file e visualizzarle</span><span class="sxs-lookup"><span data-stu-id="a4454-114">Example 2: Update all properties on a file, and show them</span></span>
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

<span data-ttu-id="a4454-115">Questo comando Aggiorna tutte le proprietà di un file (ACL, permission, Owner, Group, Metadata, Property può essere aggiornato con qualsiasi conbination) e visualizzarlo nella console di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a4454-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="a4454-116">Esempio 3: aggiungere una voce ACL a una directory</span><span class="sxs-lookup"><span data-stu-id="a4454-116">Example 3: Add an ACL entry to a directory</span></span>
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

<span data-ttu-id="a4454-117">Questo comando consente di ottenere ACL da una directory, di aggiornare/aggiungere una voce ACL e di ritornare alla directory.</span><span class="sxs-lookup"><span data-stu-id="a4454-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="a4454-118">Se l'immissione ACL con lo stesso AccessControlType/EntityId/DefaultScope non esiste, aggiungerà una nuova voce ACL, else l'autorizzazione di aggiornamento della voce ACL esistente.</span><span class="sxs-lookup"><span data-stu-id="a4454-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="a4454-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4454-119">PARAMETERS</span></span>

### <span data-ttu-id="a4454-120">-ACL</span><span class="sxs-lookup"><span data-stu-id="a4454-120">-Acl</span></span>
<span data-ttu-id="a4454-121">Imposta i diritti di controllo di accesso POSIX su file e directory.</span><span class="sxs-lookup"><span data-stu-id="a4454-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="a4454-122">Crea questo oggetto con New-AzDataLakeGen2ItemAclObject.</span><span class="sxs-lookup"><span data-stu-id="a4454-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

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

### <span data-ttu-id="a4454-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="a4454-123">-Context</span></span>
<span data-ttu-id="a4454-124">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="a4454-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="a4454-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4454-125">-DefaultProfile</span></span>
<span data-ttu-id="a4454-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4454-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4454-127">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="a4454-127">-FileSystem</span></span>
<span data-ttu-id="a4454-128">Nome FileSystem</span><span class="sxs-lookup"><span data-stu-id="a4454-128">FileSystem name</span></span>

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

### <span data-ttu-id="a4454-129">-Gruppo</span><span class="sxs-lookup"><span data-stu-id="a4454-129">-Group</span></span>
<span data-ttu-id="a4454-130">Imposta il gruppo proprietario del BLOB.</span><span class="sxs-lookup"><span data-stu-id="a4454-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="a4454-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4454-131">-InputObject</span></span>
<span data-ttu-id="a4454-132">Oggetto elemento Gen2 di Azure datalake da aggiornare</span><span class="sxs-lookup"><span data-stu-id="a4454-132">Azure Datalake Gen2 Item Object to update</span></span>

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

### <span data-ttu-id="a4454-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a4454-133">-Metadata</span></span>
<span data-ttu-id="a4454-134">Specifica i metadati per la directory o il file.</span><span class="sxs-lookup"><span data-stu-id="a4454-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="a4454-135">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="a4454-135">-Owner</span></span>
<span data-ttu-id="a4454-136">Imposta il proprietario del BLOB.</span><span class="sxs-lookup"><span data-stu-id="a4454-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="a4454-137">-Path</span><span class="sxs-lookup"><span data-stu-id="a4454-137">-Path</span></span>
<span data-ttu-id="a4454-138">Il percorso nel filesystem specificato che deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a4454-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="a4454-139">Può essere un file o una directory nel formato ' directory/file.txt' o ' directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="a4454-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="a4454-140">Se non specifichi questo parametro verrà aggiornata la directory radice del filesystem.</span><span class="sxs-lookup"><span data-stu-id="a4454-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="a4454-141">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="a4454-141">-Permission</span></span>
<span data-ttu-id="a4454-142">Imposta le autorizzazioni di accesso POSIX per il proprietario del file, il gruppo proprietario file e altri.</span><span class="sxs-lookup"><span data-stu-id="a4454-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="a4454-143">A ogni classe può essere concessa l'autorizzazione di lettura, scrittura o esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a4454-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="a4454-144">Il simbolo (rwxrw-RW-) è supportato.</span><span class="sxs-lookup"><span data-stu-id="a4454-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="a4454-145">Non valido in combinazione con ACL.</span><span class="sxs-lookup"><span data-stu-id="a4454-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="a4454-146">-Property</span><span class="sxs-lookup"><span data-stu-id="a4454-146">-Property</span></span>
<span data-ttu-id="a4454-147">Specifica le proprietà per la directory o il file.</span><span class="sxs-lookup"><span data-stu-id="a4454-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="a4454-148">Le proprietà supportate per file sono: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="a4454-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="a4454-149">Le proprietà supportate per la directory sono: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="a4454-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="a4454-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4454-150">-Confirm</span></span>
<span data-ttu-id="a4454-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4454-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4454-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4454-152">-WhatIf</span></span>
<span data-ttu-id="a4454-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4454-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4454-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4454-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4454-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4454-155">CommonParameters</span></span>
<span data-ttu-id="a4454-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4454-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4454-157">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4454-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4454-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4454-158">INPUTS</span></span>

### <span data-ttu-id="a4454-159">System. String</span><span class="sxs-lookup"><span data-stu-id="a4454-159">System.String</span></span>

### <span data-ttu-id="a4454-160">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a4454-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="a4454-161">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a4454-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a4454-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4454-162">OUTPUTS</span></span>

### <span data-ttu-id="a4454-163">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a4454-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="a4454-164">Note</span><span class="sxs-lookup"><span data-stu-id="a4454-164">NOTES</span></span>

## <span data-ttu-id="a4454-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4454-165">RELATED LINKS</span></span>
