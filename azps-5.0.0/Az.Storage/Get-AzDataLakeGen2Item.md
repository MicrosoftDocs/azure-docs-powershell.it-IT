---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: edd65cc10ca90592225b6b9deb04167202510a2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202820"
---
# <span data-ttu-id="965fa-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="965fa-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="965fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="965fa-102">SYNOPSIS</span></span>
<span data-ttu-id="965fa-103">Ottiene i dettagli di un file o di una directory in un filesystem.</span><span class="sxs-lookup"><span data-stu-id="965fa-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="965fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="965fa-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="965fa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="965fa-105">DESCRIPTION</span></span>
<span data-ttu-id="965fa-106">Il cmdlet **Get-AzDataLakeGen2Item** ottiene i dettagli di un file o di una directory in un filesystem in un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="965fa-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="965fa-107">Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="965fa-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="965fa-108">Questo tipo di account può essere creato eseguendo il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="965fa-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="965fa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="965fa-109">EXAMPLES</span></span>

### <span data-ttu-id="965fa-110">Esempio 1: ottenere una directory da un filesystem e visualizzare i dettagli</span><span class="sxs-lookup"><span data-stu-id="965fa-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/"
PS C:\> $dir1

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser     
 
PS C:\WINDOWS\system32> $dir1.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      ---        
False        Other                      rwx      

PS C:\WINDOWS\system32> $dir1.Permissions

Owner        : Execute, Write, Read
Group        : None
Other        : Execute, Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\WINDOWS\system32> $dir1.Properties.Metadata

Key          Value 
---          ----- 
hdi_isfolder true  
tag1         value1
tag2         value2

PS C:\WINDOWS\system32> $dir1.Properties

LastModified          : 3/23/2020 9:15:56 AM +00:00
CreatedOn             : 3/23/2020 9:15:56 AM +00:00
Metadata              : {[hdi_isfolder, true], [tag1, value1], [tag2, value2]}
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
ContentLength         : 0
ContentType           : application/octet-stream
ETag                  : "0x8D7CF0ACBA35FA8"
ContentHash           : 
ContentEncoding       : UDF12
ContentDisposition    : 
ContentLanguage       : 
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="965fa-111">Questo comando consente di ottenere una directory da un filesystem e visualizzare i dettagli.</span><span class="sxs-lookup"><span data-stu-id="965fa-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="965fa-112">Esempio 2: ottenere un file da un filesystem</span><span class="sxs-lookup"><span data-stu-id="965fa-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="965fa-113">Questo comando consente di ottenere i dettagli di un file da un filesystem.</span><span class="sxs-lookup"><span data-stu-id="965fa-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="965fa-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="965fa-114">PARAMETERS</span></span>

### <span data-ttu-id="965fa-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="965fa-115">-Context</span></span>
<span data-ttu-id="965fa-116">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="965fa-116">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="965fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="965fa-117">-DefaultProfile</span></span>
<span data-ttu-id="965fa-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="965fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="965fa-119">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="965fa-119">-FileSystem</span></span>
<span data-ttu-id="965fa-120">Nome FileSystem</span><span class="sxs-lookup"><span data-stu-id="965fa-120">FileSystem name</span></span>

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

### <span data-ttu-id="965fa-121">-Path</span><span class="sxs-lookup"><span data-stu-id="965fa-121">-Path</span></span>
<span data-ttu-id="965fa-122">Il percorso nel filesystem specificato che deve essere recuperato.</span><span class="sxs-lookup"><span data-stu-id="965fa-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="965fa-123">Può essere un file o una directory nel formato ' directory/file.txt' o ' directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="965fa-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="965fa-124">Non specificare questo parametro per ottenere la directory radice del filesystem.</span><span class="sxs-lookup"><span data-stu-id="965fa-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="965fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="965fa-125">CommonParameters</span></span>
<span data-ttu-id="965fa-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="965fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="965fa-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="965fa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="965fa-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="965fa-128">INPUTS</span></span>

### <span data-ttu-id="965fa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="965fa-129">System.String</span></span>

### <span data-ttu-id="965fa-130">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="965fa-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="965fa-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="965fa-131">OUTPUTS</span></span>

### <span data-ttu-id="965fa-132">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="965fa-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="965fa-133">Note</span><span class="sxs-lookup"><span data-stu-id="965fa-133">NOTES</span></span>

## <span data-ttu-id="965fa-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="965fa-134">RELATED LINKS</span></span>
