---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: 106f6d9ed794ac2e4595f480616fa2c64663e554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521772"
---
# <span data-ttu-id="4fa9d-101">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="4fa9d-101">Add-AzureRmVhd</span></span>

## <span data-ttu-id="4fa9d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fa9d-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa9d-103">Carica un disco rigido virtuale da una macchina virtuale locale a un BLOB in un account di archiviazione cloud in Azure.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fa9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fa9d-104">SYNTAX</span></span>

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fa9d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fa9d-105">DESCRIPTION</span></span>
<span data-ttu-id="4fa9d-106">Il cmdlet **Add-AzureRmVhd** carica i dischi rigidi virtuali locali, in formato file VHD, in un account di archiviazione BLOB come dischi rigidi virtuali fissi.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-106">The **Add-AzureRmVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="4fa9d-107">Puoi configurare il numero di thread di Uploader che verranno usati o sovrascriveranno un BLOB esistente nell'URI di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="4fa9d-108">È anche supportata la possibilità di caricare una versione con patch di un file VHD locale.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="4fa9d-109">Quando è già stato caricato un disco rigido virtuale di base, è possibile caricare dischi differenze che usano l'immagine di base come padre.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="4fa9d-110">Anche l'URI della firma di accesso condiviso (SAS) è supportato.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="4fa9d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fa9d-111">EXAMPLES</span></span>

### <span data-ttu-id="4fa9d-112">Esempio 1: aggiungere un file VHD</span><span class="sxs-lookup"><span data-stu-id="4fa9d-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="4fa9d-113">Questo comando aggiunge un file con estensione VHD a un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="4fa9d-114">Esempio 2: aggiungere un file VHD e sovrascrivere la destinazione</span><span class="sxs-lookup"><span data-stu-id="4fa9d-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="4fa9d-115">Questo comando aggiunge un file con estensione VHD a un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="4fa9d-116">Il comando sovrascrive un file esistente.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="4fa9d-117">Esempio 3: aggiungere un file VHD e specificare il numero di thread</span><span class="sxs-lookup"><span data-stu-id="4fa9d-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="4fa9d-118">Questo comando aggiunge un file con estensione VHD a un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="4fa9d-119">Il comando specifica il numero di thread da usare per caricare il file.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="4fa9d-120">Esempio 4: aggiungere un file VHD e specificare l'URI SAS</span><span class="sxs-lookup"><span data-stu-id="4fa9d-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="4fa9d-121">Questo comando aggiunge un file con estensione VHD a un account di archiviazione e specifica l'URI SAS.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="4fa9d-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fa9d-122">PARAMETERS</span></span>

### <span data-ttu-id="4fa9d-123">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="4fa9d-123">-BaseImageUriToPatch</span></span>
<span data-ttu-id="4fa9d-124">Specifica l'URI per un BLOB di immagini di base nell'archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-124">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="4fa9d-125">Un SAS può essere specificato come valore per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-125">An SAS can be specified as the value for this parameter.</span></span>

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

### <span data-ttu-id="4fa9d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa9d-126">-DefaultProfile</span></span>
<span data-ttu-id="4fa9d-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fa9d-128">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="4fa9d-128">-Destination</span></span>
<span data-ttu-id="4fa9d-129">Specifica l'URI di un BLOB nell'archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-129">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="4fa9d-130">Il parametro supporta l'URI SAS, anche se la destinazione degli scenari di correzione non può essere un URI SAS.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-130">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

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

### <span data-ttu-id="4fa9d-131">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="4fa9d-131">-LocalFilePath</span></span>
<span data-ttu-id="4fa9d-132">Specifica il percorso del file con estensione VHD locale.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-132">Specifies the path of the local .vhd file.</span></span>

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

### <span data-ttu-id="4fa9d-133">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="4fa9d-133">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="4fa9d-134">Specifica il numero di thread di Uploader da usare durante il caricamento del file con estensione vhd.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-134">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

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

### <span data-ttu-id="4fa9d-135">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="4fa9d-135">-OverWrite</span></span>
<span data-ttu-id="4fa9d-136">Indica che questo cmdlet sovrascrive un BLOB esistente nell'URI di destinazione specificato, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-136">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

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

### <span data-ttu-id="4fa9d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fa9d-137">-ResourceGroupName</span></span>
<span data-ttu-id="4fa9d-138">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-138">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4fa9d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa9d-139">CommonParameters</span></span>
<span data-ttu-id="4fa9d-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fa9d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa9d-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fa9d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa9d-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fa9d-142">INPUTS</span></span>

## <span data-ttu-id="4fa9d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fa9d-143">OUTPUTS</span></span>

## <span data-ttu-id="4fa9d-144">Note</span><span class="sxs-lookup"><span data-stu-id="4fa9d-144">NOTES</span></span>

## <span data-ttu-id="4fa9d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fa9d-145">RELATED LINKS</span></span>

[<span data-ttu-id="4fa9d-146">Salva-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="4fa9d-146">Save-AzureRmVhd</span></span>](./Save-AzureRmVhd.md)


