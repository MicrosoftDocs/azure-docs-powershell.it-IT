---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: aee844d36fb2083e56415b34032cf928cb01d99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519747"
---
# <span data-ttu-id="40df1-101">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="40df1-101">Add-AzureRmVhd</span></span>

## <span data-ttu-id="40df1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40df1-102">SYNOPSIS</span></span>
<span data-ttu-id="40df1-103">Carica un disco rigido virtuale da una macchina virtuale locale a un BLOB in un account di archiviazione cloud in Azure.</span><span class="sxs-lookup"><span data-stu-id="40df1-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40df1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40df1-104">SYNTAX</span></span>

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40df1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40df1-105">DESCRIPTION</span></span>
<span data-ttu-id="40df1-106">Il cmdlet **Add-AzureRmVhd** carica i dischi rigidi virtuali locali, in formato file VHD, in un account di archiviazione BLOB come dischi rigidi virtuali fissi.</span><span class="sxs-lookup"><span data-stu-id="40df1-106">The **Add-AzureRmVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="40df1-107">Puoi configurare il numero di thread di Uploader che verranno usati o sovrascriveranno un BLOB esistente nell'URI di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="40df1-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="40df1-108">È anche supportata la possibilità di caricare una versione con patch di un file VHD locale.</span><span class="sxs-lookup"><span data-stu-id="40df1-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="40df1-109">Quando è già stato caricato un disco rigido virtuale di base, è possibile caricare dischi differenze che usano l'immagine di base come padre.</span><span class="sxs-lookup"><span data-stu-id="40df1-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="40df1-110">Anche l'URI della firma di accesso condiviso (SAS) è supportato.</span><span class="sxs-lookup"><span data-stu-id="40df1-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="40df1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40df1-111">EXAMPLES</span></span>

### <span data-ttu-id="40df1-112">Esempio 1: aggiungere un file VHD</span><span class="sxs-lookup"><span data-stu-id="40df1-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="40df1-113">Questo comando aggiunge un file con estensione VHD a un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="40df1-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="40df1-114">Esempio 2: aggiungere un file VHD e sovrascrivere la destinazione</span><span class="sxs-lookup"><span data-stu-id="40df1-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="40df1-115">Questo comando aggiunge un file con estensione VHD a un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="40df1-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="40df1-116">Il comando sovrascrive un file esistente.</span><span class="sxs-lookup"><span data-stu-id="40df1-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="40df1-117">Esempio 3: aggiungere un file VHD e specificare il numero di thread</span><span class="sxs-lookup"><span data-stu-id="40df1-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="40df1-118">Questo comando aggiunge un file con estensione VHD a un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="40df1-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="40df1-119">Il comando specifica il numero di thread da usare per caricare il file.</span><span class="sxs-lookup"><span data-stu-id="40df1-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="40df1-120">Esempio 4: aggiungere un file VHD e specificare l'URI SAS</span><span class="sxs-lookup"><span data-stu-id="40df1-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="40df1-121">Questo comando aggiunge un file con estensione VHD a un account di archiviazione e specifica l'URI SAS.</span><span class="sxs-lookup"><span data-stu-id="40df1-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="40df1-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40df1-122">PARAMETERS</span></span>

### <span data-ttu-id="40df1-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40df1-123">-AsJob</span></span>
<span data-ttu-id="40df1-124">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="40df1-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="40df1-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="40df1-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="40df1-126">Specifica l'URI per un BLOB di immagini di base nell'archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="40df1-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="40df1-127">Un SAS può essere specificato come valore per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="40df1-127">An SAS can be specified as the value for this parameter.</span></span>

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

### <span data-ttu-id="40df1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40df1-128">-DefaultProfile</span></span>
<span data-ttu-id="40df1-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40df1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40df1-130">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="40df1-130">-Destination</span></span>
<span data-ttu-id="40df1-131">Specifica l'URI di un BLOB nell'archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="40df1-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="40df1-132">Il parametro supporta l'URI SAS, anche se la destinazione degli scenari di correzione non può essere un URI SAS.</span><span class="sxs-lookup"><span data-stu-id="40df1-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

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

### <span data-ttu-id="40df1-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="40df1-133">-LocalFilePath</span></span>
<span data-ttu-id="40df1-134">Specifica il percorso del file con estensione VHD locale.</span><span class="sxs-lookup"><span data-stu-id="40df1-134">Specifies the path of the local .vhd file.</span></span>

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

### <span data-ttu-id="40df1-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="40df1-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="40df1-136">Specifica il numero di thread di Uploader da usare durante il caricamento del file con estensione vhd.</span><span class="sxs-lookup"><span data-stu-id="40df1-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

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

### <span data-ttu-id="40df1-137">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="40df1-137">-OverWrite</span></span>
<span data-ttu-id="40df1-138">Indica che questo cmdlet sovrascrive un BLOB esistente nell'URI di destinazione specificato, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="40df1-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

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

### <span data-ttu-id="40df1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40df1-139">-ResourceGroupName</span></span>
<span data-ttu-id="40df1-140">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="40df1-140">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="40df1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40df1-141">CommonParameters</span></span>
<span data-ttu-id="40df1-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40df1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40df1-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40df1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40df1-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40df1-144">INPUTS</span></span>

### <span data-ttu-id="40df1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="40df1-145">System.String</span></span>

### <span data-ttu-id="40df1-146">System. Uri</span><span class="sxs-lookup"><span data-stu-id="40df1-146">System.Uri</span></span>

### <span data-ttu-id="40df1-147">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="40df1-147">System.IO.FileInfo</span></span>

### <span data-ttu-id="40df1-148">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="40df1-148">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="40df1-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="40df1-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="40df1-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40df1-150">OUTPUTS</span></span>

### <span data-ttu-id="40df1-151">Microsoft. Azure. Commands. Compute. Models. VhdUploadContext</span><span class="sxs-lookup"><span data-stu-id="40df1-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="40df1-152">Note</span><span class="sxs-lookup"><span data-stu-id="40df1-152">NOTES</span></span>

## <span data-ttu-id="40df1-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40df1-153">RELATED LINKS</span></span>

[<span data-ttu-id="40df1-154">Salva-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="40df1-154">Save-AzureRmVhd</span></span>](./Save-AzureRmVhd.md)


