---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4660D0A-26CB-488C-9A29-3ED94A0DCDA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e62cb7ed272a5c0d5ff4ff0ecbafe30a0c5ee9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023419"
---
# <span data-ttu-id="2bb52-101">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="2bb52-101">Save-AzureVhd</span></span>

## <span data-ttu-id="2bb52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2bb52-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb52-103">Consente il download di immagini con estensione vhd.</span><span class="sxs-lookup"><span data-stu-id="2bb52-103">Enables download of .vhd images.</span></span>

## <span data-ttu-id="2bb52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bb52-104">SYNTAX</span></span>

```
Save-AzureVhd [-Source] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>] [[-StorageKey] <String>]
 [-OverWrite] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2bb52-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bb52-105">DESCRIPTION</span></span>
<span data-ttu-id="2bb52-106">Il cmdlet **Save-AzureVhd** consente il download di immagini con estensione VHD da un BLOB in cui sono archiviate in un file.</span><span class="sxs-lookup"><span data-stu-id="2bb52-106">The **Save-AzureVhd** cmdlet enables download of .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="2bb52-107">Include parametri per configurare il processo di download specificando il numero di thread di Downloader usati o sovrascrivendo il file già esistente nel percorso di file specificato.</span><span class="sxs-lookup"><span data-stu-id="2bb52-107">It has parameters to configure the download process by specifying the number of downloader threads that are used or overwriting the file which already exists in the specified file path.</span></span>

<span data-ttu-id="2bb52-108">**Save-AzureVhd** non esegue alcuna conversione di formato VHD e il BLOB viene scaricato così com'è.</span><span class="sxs-lookup"><span data-stu-id="2bb52-108">**Save-AzureVhd** does not do any VHD format conversion and the blob is downloaded as it is.</span></span>

## <span data-ttu-id="2bb52-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bb52-109">EXAMPLES</span></span>

### <span data-ttu-id="2bb52-110">Esempio 1: scaricare un file VHD</span><span class="sxs-lookup"><span data-stu-id="2bb52-110">Example 1: Download a VHD file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="2bb52-111">Questo comando Scarica un file con estensione vhd.</span><span class="sxs-lookup"><span data-stu-id="2bb52-111">This command downloads a .vhd file.</span></span>

### <span data-ttu-id="2bb52-112">Esempio 2: scaricare un file VHD e sovrascrivere il file locale</span><span class="sxs-lookup"><span data-stu-id="2bb52-112">Example 2: Download a VHD file and overwrite the local file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="2bb52-113">Questo comando Scarica un file con estensione vhd e sovrascrive qualsiasi file nel percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2bb52-113">This command downloads a .vhd file and overwrites any file in the destination path.</span></span>

### <span data-ttu-id="2bb52-114">Esempio 3: scaricare un file VHD e specificare il numero di thread</span><span class="sxs-lookup"><span data-stu-id="2bb52-114">Example 3: Download a VHD file and specify the number of threads</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="2bb52-115">Questo comando Scarica un file con estensione vhd e specifica il numero di thread.</span><span class="sxs-lookup"><span data-stu-id="2bb52-115">This command downloads a .vhd file and specifies the number of threads.</span></span>

### <span data-ttu-id="2bb52-116">Esempio 4: scaricare un file VHD e specificare la chiave di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2bb52-116">Example 4: Download a VHD file and specify the storage key</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="2bb52-117">Questo comando Scarica un file con estensione vhd e specifica la chiave di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2bb52-117">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="2bb52-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2bb52-118">PARAMETERS</span></span>

### <span data-ttu-id="2bb52-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2bb52-119">-InformationAction</span></span>
<span data-ttu-id="2bb52-120">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="2bb52-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2bb52-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2bb52-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2bb52-122">Continuare</span><span class="sxs-lookup"><span data-stu-id="2bb52-122">Continue</span></span>
- <span data-ttu-id="2bb52-123">Ignora</span><span class="sxs-lookup"><span data-stu-id="2bb52-123">Ignore</span></span>
- <span data-ttu-id="2bb52-124">Informarsi</span><span class="sxs-lookup"><span data-stu-id="2bb52-124">Inquire</span></span>
- <span data-ttu-id="2bb52-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2bb52-125">SilentlyContinue</span></span>
- <span data-ttu-id="2bb52-126">Stop</span><span class="sxs-lookup"><span data-stu-id="2bb52-126">Stop</span></span>
- <span data-ttu-id="2bb52-127">Sospensione</span><span class="sxs-lookup"><span data-stu-id="2bb52-127">Suspend</span></span>

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

### <span data-ttu-id="2bb52-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2bb52-128">-InformationVariable</span></span>
<span data-ttu-id="2bb52-129">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="2bb52-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2bb52-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="2bb52-130">-LocalFilePath</span></span>
<span data-ttu-id="2bb52-131">Specifica il percorso del file locale.</span><span class="sxs-lookup"><span data-stu-id="2bb52-131">Specifies the local file path.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb52-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="2bb52-132">-NumberOfThreads</span></span>
<span data-ttu-id="2bb52-133">Specifica il numero di thread di download usati dal cmdlet durante il download.</span><span class="sxs-lookup"><span data-stu-id="2bb52-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb52-134">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="2bb52-134">-OverWrite</span></span>
<span data-ttu-id="2bb52-135">Specifica che questo cmdlet elimina il file specificato dal file *LocalFilePath* , se esistente.</span><span class="sxs-lookup"><span data-stu-id="2bb52-135">Specifies that this cmdlet deletes the file specified by *LocalFilePath* file if it exists.</span></span>

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

### <span data-ttu-id="2bb52-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="2bb52-136">-Profile</span></span>
<span data-ttu-id="2bb52-137">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bb52-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2bb52-138">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2bb52-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2bb52-139">-Origine</span><span class="sxs-lookup"><span data-stu-id="2bb52-139">-Source</span></span>
<span data-ttu-id="2bb52-140">Specifica l'URI (Uniform Resource Identifier) del BLOB in `Azure` .</span><span class="sxs-lookup"><span data-stu-id="2bb52-140">Specifies the Uniform Resource Identifier (URI) to the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bb52-141">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="2bb52-141">-StorageKey</span></span>
<span data-ttu-id="2bb52-142">Specifica la chiave di archiviazione dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="2bb52-142">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="2bb52-143">Se non è disponibile, **Salva-AzureVhd** tenta di determinare la chiave di archiviazione dell'account in *SourceUri* da Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb52-143">If it is not provided, **Save-AzureVhd** attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sk

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb52-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb52-144">CommonParameters</span></span>
<span data-ttu-id="2bb52-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bb52-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb52-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bb52-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb52-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2bb52-147">INPUTS</span></span>

## <span data-ttu-id="2bb52-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bb52-148">OUTPUTS</span></span>

## <span data-ttu-id="2bb52-149">Note</span><span class="sxs-lookup"><span data-stu-id="2bb52-149">NOTES</span></span>

## <span data-ttu-id="2bb52-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bb52-150">RELATED LINKS</span></span>

[<span data-ttu-id="2bb52-151">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="2bb52-151">Add-AzureVhd</span></span>](./Add-AzureVhd.md)


