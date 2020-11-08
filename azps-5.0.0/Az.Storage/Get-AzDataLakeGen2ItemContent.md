---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202819"
---
# <span data-ttu-id="434f0-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="434f0-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="434f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="434f0-102">SYNOPSIS</span></span>
<span data-ttu-id="434f0-103">Scaricare un file.</span><span class="sxs-lookup"><span data-stu-id="434f0-103">Download a file.</span></span>

## <span data-ttu-id="434f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="434f0-104">SYNTAX</span></span>

### <span data-ttu-id="434f0-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="434f0-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="434f0-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="434f0-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="434f0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="434f0-107">DESCRIPTION</span></span>
<span data-ttu-id="434f0-108">Il cmdlet **Get-AzDataLakeGen2ItemContent** Scarica un file in un filesystem in un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="434f0-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="434f0-109">Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="434f0-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="434f0-110">Questo tipo di account può essere creato eseguendo il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="434f0-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="434f0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="434f0-111">EXAMPLES</span></span>

### <span data-ttu-id="434f0-112">Esempio 1: scaricare un file senza richiesta</span><span class="sxs-lookup"><span data-stu-id="434f0-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="434f0-113">Questo comando consente di scaricare un file in un file locale senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="434f0-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="434f0-114">Esempio 2: ottenere un file, quindi pipeline per scaricare il file in un file locale</span><span class="sxs-lookup"><span data-stu-id="434f0-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="434f0-115">Questo comando ottiene prima di tutto un file, quindi pipeline per scaricare il file in un file locale.</span><span class="sxs-lookup"><span data-stu-id="434f0-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="434f0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="434f0-116">PARAMETERS</span></span>

### <span data-ttu-id="434f0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="434f0-117">-AsJob</span></span>
<span data-ttu-id="434f0-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="434f0-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="434f0-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="434f0-119">-CheckMd5</span></span>
<span data-ttu-id="434f0-120">controllare la somma MD5</span><span class="sxs-lookup"><span data-stu-id="434f0-120">check the md5sum</span></span>

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

### <span data-ttu-id="434f0-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="434f0-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="434f0-122">La quantità totale di attività asincrone simultanee.</span><span class="sxs-lookup"><span data-stu-id="434f0-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="434f0-123">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="434f0-123">The default value is 10.</span></span>

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

### <span data-ttu-id="434f0-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="434f0-124">-Context</span></span>
<span data-ttu-id="434f0-125">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="434f0-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="434f0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434f0-126">-DefaultProfile</span></span>
<span data-ttu-id="434f0-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="434f0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="434f0-128">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="434f0-128">-Destination</span></span>
<span data-ttu-id="434f0-129">Percorso file locale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="434f0-129">Destination local file path.</span></span>

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

### <span data-ttu-id="434f0-130">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="434f0-130">-FileSystem</span></span>
<span data-ttu-id="434f0-131">Nome FileSystem</span><span class="sxs-lookup"><span data-stu-id="434f0-131">FileSystem name</span></span>

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

### <span data-ttu-id="434f0-132">-Force</span><span class="sxs-lookup"><span data-stu-id="434f0-132">-Force</span></span>
<span data-ttu-id="434f0-133">Forza per sovrascrivere il BLOB o il file esistente</span><span class="sxs-lookup"><span data-stu-id="434f0-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="434f0-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="434f0-134">-InputObject</span></span>
<span data-ttu-id="434f0-135">Oggetto elemento Gen2 di Azure datalake da scaricare.</span><span class="sxs-lookup"><span data-stu-id="434f0-135">Azure Datalake Gen2 Item Object to download.</span></span>

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

### <span data-ttu-id="434f0-136">-Path</span><span class="sxs-lookup"><span data-stu-id="434f0-136">-Path</span></span>
<span data-ttu-id="434f0-137">Il percorso nel filesystem specificato che deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="434f0-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="434f0-138">Può essere un file o una directory nel formato ' directory/file.txt' o ' directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="434f0-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="434f0-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="434f0-139">-Confirm</span></span>
<span data-ttu-id="434f0-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="434f0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="434f0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="434f0-141">-WhatIf</span></span>
<span data-ttu-id="434f0-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="434f0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="434f0-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="434f0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="434f0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434f0-144">CommonParameters</span></span>
<span data-ttu-id="434f0-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="434f0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434f0-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="434f0-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434f0-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="434f0-147">INPUTS</span></span>

### <span data-ttu-id="434f0-148">System. String</span><span class="sxs-lookup"><span data-stu-id="434f0-148">System.String</span></span>

### <span data-ttu-id="434f0-149">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="434f0-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="434f0-150">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="434f0-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="434f0-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="434f0-151">OUTPUTS</span></span>

### <span data-ttu-id="434f0-152">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="434f0-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="434f0-153">Note</span><span class="sxs-lookup"><span data-stu-id="434f0-153">NOTES</span></span>

## <span data-ttu-id="434f0-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="434f0-154">RELATED LINKS</span></span>
