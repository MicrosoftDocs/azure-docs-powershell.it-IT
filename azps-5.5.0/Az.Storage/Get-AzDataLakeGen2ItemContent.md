---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178270"
---
# <span data-ttu-id="8cf35-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="8cf35-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="8cf35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cf35-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf35-103">Scaricare un file.</span><span class="sxs-lookup"><span data-stu-id="8cf35-103">Download a file.</span></span>

## <span data-ttu-id="8cf35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cf35-104">SYNTAX</span></span>

### <span data-ttu-id="8cf35-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8cf35-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf35-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="8cf35-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cf35-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8cf35-107">DESCRIPTION</span></span>
<span data-ttu-id="8cf35-108">Il cmdlet **Get-AzDataLakeGen2ItemContent** scarica un file in un Filesystem in un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cf35-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="8cf35-109">Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8cf35-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="8cf35-110">Questo tipo di account può essere creato eseguire il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalZone $true".</span><span class="sxs-lookup"><span data-stu-id="8cf35-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="8cf35-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cf35-111">EXAMPLES</span></span>

### <span data-ttu-id="8cf35-112">Esempio 1: Scaricare un file senza richiesta</span><span class="sxs-lookup"><span data-stu-id="8cf35-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="8cf35-113">Questo comando scarica un file in un file locale senza richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="8cf35-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="8cf35-114">Esempio 2: Ottenere un file, quindi pipeline per scaricare il file in un file locale</span><span class="sxs-lookup"><span data-stu-id="8cf35-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="8cf35-115">Questo comando recupera prima un file, quindi lo pipeline per scaricarlo in un file locale.</span><span class="sxs-lookup"><span data-stu-id="8cf35-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="8cf35-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cf35-116">PARAMETERS</span></span>

### <span data-ttu-id="8cf35-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cf35-117">-AsJob</span></span>
<span data-ttu-id="8cf35-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8cf35-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cf35-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="8cf35-119">-CheckMd5</span></span>
<span data-ttu-id="8cf35-120">controllare il valore md5sum</span><span class="sxs-lookup"><span data-stu-id="8cf35-120">check the md5sum</span></span>

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

### <span data-ttu-id="8cf35-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8cf35-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8cf35-122">La quantità totale di attività sincronizzate simultanee.</span><span class="sxs-lookup"><span data-stu-id="8cf35-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="8cf35-123">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="8cf35-123">The default value is 10.</span></span>

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

### <span data-ttu-id="8cf35-124">-Context</span><span class="sxs-lookup"><span data-stu-id="8cf35-124">-Context</span></span>
<span data-ttu-id="8cf35-125">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="8cf35-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="8cf35-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf35-126">-DefaultProfile</span></span>
<span data-ttu-id="8cf35-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cf35-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cf35-128">-Destination</span><span class="sxs-lookup"><span data-stu-id="8cf35-128">-Destination</span></span>
<span data-ttu-id="8cf35-129">Percorso file locale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8cf35-129">Destination local file path.</span></span>

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

### <span data-ttu-id="8cf35-130">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="8cf35-130">-FileSystem</span></span>
<span data-ttu-id="8cf35-131">Nome filesystem</span><span class="sxs-lookup"><span data-stu-id="8cf35-131">FileSystem name</span></span>

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

### <span data-ttu-id="8cf35-132">-Force</span><span class="sxs-lookup"><span data-stu-id="8cf35-132">-Force</span></span>
<span data-ttu-id="8cf35-133">Forzare la sovrascrittura del BLOB o del file esistente</span><span class="sxs-lookup"><span data-stu-id="8cf35-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="8cf35-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cf35-134">-InputObject</span></span>
<span data-ttu-id="8cf35-135">Oggetto Elemento Gen2 di Azure Datalake da scaricare.</span><span class="sxs-lookup"><span data-stu-id="8cf35-135">Azure Datalake Gen2 Item Object to download.</span></span>

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

### <span data-ttu-id="8cf35-136">-Path</span><span class="sxs-lookup"><span data-stu-id="8cf35-136">-Path</span></span>
<span data-ttu-id="8cf35-137">Percorso nel file system specificato che deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="8cf35-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="8cf35-138">Può essere un file o una directory nel formato 'directory/file.txt' o 'directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="8cf35-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="8cf35-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cf35-139">-Confirm</span></span>
<span data-ttu-id="8cf35-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf35-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf35-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf35-141">-WhatIf</span></span>
<span data-ttu-id="8cf35-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cf35-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf35-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cf35-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf35-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf35-144">CommonParameters</span></span>
<span data-ttu-id="8cf35-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf35-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf35-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf35-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf35-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="8cf35-147">INPUTS</span></span>

### <span data-ttu-id="8cf35-148">System.String</span><span class="sxs-lookup"><span data-stu-id="8cf35-148">System.String</span></span>

### <span data-ttu-id="8cf35-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="8cf35-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="8cf35-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8cf35-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8cf35-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cf35-151">OUTPUTS</span></span>

### <span data-ttu-id="8cf35-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="8cf35-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="8cf35-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="8cf35-153">NOTES</span></span>

## <span data-ttu-id="8cf35-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cf35-154">RELATED LINKS</span></span>
