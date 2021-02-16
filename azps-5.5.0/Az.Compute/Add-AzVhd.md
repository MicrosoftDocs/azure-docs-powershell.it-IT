---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: d0031ad2a6b4c38937e7faaf0743d6181608ff15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199350"
---
# <span data-ttu-id="77445-101">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="77445-101">Add-AzVhd</span></span>

## <span data-ttu-id="77445-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77445-102">SYNOPSIS</span></span>
<span data-ttu-id="77445-103">Carica un disco rigido virtuale da una macchina virtuale locale in un BLOB in un account di archiviazione cloud in Azure.</span><span class="sxs-lookup"><span data-stu-id="77445-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="77445-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77445-104">SYNTAX</span></span>

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77445-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="77445-105">DESCRIPTION</span></span>
<span data-ttu-id="77445-106">Il cmdlet **Add-AzVhd** carica i dischi rigidi virtuali locali, nel formato di file VHD, in un account di archiviazione BLOB come dischi rigidi virtuali fissi.</span><span class="sxs-lookup"><span data-stu-id="77445-106">The **Add-AzVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="77445-107">È possibile configurare il numero di thread del caricatore che verranno usati o sovrascrivere un BLOB esistente nell'URI di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="77445-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="77445-108">È anche supportata la possibilità di caricare una versione con patch di un file VHD locale.</span><span class="sxs-lookup"><span data-stu-id="77445-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="77445-109">Quando è già stato caricato un disco rigido virtuale di base, è possibile caricare dischi diversi che usano l'immagine di base come elemento padre.</span><span class="sxs-lookup"><span data-stu-id="77445-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="77445-110">È supportato anche l'URI della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="77445-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="77445-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77445-111">EXAMPLES</span></span>

### <span data-ttu-id="77445-112">Esempio 1: Aggiungere un file VHD</span><span class="sxs-lookup"><span data-stu-id="77445-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="77445-113">Questo comando aggiunge un file VHD a un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="77445-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="77445-114">Esempio 2: Aggiungere un file VHD e sovrascrivere la destinazione</span><span class="sxs-lookup"><span data-stu-id="77445-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="77445-115">Questo comando aggiunge un file VHD a un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="77445-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="77445-116">Il comando sovrascrive un file esistente.</span><span class="sxs-lookup"><span data-stu-id="77445-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="77445-117">Esempio 3: Aggiungere un file VHD e specificare il numero di thread</span><span class="sxs-lookup"><span data-stu-id="77445-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="77445-118">Questo comando aggiunge un file VHD a un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="77445-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="77445-119">Il comando specifica il numero di thread da usare per caricare il file.</span><span class="sxs-lookup"><span data-stu-id="77445-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="77445-120">Esempio 4: Aggiungere un file VHD e specificare l'URI di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="77445-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="77445-121">Questo comando aggiunge un file VHD a un account di archiviazione e specifica l'URI di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="77445-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="77445-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77445-122">PARAMETERS</span></span>

### <span data-ttu-id="77445-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77445-123">-AsJob</span></span>
<span data-ttu-id="77445-124">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="77445-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="77445-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="77445-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="77445-126">Specifica l'URI di un BLOB dell'immagine di base in Archiviazione BLOB Azure.</span><span class="sxs-lookup"><span data-stu-id="77445-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="77445-127">È possibile specificare una firma di accesso condiviso come valore per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="77445-127">An SAS can be specified as the value for this parameter.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77445-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77445-128">-DefaultProfile</span></span>
<span data-ttu-id="77445-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77445-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77445-130">-Destination</span><span class="sxs-lookup"><span data-stu-id="77445-130">-Destination</span></span>
<span data-ttu-id="77445-131">Specifica l'URI di un BLOB in Archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="77445-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="77445-132">Il parametro supporta l'URI della firma di accesso condiviso, anche se la destinazione degli scenari di applicazione delle patch non può essere un URI di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="77445-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77445-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="77445-133">-LocalFilePath</span></span>
<span data-ttu-id="77445-134">Specifica il percorso del file VHD locale.</span><span class="sxs-lookup"><span data-stu-id="77445-134">Specifies the path of the local .vhd file.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77445-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="77445-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="77445-136">Specifica il numero di thread del caricatore da usare durante il caricamento del file VHD.</span><span class="sxs-lookup"><span data-stu-id="77445-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77445-137">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="77445-137">-OverWrite</span></span>
<span data-ttu-id="77445-138">Indica che questo cmdlet sovrascrive un BLOB esistente nell'URI di destinazione specificato, se presente.</span><span class="sxs-lookup"><span data-stu-id="77445-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77445-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77445-139">-ResourceGroupName</span></span>
<span data-ttu-id="77445-140">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77445-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77445-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77445-141">CommonParameters</span></span>
<span data-ttu-id="77445-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77445-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77445-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="77445-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77445-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="77445-144">INPUTS</span></span>

### <span data-ttu-id="77445-145">System.String</span><span class="sxs-lookup"><span data-stu-id="77445-145">System.String</span></span>

### <span data-ttu-id="77445-146">System.Uri</span><span class="sxs-lookup"><span data-stu-id="77445-146">System.Uri</span></span>

### <span data-ttu-id="77445-147">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="77445-147">System.IO.FileInfo</span></span>

### <span data-ttu-id="77445-148">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="77445-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="77445-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="77445-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="77445-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77445-150">OUTPUTS</span></span>

### <span data-ttu-id="77445-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span><span class="sxs-lookup"><span data-stu-id="77445-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="77445-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="77445-152">NOTES</span></span>

## <span data-ttu-id="77445-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77445-153">RELATED LINKS</span></span>

[<span data-ttu-id="77445-154">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="77445-154">Save-AzVhd</span></span>](./Save-AzVhd.md)


