---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023676"
---
# <span data-ttu-id="6671f-101">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="6671f-101">Add-AzureVhd</span></span>

## <span data-ttu-id="6671f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6671f-102">SYNOPSIS</span></span>
<span data-ttu-id="6671f-103">Carica un file VHD da un computer locale a un BLOB in un account di archiviazione cloud in Azure.</span><span class="sxs-lookup"><span data-stu-id="6671f-103">Uploads a VHD file from an on-premise computer to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="6671f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6671f-104">SYNTAX</span></span>

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6671f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6671f-105">DESCRIPTION</span></span>
<span data-ttu-id="6671f-106">Il cmdlet **Add-AzureVhd** carica le immagini del disco rigido virtuale (VHD) locale in un account di archiviazione BLOB come immagini fisse con estensione vhd.</span><span class="sxs-lookup"><span data-stu-id="6671f-106">The **Add-AzureVhd** cmdlet uploads on premise Virtual hard disk (VHD) images to a blob storage account as fixed .vhd images.</span></span>
<span data-ttu-id="6671f-107">Include parametri per configurare il processo di caricamento, ad esempio specificando il numero di thread di Uploader che verranno usati o sovrascrivendo un BLOB già esistente nell'URI di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="6671f-107">It has parameters to configure the upload process such as specifying the number of uploader threads that will be used or overwriting a blob which already exists in the specified destination URI.</span></span>
<span data-ttu-id="6671f-108">Per le immagini VHD locali, è anche supportato lo scenario di patching in modo che le immagini del disco diff possano essere caricate senza dover caricare le immagini di base già caricate.</span><span class="sxs-lookup"><span data-stu-id="6671f-108">For on premise VHD images, patching scenario is also supported so that diff disk images can be uploaded without having to upload the already uploaded base images.</span></span> <span data-ttu-id="6671f-109">È anche supportato l'URI della firma di accesso condiviso (SAS).</span><span class="sxs-lookup"><span data-stu-id="6671f-109">Shared Access Signature (SAS) URI is also supported.</span></span>

## <span data-ttu-id="6671f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6671f-110">EXAMPLES</span></span>

### <span data-ttu-id="6671f-111">Esempio 1: aggiungere un file VHD</span><span class="sxs-lookup"><span data-stu-id="6671f-111">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="6671f-112">Questo comando aggiunge un file con estensione VHD a un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6671f-112">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="6671f-113">Esempio 2: aggiungere un file VHD e sovrascrivere la destinazione</span><span class="sxs-lookup"><span data-stu-id="6671f-113">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="6671f-114">Questo comando aggiunge un file con estensione VHD a un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6671f-114">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="6671f-115">Esempio 3: aggiungere un file VHD e specificare il numero di thread</span><span class="sxs-lookup"><span data-stu-id="6671f-115">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="6671f-116">Questo comando aggiunge un file con estensione VHD a un account di archiviazione e specifica il numero di thread da usare per caricare il file.</span><span class="sxs-lookup"><span data-stu-id="6671f-116">This command adds a .vhd file to a storage account and specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="6671f-117">Esempio 4: aggiungere un file VHD e specificare l'URI SAS</span><span class="sxs-lookup"><span data-stu-id="6671f-117">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="6671f-118">Questo comando aggiunge un file con estensione VHD a un account di archiviazione e specifica l'URI SAS.</span><span class="sxs-lookup"><span data-stu-id="6671f-118">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="6671f-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6671f-119">PARAMETERS</span></span>

### <span data-ttu-id="6671f-120">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="6671f-120">-BaseImageUriToPatch</span></span>
<span data-ttu-id="6671f-121">Specifica un URI per un BLOB di immagini di base nell'archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="6671f-121">Specifies an URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="6671f-122">Anche SAS nell'input URI è supportato.</span><span class="sxs-lookup"><span data-stu-id="6671f-122">SAS in URI input is supported as well.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6671f-123">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="6671f-123">-Destination</span></span>
<span data-ttu-id="6671f-124">Specifica un URI per un BLOB nell'archiviazione BLOB di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6671f-124">Specifies a URI to a blob in Microsoft Azure Blob Storage.</span></span>
<span data-ttu-id="6671f-125">SAS nell'input URI è supportato.</span><span class="sxs-lookup"><span data-stu-id="6671f-125">SAS in URI input is supported.</span></span>
<span data-ttu-id="6671f-126">Tuttavia, in scenari di patch la destinazione non può essere un URI SAS.</span><span class="sxs-lookup"><span data-stu-id="6671f-126">However, in patching scenarios the destination cannot be a SAS URI.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6671f-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6671f-127">-InformationAction</span></span>
<span data-ttu-id="6671f-128">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="6671f-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6671f-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6671f-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6671f-130">Continuare</span><span class="sxs-lookup"><span data-stu-id="6671f-130">Continue</span></span>
- <span data-ttu-id="6671f-131">Ignora</span><span class="sxs-lookup"><span data-stu-id="6671f-131">Ignore</span></span>
- <span data-ttu-id="6671f-132">Informarsi</span><span class="sxs-lookup"><span data-stu-id="6671f-132">Inquire</span></span>
- <span data-ttu-id="6671f-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6671f-133">SilentlyContinue</span></span>
- <span data-ttu-id="6671f-134">Stop</span><span class="sxs-lookup"><span data-stu-id="6671f-134">Stop</span></span>
- <span data-ttu-id="6671f-135">Sospensione</span><span class="sxs-lookup"><span data-stu-id="6671f-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6671f-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6671f-136">-InformationVariable</span></span>
<span data-ttu-id="6671f-137">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="6671f-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6671f-138">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="6671f-138">-LocalFilePath</span></span>
<span data-ttu-id="6671f-139">Specie il percorso del file con estensione VHD locale.</span><span class="sxs-lookup"><span data-stu-id="6671f-139">Species the file path of the local .vhd file.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6671f-140">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="6671f-140">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="6671f-141">Specifica il numero di thread da usare per il caricamento.</span><span class="sxs-lookup"><span data-stu-id="6671f-141">Specifies the number of threads to use for upload.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6671f-142">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="6671f-142">-OverWrite</span></span>
<span data-ttu-id="6671f-143">Specifica che questo cmdlet elimina il BLOB esistente nell'URI di destinazione specificato se esiste.</span><span class="sxs-lookup"><span data-stu-id="6671f-143">Specifies that this cmdlet deletes the existing blob in the specified destination URI if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6671f-144">-Profile</span><span class="sxs-lookup"><span data-stu-id="6671f-144">-Profile</span></span>
<span data-ttu-id="6671f-145">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6671f-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6671f-146">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6671f-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6671f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6671f-147">CommonParameters</span></span>
<span data-ttu-id="6671f-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6671f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6671f-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6671f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6671f-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6671f-150">INPUTS</span></span>

## <span data-ttu-id="6671f-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6671f-151">OUTPUTS</span></span>

## <span data-ttu-id="6671f-152">Note</span><span class="sxs-lookup"><span data-stu-id="6671f-152">NOTES</span></span>

## <span data-ttu-id="6671f-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6671f-153">RELATED LINKS</span></span>

[<span data-ttu-id="6671f-154">Salva-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="6671f-154">Save-AzureVhd</span></span>](./Save-AzureVhd.md)


