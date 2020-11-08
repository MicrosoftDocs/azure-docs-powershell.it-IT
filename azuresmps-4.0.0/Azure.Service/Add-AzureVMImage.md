---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DECCEE-86C8-4662-9ED0-D1BDB4E687C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68efd1c750646abffa90eb8318d0df189a4c9eb9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023673"
---
# <span data-ttu-id="c2aa7-101">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c2aa7-101">Add-AzureVMImage</span></span>

## <span data-ttu-id="c2aa7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="c2aa7-103">Aggiunge una nuova immagine del sistema operativo o una nuova immagine della macchina virtuale al repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-103">Adds a new operating system image or a new virtual machine image to the image repository.</span></span>

## <span data-ttu-id="c2aa7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2aa7-104">SYNTAX</span></span>

### <span data-ttu-id="c2aa7-105">OSImage (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2aa7-105">OSImage (Default)</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-MediaLocation] <String> [-OS] <String> [[-Label] <String>]
 [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>]
 [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>] [[-SmallIconName] <String>]
 [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c2aa7-106">VMImage</span><span class="sxs-lookup"><span data-stu-id="c2aa7-106">VMImage</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-OS] <String>]
 [[-Label] <String>] [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>]
 [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c2aa7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2aa7-107">DESCRIPTION</span></span>
<span data-ttu-id="c2aa7-108">Il cmdlet **Add-AzureVMImage** aggiunge una nuova immagine del sistema operativo o una nuova immagine della macchina virtuale al repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-108">The **Add-AzureVMImage** cmdlet adds a new operating system image or a new virtual machine image to the image repository.</span></span>
<span data-ttu-id="c2aa7-109">L'immagine è un'immagine del sistema operativo generalizzata, che usa Sysprep per Windows o, per Linux, usando lo strumento appropriato per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-109">The image is a generalized operating system image, using either Sysprep for Windows or, for Linux, using the appropriate tool for the distribution.</span></span>

## <span data-ttu-id="c2aa7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2aa7-110">EXAMPLES</span></span>

### <span data-ttu-id="c2aa7-111">Esempio 1: aggiungere un'immagine del sistema operativo al repository</span><span class="sxs-lookup"><span data-stu-id="c2aa7-111">Example 1: Add an operating system image to the repository</span></span>
```
PS C:\> $S = New-AzureVMImageDiskConfigSet
PS C:\> Set-AzureVMImageOSDiskConfig -DiskConfig $S -HostCaching ReadWrite -OSState "Generalized" -OS "Windows" -MediaLink $Link
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test1" -HostCaching ReadWrite -Lun 0 -MediaLink $Link1
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4" -HostCaching ReadWrite -Lun 0 -MediaLink $Link
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4"
PS C:\> $IMGName = "TestCREATEvmimage2";
PS C:\> Add-AzureVMImage -ImageName $IMGName -Label "Test1" -Description "Test1" -DiskConfig $S -Eula "http://www.contoso.com" -ImageFamily Windows -PublishedDate (Get-Date) -PrivacyUri "http://www.test.com" -RecommendedVMSize Small -IconName "Icon01" -SmallIconName "SmallIcon01" -ShowInGui
```

<span data-ttu-id="c2aa7-112">Questo esempio aggiunge un'immagine del sistema operativo al repository.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-112">This example adds an operating system image to the repository.</span></span>

## <span data-ttu-id="c2aa7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2aa7-113">PARAMETERS</span></span>

### <span data-ttu-id="c2aa7-114">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2aa7-114">-Description</span></span>
<span data-ttu-id="c2aa7-115">Specifica la descrizione dell'immagine del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-115">Specifies the description of the operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="c2aa7-116">-DiskConfig</span></span>
<span data-ttu-id="c2aa7-117">Specifica la configurazione del disco del sistema operativo per l'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-117">Specifies the operating system disk configuration for the virtual machine image.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: VMImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-118">-EULA</span><span class="sxs-lookup"><span data-stu-id="c2aa7-118">-Eula</span></span>
<span data-ttu-id="c2aa7-119">Specifica il contratto di licenza con l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-119">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="c2aa7-120">È consigliabile usare un URL per questo valore.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-120">It is recommended that you use an URL for this value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-121">-IconName</span><span class="sxs-lookup"><span data-stu-id="c2aa7-121">-IconName</span></span>
<span data-ttu-id="c2aa7-122">Specifica il nome dell'icona che viene usata quando l'immagine viene aggiunta al repository.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-122">Specifies the name of the icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-123">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="c2aa7-123">-ImageFamily</span></span>
<span data-ttu-id="c2aa7-124">Specifica un valore usato per raggruppare le immagini del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-124">Specifies a value that is used to group operating system images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-125">-ImageName</span><span class="sxs-lookup"><span data-stu-id="c2aa7-125">-ImageName</span></span>
<span data-ttu-id="c2aa7-126">Specifica il nome dell'immagine che viene aggiunta al repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-126">Specifies the name of the image being added to the image repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c2aa7-127">-InformationAction</span></span>
<span data-ttu-id="c2aa7-128">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c2aa7-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2aa7-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2aa7-130">Continuare</span><span class="sxs-lookup"><span data-stu-id="c2aa7-130">Continue</span></span>
- <span data-ttu-id="c2aa7-131">Ignora</span><span class="sxs-lookup"><span data-stu-id="c2aa7-131">Ignore</span></span>
- <span data-ttu-id="c2aa7-132">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c2aa7-132">Inquire</span></span>
- <span data-ttu-id="c2aa7-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c2aa7-133">SilentlyContinue</span></span>
- <span data-ttu-id="c2aa7-134">Stop</span><span class="sxs-lookup"><span data-stu-id="c2aa7-134">Stop</span></span>
- <span data-ttu-id="c2aa7-135">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c2aa7-135">Suspend</span></span>

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

### <span data-ttu-id="c2aa7-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c2aa7-136">-InformationVariable</span></span>
<span data-ttu-id="c2aa7-137">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c2aa7-138">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="c2aa7-138">-Label</span></span>
<span data-ttu-id="c2aa7-139">Specifica un'etichetta per assegnare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-139">Specifies a label to give the image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-140">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="c2aa7-140">-MediaLocation</span></span>
<span data-ttu-id="c2aa7-141">Specifica la posizione della pagina BLOB fisico in cui si trova l'immagine.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-141">Specifies the location of the physical blob page where the image resides.</span></span>
<span data-ttu-id="c2aa7-142">Si tratta di un collegamento a una pagina BLOB nello spazio di archiviazione corrente dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-142">This is a link to a blob page in the current subscription's storage.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-143">-OS</span><span class="sxs-lookup"><span data-stu-id="c2aa7-143">-OS</span></span>
<span data-ttu-id="c2aa7-144">Specifica la versione del sistema operativo dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-144">Specifies the operating system version of the image.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: VMImage
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-145">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="c2aa7-145">-PrivacyUri</span></span>
<span data-ttu-id="c2aa7-146">Specifica l'URL che punta a un documento che contiene i criteri di privacy correlati all'immagine del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-146">Specifies the URL that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="c2aa7-147">-Profile</span></span>
<span data-ttu-id="c2aa7-148">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c2aa7-149">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c2aa7-150">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="c2aa7-150">-PublishedDate</span></span>
<span data-ttu-id="c2aa7-151">Specifica la data in cui l'immagine del sistema operativo è stata aggiunta al repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-151">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-152">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="c2aa7-152">-RecommendedVMSize</span></span>
<span data-ttu-id="c2aa7-153">Specifica le dimensioni da usare per la macchina virtuale creata dall'immagine del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-153">Specifies the size to use for the virtual machine that is created from the operating system image.</span></span>

<span data-ttu-id="c2aa7-154">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2aa7-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2aa7-155">Medio</span><span class="sxs-lookup"><span data-stu-id="c2aa7-155">Medium</span></span>
- <span data-ttu-id="c2aa7-156">Grande</span><span class="sxs-lookup"><span data-stu-id="c2aa7-156">Large</span></span>
- <span data-ttu-id="c2aa7-157">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="c2aa7-157">ExtraLarge</span></span>
- <span data-ttu-id="c2aa7-158">A5</span><span class="sxs-lookup"><span data-stu-id="c2aa7-158">A5</span></span>
- <span data-ttu-id="c2aa7-159">A6</span><span class="sxs-lookup"><span data-stu-id="c2aa7-159">A6</span></span>
- <span data-ttu-id="c2aa7-160">A7</span><span class="sxs-lookup"><span data-stu-id="c2aa7-160">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-161">-ShowInGui</span><span class="sxs-lookup"><span data-stu-id="c2aa7-161">-ShowInGui</span></span>
<span data-ttu-id="c2aa7-162">Indica che questo cmdlet Mostra l'immagine nella GUI.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-162">Indicates that this cmdlet shows the image in the GUI.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-163">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="c2aa7-163">-SmallIconName</span></span>
<span data-ttu-id="c2aa7-164">Specifica il nome dell'icona piccola usata quando l'immagine viene aggiunta al repository.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-164">Specifies the name of the small icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2aa7-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2aa7-165">CommonParameters</span></span>
<span data-ttu-id="c2aa7-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2aa7-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2aa7-167">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2aa7-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2aa7-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2aa7-168">INPUTS</span></span>

## <span data-ttu-id="c2aa7-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2aa7-169">OUTPUTS</span></span>

### <span data-ttu-id="c2aa7-170">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="c2aa7-170">OSImageContext</span></span>

## <span data-ttu-id="c2aa7-171">Note</span><span class="sxs-lookup"><span data-stu-id="c2aa7-171">NOTES</span></span>

## <span data-ttu-id="c2aa7-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2aa7-172">RELATED LINKS</span></span>

[<span data-ttu-id="c2aa7-173">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c2aa7-173">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="c2aa7-174">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c2aa7-174">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="c2aa7-175">Salva-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c2aa7-175">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="c2aa7-176">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c2aa7-176">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


