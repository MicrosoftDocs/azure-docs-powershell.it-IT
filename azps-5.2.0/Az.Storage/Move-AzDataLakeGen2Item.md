---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324906"
---
# <span data-ttu-id="553c0-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="553c0-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="553c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="553c0-102">SYNOPSIS</span></span>
<span data-ttu-id="553c0-103">Trasferire un file o una directory in un altro file o directory nello stesso account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="553c0-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="553c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="553c0-104">SYNTAX</span></span>

### <span data-ttu-id="553c0-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="553c0-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="553c0-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="553c0-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="553c0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="553c0-107">DESCRIPTION</span></span>
<span data-ttu-id="553c0-108">Il cmdlet **Move-AzDataLakeGen2Item** sposta un file o una directory in un altro file o directory nello stesso account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="553c0-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="553c0-109">Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="553c0-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="553c0-110">Questo tipo di account può essere creato eseguendo il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="553c0-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="553c0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="553c0-111">EXAMPLES</span></span>

### <span data-ttu-id="553c0-112">Esempio 1: posizionare una piega nello stesso filesystem</span><span class="sxs-lookup"><span data-stu-id="553c0-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="553c0-113">Questo comando consente di trasferire la directory "dir1" nella directory "dir3" nello stesso filesystem.</span><span class="sxs-lookup"><span data-stu-id="553c0-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="553c0-114">Esempio 2: trasferire un file per pipeline, in un altro filesystem nello stesso account di archiviazione senza richiesta</span><span class="sxs-lookup"><span data-stu-id="553c0-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="553c0-115">Questo comando consente di trasferire il file "dir1/file1" in "filesystem1" nel file "dir2/file2" in "filesystem2" nello stesso account di archiviazione senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="553c0-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="553c0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="553c0-116">PARAMETERS</span></span>

### <span data-ttu-id="553c0-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="553c0-117">-Context</span></span>
<span data-ttu-id="553c0-118">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="553c0-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="553c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553c0-119">-DefaultProfile</span></span>
<span data-ttu-id="553c0-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="553c0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="553c0-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="553c0-121">-DestFileSystem</span></span>
<span data-ttu-id="553c0-122">Nome del FileSystem dest</span><span class="sxs-lookup"><span data-stu-id="553c0-122">Dest FileSystem name</span></span>

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

### <span data-ttu-id="553c0-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="553c0-123">-DestPath</span></span>
<span data-ttu-id="553c0-124">Percorso BLOB di destinazione</span><span class="sxs-lookup"><span data-stu-id="553c0-124">Dest Blob path</span></span>

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

### <span data-ttu-id="553c0-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="553c0-125">-FileSystem</span></span>
<span data-ttu-id="553c0-126">Nome FileSystem</span><span class="sxs-lookup"><span data-stu-id="553c0-126">FileSystem name</span></span>

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

### <span data-ttu-id="553c0-127">-Force</span><span class="sxs-lookup"><span data-stu-id="553c0-127">-Force</span></span>
<span data-ttu-id="553c0-128">Forza a sovrascrivere la destinazione.</span><span class="sxs-lookup"><span data-stu-id="553c0-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="553c0-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="553c0-129">-InputObject</span></span>
<span data-ttu-id="553c0-130">Oggetto Item di Azure datalake Gen2 da cui partire.</span><span class="sxs-lookup"><span data-stu-id="553c0-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="553c0-131">-Path</span><span class="sxs-lookup"><span data-stu-id="553c0-131">-Path</span></span>
<span data-ttu-id="553c0-132">Il percorso nel filesystem specificato da cui deve essere spostato.</span><span class="sxs-lookup"><span data-stu-id="553c0-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="553c0-133">Può essere un file o una directory nel formato ' directory/file.txt' o ' directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="553c0-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="553c0-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="553c0-134">-Confirm</span></span>
<span data-ttu-id="553c0-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="553c0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="553c0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="553c0-136">-WhatIf</span></span>
<span data-ttu-id="553c0-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="553c0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="553c0-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="553c0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="553c0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553c0-139">CommonParameters</span></span>
<span data-ttu-id="553c0-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="553c0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553c0-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="553c0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553c0-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="553c0-142">INPUTS</span></span>

### <span data-ttu-id="553c0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="553c0-143">System.String</span></span>

### <span data-ttu-id="553c0-144">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="553c0-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="553c0-145">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="553c0-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="553c0-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="553c0-146">OUTPUTS</span></span>

### <span data-ttu-id="553c0-147">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="553c0-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="553c0-148">Note</span><span class="sxs-lookup"><span data-stu-id="553c0-148">NOTES</span></span>

## <span data-ttu-id="553c0-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="553c0-149">RELATED LINKS</span></span>
