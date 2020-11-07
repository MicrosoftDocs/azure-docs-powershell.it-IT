---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVhd.md
ms.openlocfilehash: db2148be139130f5963214c5e66809a3e66a22ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518827"
---
# <span data-ttu-id="9d65b-101">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="9d65b-101">Save-AzureRmVhd</span></span>

## <span data-ttu-id="9d65b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d65b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d65b-103">Salva le immagini scaricate con estensione vhd localmente.</span><span class="sxs-lookup"><span data-stu-id="9d65b-103">Saves downloaded .vhd images locally.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d65b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d65b-104">SYNTAX</span></span>

### <span data-ttu-id="9d65b-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9d65b-105">ResourceGroupParameterSetName</span></span>
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d65b-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9d65b-106">StorageKeyParameterSetName</span></span>
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d65b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d65b-107">DESCRIPTION</span></span>
<span data-ttu-id="9d65b-108">Il cmdlet **Save-AzureRmVhd** Salva le immagini con estensione VHD da un BLOB in cui sono archiviate in un file.</span><span class="sxs-lookup"><span data-stu-id="9d65b-108">The **Save-AzureRmVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="9d65b-109">Puoi specificare il numero di thread di Downloader che il processo USA e se sostituire un file già esistente.</span><span class="sxs-lookup"><span data-stu-id="9d65b-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>
<span data-ttu-id="9d65b-110">Questo cmdlet Scarica il contenuto così com'è.</span><span class="sxs-lookup"><span data-stu-id="9d65b-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="9d65b-111">Non applica una conversione di formato VHD (Virtual Hard disk).</span><span class="sxs-lookup"><span data-stu-id="9d65b-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="9d65b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d65b-112">EXAMPLES</span></span>

### <span data-ttu-id="9d65b-113">Esempio 1: scaricare un'immagine</span><span class="sxs-lookup"><span data-stu-id="9d65b-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="9d65b-114">Questo comando Scarica un file con estensione vhd e lo archivia nel percorso locale C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="9d65b-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="9d65b-115">Esempio 2: scaricare un'immagine e sovrascrivere il file locale</span><span class="sxs-lookup"><span data-stu-id="9d65b-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="9d65b-116">Questo comando Scarica un file con estensione vhd e lo archivia nel percorso locale.</span><span class="sxs-lookup"><span data-stu-id="9d65b-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="9d65b-117">Il comando include il parametro *overwrite* .</span><span class="sxs-lookup"><span data-stu-id="9d65b-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="9d65b-118">Di conseguenza, se C:\vhd\Win7Image.vhd esiste già, questo comando lo sostituisce.</span><span class="sxs-lookup"><span data-stu-id="9d65b-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="9d65b-119">Esempio 3: scaricare un'immagine usando un numero specificato di thread</span><span class="sxs-lookup"><span data-stu-id="9d65b-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="9d65b-120">Questo comando Scarica un file con estensione vhd e lo archivia nel percorso locale.</span><span class="sxs-lookup"><span data-stu-id="9d65b-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="9d65b-121">Il comando specifica un valore di 32 per il parametro *NumberOfThreads* .</span><span class="sxs-lookup"><span data-stu-id="9d65b-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="9d65b-122">Di conseguenza, il cmdlet usa i thread di 32 per questa azione.</span><span class="sxs-lookup"><span data-stu-id="9d65b-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="9d65b-123">Esempio 4: scaricare un'immagine e specificare la chiave di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9d65b-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="9d65b-124">Questo comando Scarica un file con estensione vhd e specifica la chiave di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9d65b-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="9d65b-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d65b-125">PARAMETERS</span></span>

### <span data-ttu-id="9d65b-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d65b-126">-AsJob</span></span>
<span data-ttu-id="9d65b-127">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="9d65b-127">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9d65b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d65b-128">-DefaultProfile</span></span>
<span data-ttu-id="9d65b-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d65b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d65b-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="9d65b-130">-LocalFilePath</span></span>
<span data-ttu-id="9d65b-131">Specifica il percorso del file locale dell'immagine salvata.</span><span class="sxs-lookup"><span data-stu-id="9d65b-131">Specifies the local file path of the saved image.</span></span>

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

### <span data-ttu-id="9d65b-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="9d65b-132">-NumberOfThreads</span></span>
<span data-ttu-id="9d65b-133">Specifica il numero di thread di download usati dal cmdlet durante il download.</span><span class="sxs-lookup"><span data-stu-id="9d65b-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="9d65b-134">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="9d65b-134">-OverWrite</span></span>
<span data-ttu-id="9d65b-135">Indica che questo cmdlet sostituisce il file specificato da *LocalFilePath* se esiste.</span><span class="sxs-lookup"><span data-stu-id="9d65b-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

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

### <span data-ttu-id="9d65b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d65b-136">-ResourceGroupName</span></span>
<span data-ttu-id="9d65b-137">Specifica il nome del gruppo di risorse dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9d65b-137">Specifies the name of the resource group of the storage account.</span></span>

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

### <span data-ttu-id="9d65b-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="9d65b-138">-SourceUri</span></span>
<span data-ttu-id="9d65b-139">Specifica l'URI (Uniform Resource Identifier) del BLOB in `Azure` .</span><span class="sxs-lookup"><span data-stu-id="9d65b-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

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

### <span data-ttu-id="9d65b-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="9d65b-140">-StorageKey</span></span>
<span data-ttu-id="9d65b-141">Specifica la chiave di archiviazione dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="9d65b-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="9d65b-142">Se non si specifica una chiave, questo cmdlet tenterà di determinare la chiave di archiviazione dell'account in *SourceUri* da Azure.</span><span class="sxs-lookup"><span data-stu-id="9d65b-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

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

### <span data-ttu-id="9d65b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d65b-143">CommonParameters</span></span>
<span data-ttu-id="9d65b-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d65b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d65b-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d65b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d65b-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d65b-146">INPUTS</span></span>

### <span data-ttu-id="9d65b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9d65b-147">System.String</span></span>

### <span data-ttu-id="9d65b-148">System. Uri</span><span class="sxs-lookup"><span data-stu-id="9d65b-148">System.Uri</span></span>

## <span data-ttu-id="9d65b-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d65b-149">OUTPUTS</span></span>

### <span data-ttu-id="9d65b-150">Microsoft. Azure. Commands. Compute. Models. VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="9d65b-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="9d65b-151">Note</span><span class="sxs-lookup"><span data-stu-id="9d65b-151">NOTES</span></span>

## <span data-ttu-id="9d65b-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d65b-152">RELATED LINKS</span></span>

[<span data-ttu-id="9d65b-153">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="9d65b-153">Add-AzureRmVhd</span></span>](./Add-AzureRMVhd.md)

