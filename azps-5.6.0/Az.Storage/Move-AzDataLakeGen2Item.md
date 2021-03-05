---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: 203e7a246c16345631da290645b356392c165bad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979182"
---
# <span data-ttu-id="d538c-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d538c-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="d538c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d538c-102">SYNOPSIS</span></span>
<span data-ttu-id="d538c-103">Spostare un file o una directory in un altro file o directory nello stesso account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d538c-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="d538c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d538c-104">SYNTAX</span></span>

### <span data-ttu-id="d538c-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d538c-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d538c-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="d538c-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d538c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d538c-107">DESCRIPTION</span></span>
<span data-ttu-id="d538c-108">Il cmdlet **Move-AzDataLakeGen2Item** sposta un file o una directory in un altro file o directory nello stesso account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d538c-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="d538c-109">Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d538c-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="d538c-110">Questo tipo di account può essere creato eseguire il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalZone $true".</span><span class="sxs-lookup"><span data-stu-id="d538c-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="d538c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d538c-111">EXAMPLES</span></span>

### <span data-ttu-id="d538c-112">Esempio 1: Spostare una piega nello stesso Filesystem</span><span class="sxs-lookup"><span data-stu-id="d538c-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="d538c-113">Questo comando sposta la directory 'dir1' nella directory 'dir3' nello stesso Filesystem.</span><span class="sxs-lookup"><span data-stu-id="d538c-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="d538c-114">Esempio 2: Spostare un file per pipeline in un altro filesystem nello stesso account di archiviazione senza richiesta</span><span class="sxs-lookup"><span data-stu-id="d538c-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="d538c-115">Questo comando sposta il file 'dir1/file1' in 'filesystem1' nel file 'dir2/file2' in 'filesystem2' nello stesso account di archiviazione senza richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="d538c-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="d538c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d538c-116">PARAMETERS</span></span>

### <span data-ttu-id="d538c-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d538c-117">-Context</span></span>
<span data-ttu-id="d538c-118">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="d538c-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="d538c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d538c-119">-DefaultProfile</span></span>
<span data-ttu-id="d538c-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d538c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d538c-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="d538c-121">-DestFileSystem</span></span>
<span data-ttu-id="d538c-122">Dest FileSystem name</span><span class="sxs-lookup"><span data-stu-id="d538c-122">Dest FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d538c-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="d538c-123">-DestPath</span></span>
<span data-ttu-id="d538c-124">Dest BLOB path</span><span class="sxs-lookup"><span data-stu-id="d538c-124">Dest Blob path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d538c-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="d538c-125">-FileSystem</span></span>
<span data-ttu-id="d538c-126">Nome filesystem</span><span class="sxs-lookup"><span data-stu-id="d538c-126">FileSystem name</span></span>

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

### <span data-ttu-id="d538c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="d538c-127">-Force</span></span>
<span data-ttu-id="d538c-128">Forzare la scrittura sulla destinazione.</span><span class="sxs-lookup"><span data-stu-id="d538c-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="d538c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d538c-129">-InputObject</span></span>
<span data-ttu-id="d538c-130">Oggetto Gen2 Item di Azure Datalake da cui spostarsi.</span><span class="sxs-lookup"><span data-stu-id="d538c-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="d538c-131">-Path</span><span class="sxs-lookup"><span data-stu-id="d538c-131">-Path</span></span>
<span data-ttu-id="d538c-132">Percorso nel file system specificato da cui eseguire lo spostamento.</span><span class="sxs-lookup"><span data-stu-id="d538c-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="d538c-133">Può essere un file o una directory nel formato 'directory/file.txt' o 'directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="d538c-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d538c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d538c-134">-Confirm</span></span>
<span data-ttu-id="d538c-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d538c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d538c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d538c-136">-WhatIf</span></span>
<span data-ttu-id="d538c-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d538c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d538c-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d538c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d538c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d538c-139">CommonParameters</span></span>
<span data-ttu-id="d538c-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d538c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d538c-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d538c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d538c-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="d538c-142">INPUTS</span></span>

### <span data-ttu-id="d538c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d538c-143">System.String</span></span>

### <span data-ttu-id="d538c-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d538c-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="d538c-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d538c-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d538c-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d538c-146">OUTPUTS</span></span>

### <span data-ttu-id="d538c-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d538c-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="d538c-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="d538c-148">NOTES</span></span>

## <span data-ttu-id="d538c-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d538c-149">RELATED LINKS</span></span>
