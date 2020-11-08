---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DBC4A0B8-A34A-47AC-930B-EFE23A95A216
online version: ''
schema: 2.0.0
ms.openlocfilehash: 178349299767eefb1d89c31a0199f53373bd2ae2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023953"
---
# <span data-ttu-id="373ca-101">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="373ca-101">New-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="373ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="373ca-102">SYNOPSIS</span></span>
<span data-ttu-id="373ca-103">Carica o importa un'immagine del modello RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="373ca-103">Uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="373ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="373ca-104">SYNTAX</span></span>

### <span data-ttu-id="373ca-105">UploadLocalVhd (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="373ca-105">UploadLocalVhd (Default)</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> [-Path] <String> [-Resume]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="373ca-106">AzureVmUpload</span><span class="sxs-lookup"><span data-stu-id="373ca-106">AzureVmUpload</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> -AzureVmImageName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="373ca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="373ca-107">DESCRIPTION</span></span>
<span data-ttu-id="373ca-108">Il cmdlet **New-AzureRemoteAppTemplateImage** carica o importa un'immagine del modello RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="373ca-108">The **New-AzureRemoteAppTemplateImage** cmdlet uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="373ca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="373ca-109">EXAMPLES</span></span>

### <span data-ttu-id="373ca-110">Esempio 1: caricare un file VHD per creare un'immagine modello</span><span class="sxs-lookup"><span data-stu-id="373ca-110">Example 1: Upload a VHD file to create a template image</span></span>
```
PS C:\> New-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -Location "North Europe" -Path "C:\RemoteAppImages\ContosoApps.vhd"
```

<span data-ttu-id="373ca-111">Questo comando carica C:\RemoteAppImages\ContosoApps.vhd per creare un'immagine modello denominata ContosoApps nel centro dati Nord Europa.</span><span class="sxs-lookup"><span data-stu-id="373ca-111">This command uploads C:\RemoteAppImages\ContosoApps.vhd to create a template image named ContosoApps in the North Europe data center.</span></span>

## <span data-ttu-id="373ca-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="373ca-112">PARAMETERS</span></span>

### <span data-ttu-id="373ca-113">-AzureVmImageName</span><span class="sxs-lookup"><span data-stu-id="373ca-113">-AzureVmImageName</span></span>
<span data-ttu-id="373ca-114">Specifica il nome di una macchina virtuale di Azure da usare come immagine del modello.</span><span class="sxs-lookup"><span data-stu-id="373ca-114">Specifies the name of an Azure virtual machine to use as a template image.</span></span>

```yaml
Type: String
Parameter Sets: AzureVmUpload
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="373ca-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="373ca-115">-ImageName</span></span>
<span data-ttu-id="373ca-116">Specifica il nome di un'immagine del modello RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="373ca-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="373ca-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="373ca-117">-Location</span></span>
<span data-ttu-id="373ca-118">Specifica l'area di Azure dell'immagine del modello.</span><span class="sxs-lookup"><span data-stu-id="373ca-118">Specifies the Azure region of the template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="373ca-119">-Path</span><span class="sxs-lookup"><span data-stu-id="373ca-119">-Path</span></span>
<span data-ttu-id="373ca-120">Specifica il percorso del file dell'immagine del modello.</span><span class="sxs-lookup"><span data-stu-id="373ca-120">Specifies the file path of the template image.</span></span>

```yaml
Type: String
Parameter Sets: UploadLocalVhd
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="373ca-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="373ca-121">-Profile</span></span>
<span data-ttu-id="373ca-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="373ca-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="373ca-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="373ca-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="373ca-124">-Curriculum vitae</span><span class="sxs-lookup"><span data-stu-id="373ca-124">-Resume</span></span>
<span data-ttu-id="373ca-125">Indica che questo cmdlet riprende se il caricamento di un'immagine del modello viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="373ca-125">Indicates that this cmdlet resumes if the upload of a template image is interrupted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UploadLocalVhd
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="373ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373ca-126">CommonParameters</span></span>
<span data-ttu-id="373ca-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="373ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373ca-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="373ca-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="373ca-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="373ca-129">INPUTS</span></span>

## <span data-ttu-id="373ca-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="373ca-130">OUTPUTS</span></span>

## <span data-ttu-id="373ca-131">Note</span><span class="sxs-lookup"><span data-stu-id="373ca-131">NOTES</span></span>

## <span data-ttu-id="373ca-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="373ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="373ca-133">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="373ca-133">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="373ca-134">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="373ca-134">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="373ca-135">Rinominare-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="373ca-135">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


