---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: 4a88fe1e4bc18aaa31222b2f5d8e2a90629984d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972094"
---
# <span data-ttu-id="f569e-101">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="f569e-101">Save-AzVhd</span></span>

## <span data-ttu-id="f569e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f569e-102">SYNOPSIS</span></span>
<span data-ttu-id="f569e-103">Salva le immagini VHD scaricate localmente.</span><span class="sxs-lookup"><span data-stu-id="f569e-103">Saves downloaded .vhd images locally.</span></span>

## <span data-ttu-id="f569e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f569e-104">SYNTAX</span></span>

### <span data-ttu-id="f569e-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f569e-105">ResourceGroupParameterSetName</span></span>
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f569e-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f569e-106">StorageKeyParameterSetName</span></span>
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>]
 [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f569e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f569e-107">DESCRIPTION</span></span>
<span data-ttu-id="f569e-108">Il cmdlet **Save-AzVhd** salva le immagini vhd da un BLOB in cui sono archiviate in un file.</span><span class="sxs-lookup"><span data-stu-id="f569e-108">The **Save-AzVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="f569e-109">È possibile specificare il numero di thread del downloader utilizzati dal processo e se sostituire un file già esistente.</span><span class="sxs-lookup"><span data-stu-id="f569e-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>
<span data-ttu-id="f569e-110">Questo cmdlet scarica i contenuti così come sono.</span><span class="sxs-lookup"><span data-stu-id="f569e-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="f569e-111">Non si applica alcuna conversione del formato del disco rigido virtuale (VHD).</span><span class="sxs-lookup"><span data-stu-id="f569e-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="f569e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f569e-112">EXAMPLES</span></span>

### <span data-ttu-id="f569e-113">Esempio 1: Scaricare un'immagine</span><span class="sxs-lookup"><span data-stu-id="f569e-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="f569e-114">Questo comando scarica un file VHD e lo archivia nel percorso locale C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="f569e-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="f569e-115">Esempio 2: Scaricare un'immagine e sovrascrivere il file locale</span><span class="sxs-lookup"><span data-stu-id="f569e-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="f569e-116">Questo comando scarica un file VHD e lo archivia nel percorso locale.</span><span class="sxs-lookup"><span data-stu-id="f569e-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="f569e-117">Il comando include il *parametro Overwrite.*</span><span class="sxs-lookup"><span data-stu-id="f569e-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="f569e-118">Pertanto, se C:\vhd\Win7Image.vhd esiste già, questo comando la sostituisce.</span><span class="sxs-lookup"><span data-stu-id="f569e-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="f569e-119">Esempio 3: Scaricare un'immagine usando un numero specificato di thread</span><span class="sxs-lookup"><span data-stu-id="f569e-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="f569e-120">Questo comando scarica un file VHD e lo archivia nel percorso locale.</span><span class="sxs-lookup"><span data-stu-id="f569e-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="f569e-121">Il comando specifica il valore 32 per il *parametro NumberOfThreads.*</span><span class="sxs-lookup"><span data-stu-id="f569e-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="f569e-122">Di conseguenza, il cmdlet usa 32 thread per questa azione.</span><span class="sxs-lookup"><span data-stu-id="f569e-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="f569e-123">Esempio 4: Scaricare un'immagine e specificare la chiave di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f569e-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="f569e-124">Questo comando scarica un file VHD e specifica la chiave di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f569e-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="f569e-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f569e-125">PARAMETERS</span></span>

### <span data-ttu-id="f569e-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f569e-126">-AsJob</span></span>
<span data-ttu-id="f569e-127">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="f569e-127">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f569e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f569e-128">-DefaultProfile</span></span>
<span data-ttu-id="f569e-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f569e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f569e-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="f569e-130">-LocalFilePath</span></span>
<span data-ttu-id="f569e-131">Specifica il percorso locale dell'immagine salvata.</span><span class="sxs-lookup"><span data-stu-id="f569e-131">Specifies the local file path of the saved image.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f569e-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="f569e-132">-NumberOfThreads</span></span>
<span data-ttu-id="f569e-133">Specifica il numero di thread di download che questo cmdlet usa durante il download.</span><span class="sxs-lookup"><span data-stu-id="f569e-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f569e-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="f569e-134">-OverWrite</span></span>
<span data-ttu-id="f569e-135">Indica che questo cmdlet sostituisce il file specificato dal file *LocalFilePath,* se presente.</span><span class="sxs-lookup"><span data-stu-id="f569e-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f569e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f569e-136">-ResourceGroupName</span></span>
<span data-ttu-id="f569e-137">Specifica il nome del gruppo di risorse dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f569e-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f569e-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="f569e-138">-SourceUri</span></span>
<span data-ttu-id="f569e-139">Specifica l'URI (Uniform Resource Identifier) del BLOB in `Azure` .</span><span class="sxs-lookup"><span data-stu-id="f569e-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f569e-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="f569e-140">-StorageKey</span></span>
<span data-ttu-id="f569e-141">Specifica la chiave di archiviazione dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="f569e-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="f569e-142">Se non si specifica una chiave, questo cmdlet prova a determinare la chiave di archiviazione dell'account in *SourceUri* da Azure.</span><span class="sxs-lookup"><span data-stu-id="f569e-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f569e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f569e-143">CommonParameters</span></span>
<span data-ttu-id="f569e-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f569e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f569e-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f569e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f569e-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="f569e-146">INPUTS</span></span>

### <span data-ttu-id="f569e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f569e-147">System.String</span></span>

### <span data-ttu-id="f569e-148">System.Uri</span><span class="sxs-lookup"><span data-stu-id="f569e-148">System.Uri</span></span>

## <span data-ttu-id="f569e-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f569e-149">OUTPUTS</span></span>

### <span data-ttu-id="f569e-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="f569e-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="f569e-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="f569e-151">NOTES</span></span>

## <span data-ttu-id="f569e-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f569e-152">RELATED LINKS</span></span>

[<span data-ttu-id="f569e-153">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="f569e-153">Add-AzVhd</span></span>](./Add-AzVhd.md)


