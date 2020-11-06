---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
ms.openlocfilehash: cc43308f0e0051a050b3983968d9c86f67ec66b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521732"
---
# <span data-ttu-id="7d9e7-101">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="7d9e7-101">Save-AzureRmVhd</span></span>

## <span data-ttu-id="7d9e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d9e7-102">SYNOPSIS</span></span>
<span data-ttu-id="7d9e7-103">Salva le immagini scaricate con estensione vhd localmente.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-103">Saves downloaded .vhd images locally.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d9e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d9e7-104">SYNTAX</span></span>

### <span data-ttu-id="7d9e7-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7d9e7-105">ResourceGroupParameterSetName</span></span>
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d9e7-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7d9e7-106">StorageKeyParameterSetName</span></span>
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d9e7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d9e7-107">DESCRIPTION</span></span>
<span data-ttu-id="7d9e7-108">Il cmdlet **Save-AzureRmVhd** Salva le immagini con estensione VHD da un BLOB in cui sono archiviate in un file.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-108">The **Save-AzureRmVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="7d9e7-109">Puoi specificare il numero di thread di Downloader che il processo USA e se sostituire un file già esistente.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>

<span data-ttu-id="7d9e7-110">Questo cmdlet Scarica il contenuto così com'è.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="7d9e7-111">Non applica una conversione di formato VHD (Virtual Hard disk).</span><span class="sxs-lookup"><span data-stu-id="7d9e7-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="7d9e7-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d9e7-112">EXAMPLES</span></span>

### <span data-ttu-id="7d9e7-113">Esempio 1: scaricare un'immagine</span><span class="sxs-lookup"><span data-stu-id="7d9e7-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="7d9e7-114">Questo comando Scarica un file con estensione vhd e lo archivia nel percorso locale C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="7d9e7-115">Esempio 2: scaricare un'immagine e sovrascrivere il file locale</span><span class="sxs-lookup"><span data-stu-id="7d9e7-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="7d9e7-116">Questo comando Scarica un file con estensione vhd e lo archivia nel percorso locale.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="7d9e7-117">Il comando include il parametro *overwrite* .</span><span class="sxs-lookup"><span data-stu-id="7d9e7-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="7d9e7-118">Di conseguenza, se C:\vhd\Win7Image.vhd esiste già, questo comando lo sostituisce.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="7d9e7-119">Esempio 3: scaricare un'immagine usando un numero specificato di thread</span><span class="sxs-lookup"><span data-stu-id="7d9e7-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="7d9e7-120">Questo comando Scarica un file con estensione vhd e lo archivia nel percorso locale.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="7d9e7-121">Il comando specifica un valore di 32 per il parametro *NumberOfThreads* .</span><span class="sxs-lookup"><span data-stu-id="7d9e7-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="7d9e7-122">Di conseguenza, il cmdlet usa i thread di 32 per questa azione.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="7d9e7-123">Esempio 4: scaricare un'immagine e specificare la chiave di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7d9e7-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="7d9e7-124">Questo comando Scarica un file con estensione vhd e specifica la chiave di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="7d9e7-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d9e7-125">PARAMETERS</span></span>

### <span data-ttu-id="7d9e7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d9e7-126">-DefaultProfile</span></span>
<span data-ttu-id="7d9e7-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d9e7-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="7d9e7-128">-LocalFilePath</span></span>
<span data-ttu-id="7d9e7-129">Specifica il percorso del file locale dell'immagine salvata.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-129">Specifies the local file path of the saved image.</span></span>

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

### <span data-ttu-id="7d9e7-130">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="7d9e7-130">-NumberOfThreads</span></span>
<span data-ttu-id="7d9e7-131">Specifica il numero di thread di download usati dal cmdlet durante il download.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-131">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="7d9e7-132">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="7d9e7-132">-OverWrite</span></span>
<span data-ttu-id="7d9e7-133">Indica che questo cmdlet sostituisce il file specificato da *LocalFilePath* se esiste.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-133">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

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

### <span data-ttu-id="7d9e7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d9e7-134">-ResourceGroupName</span></span>
<span data-ttu-id="7d9e7-135">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7d9e7-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="7d9e7-136">-SourceUri</span></span>
<span data-ttu-id="7d9e7-137">Specifica l'URI (Uniform Resource Identifier) del BLOB in `Azure` .</span><span class="sxs-lookup"><span data-stu-id="7d9e7-137">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

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

### <span data-ttu-id="7d9e7-138">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="7d9e7-138">-StorageKey</span></span>
<span data-ttu-id="7d9e7-139">Specifica la chiave di archiviazione dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-139">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="7d9e7-140">Se non si specifica una chiave, questo cmdlet tenterà di determinare la chiave di archiviazione dell'account in *SourceUri* da Azure.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-140">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

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

### <span data-ttu-id="7d9e7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d9e7-141">CommonParameters</span></span>
<span data-ttu-id="7d9e7-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d9e7-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d9e7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d9e7-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d9e7-144">INPUTS</span></span>

## <span data-ttu-id="7d9e7-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d9e7-145">OUTPUTS</span></span>

## <span data-ttu-id="7d9e7-146">Note</span><span class="sxs-lookup"><span data-stu-id="7d9e7-146">NOTES</span></span>

## <span data-ttu-id="7d9e7-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d9e7-147">RELATED LINKS</span></span>

[<span data-ttu-id="7d9e7-148">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="7d9e7-148">Add-AzureRmVhd</span></span>](./Add-AzureRMVhd.md)


