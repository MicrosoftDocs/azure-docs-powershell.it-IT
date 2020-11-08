---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030045"
---
# <span data-ttu-id="53246-101">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="53246-101">Update-AzureVMImage</span></span>

## <span data-ttu-id="53246-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53246-102">SYNOPSIS</span></span>
<span data-ttu-id="53246-103">Aggiorna l'etichetta di un'immagine del sistema operativo nel repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="53246-103">Updates the label of an operating system image in the image repository.</span></span>

## <span data-ttu-id="53246-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53246-104">SYNTAX</span></span>

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="53246-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53246-105">DESCRIPTION</span></span>
<span data-ttu-id="53246-106">Il cmdlet **Update-AzureVMImage** aggiorna l'etichetta su un'immagine del sistema operativo nel repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="53246-106">The **Update-AzureVMImage** cmdlet updates the label on an operating system image in the image repository.</span></span>
<span data-ttu-id="53246-107">Restituisce un oggetto Image con informazioni sull'immagine aggiornata.</span><span class="sxs-lookup"><span data-stu-id="53246-107">It returns an image object with information about the updated image.</span></span>

## <span data-ttu-id="53246-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53246-108">EXAMPLES</span></span>

### <span data-ttu-id="53246-109">Esempio 1: aggiornare un'immagine cambiando l'etichetta dell'immagine</span><span class="sxs-lookup"><span data-stu-id="53246-109">Example 1: Update an image by changing the image label</span></span>
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

<span data-ttu-id="53246-110">Questo comando Aggiorna l'immagine denominata Windows-Server-2008-SP2 modificando l'etichetta dell'immagine in non utilizzare.</span><span class="sxs-lookup"><span data-stu-id="53246-110">This command updates the image named Windows-Server-2008-SP2 by changing the image label to DoNotUse.</span></span>

### <span data-ttu-id="53246-111">Esempio 2: ottenere tutti i sistemi operativi per etichetta e quindi aggiornare l'etichetta</span><span class="sxs-lookup"><span data-stu-id="53246-111">Example 2: Get all operating systems by label and then update the label</span></span>
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

<span data-ttu-id="53246-112">Questo comando consente di ottenere tutte le immagini del sistema operativo etichettate non utilizzare e di modificare l'etichetta in aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="53246-112">This command gets all the operating system images labeled DoNotUse and changes the label to Updated.</span></span>

## <span data-ttu-id="53246-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53246-113">PARAMETERS</span></span>

### <span data-ttu-id="53246-114">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="53246-114">-Description</span></span>
<span data-ttu-id="53246-115">Specifica la descrizione dell'immagine del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="53246-115">Specifies the description of the operating system image.</span></span>

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

### <span data-ttu-id="53246-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="53246-116">-DiskConfig</span></span>
<span data-ttu-id="53246-117">Specifica il disco del sistema operativo e la configurazione del disco dati per l'immagine della macchina virtuale creata usando i cmdlet **New-AzureVMImageDiskConfigSet** , **set-AzureVMImageOSDiskConfig** e **set-AzureVMImageDataDiskConfig** .</span><span class="sxs-lookup"><span data-stu-id="53246-117">Specifies the operating system disk and data disk configuration for the virtual machine image created by using the **New-AzureVMImageDiskConfigSet** , **Set-AzureVMImageOSDiskConfig** , and **Set-AzureVMImageDataDiskConfig** cmdlets.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53246-118">-DontShowInGui</span><span class="sxs-lookup"><span data-stu-id="53246-118">-DontShowInGui</span></span>
<span data-ttu-id="53246-119">Indica che questo cmdlet non Mostra l'immagine nella GUI.</span><span class="sxs-lookup"><span data-stu-id="53246-119">Indicates that this cmdlet does not show the image in the GUI.</span></span>

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

### <span data-ttu-id="53246-120">-EULA</span><span class="sxs-lookup"><span data-stu-id="53246-120">-Eula</span></span>
<span data-ttu-id="53246-121">Specifica il contratto di licenza con l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="53246-121">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="53246-122">È consigliabile che il valore sia un URL.</span><span class="sxs-lookup"><span data-stu-id="53246-122">We recommend that the value is a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53246-123">-IconName</span><span class="sxs-lookup"><span data-stu-id="53246-123">-IconName</span></span>
<span data-ttu-id="53246-124">Specifica il nome dell'icona standard per l'immagine del sistema operativo o della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53246-124">Specifies the standard icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="53246-125">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="53246-125">-ImageFamily</span></span>
<span data-ttu-id="53246-126">Specifica un valore che può essere usato per raggruppare immagini di sistemi operativi o macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="53246-126">Specifies a value that can be used to group operating system or virtual machine images.</span></span>

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

### <span data-ttu-id="53246-127">-ImageName</span><span class="sxs-lookup"><span data-stu-id="53246-127">-ImageName</span></span>
<span data-ttu-id="53246-128">Specifica il nome dell'immagine da aggiornare nel repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="53246-128">Specifies the name of the image to update in the image repository.</span></span>

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

### <span data-ttu-id="53246-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="53246-129">-InformationAction</span></span>
<span data-ttu-id="53246-130">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="53246-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="53246-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="53246-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53246-132">Continuare</span><span class="sxs-lookup"><span data-stu-id="53246-132">Continue</span></span>
- <span data-ttu-id="53246-133">Ignora</span><span class="sxs-lookup"><span data-stu-id="53246-133">Ignore</span></span>
- <span data-ttu-id="53246-134">Informarsi</span><span class="sxs-lookup"><span data-stu-id="53246-134">Inquire</span></span>
- <span data-ttu-id="53246-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="53246-135">SilentlyContinue</span></span>
- <span data-ttu-id="53246-136">Stop</span><span class="sxs-lookup"><span data-stu-id="53246-136">Stop</span></span>
- <span data-ttu-id="53246-137">Sospensione</span><span class="sxs-lookup"><span data-stu-id="53246-137">Suspend</span></span>

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

### <span data-ttu-id="53246-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="53246-138">-InformationVariable</span></span>
<span data-ttu-id="53246-139">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="53246-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="53246-140">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="53246-140">-Label</span></span>
<span data-ttu-id="53246-141">Specifica la nuova etichetta dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="53246-141">Specifies the new label of the image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53246-142">-Lingua</span><span class="sxs-lookup"><span data-stu-id="53246-142">-Language</span></span>
<span data-ttu-id="53246-143">Specifica la lingua per il sistema operativo nella macchina virtuale o nell'immagine del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="53246-143">Specifies the language for the operating system in the virtual machine or operating system image.</span></span>

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

### <span data-ttu-id="53246-144">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="53246-144">-PrivacyUri</span></span>
<span data-ttu-id="53246-145">Specifica l'URI che punta a un documento che contiene i criteri di privacy correlati all'immagine del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="53246-145">Specifies the URI that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53246-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="53246-146">-Profile</span></span>
<span data-ttu-id="53246-147">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53246-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53246-148">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="53246-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53246-149">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="53246-149">-PublishedDate</span></span>
<span data-ttu-id="53246-150">Specifica la data in cui l'immagine del sistema operativo è stata aggiunta al repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="53246-150">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53246-151">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="53246-151">-RecommendedVMSize</span></span>
<span data-ttu-id="53246-152">Specifica le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53246-152">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="53246-153">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="53246-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53246-154">Medio</span><span class="sxs-lookup"><span data-stu-id="53246-154">Medium</span></span>
- <span data-ttu-id="53246-155">Grande</span><span class="sxs-lookup"><span data-stu-id="53246-155">Large</span></span>
- <span data-ttu-id="53246-156">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="53246-156">ExtraLarge</span></span>
- <span data-ttu-id="53246-157">A5</span><span class="sxs-lookup"><span data-stu-id="53246-157">A5</span></span>
- <span data-ttu-id="53246-158">A6</span><span class="sxs-lookup"><span data-stu-id="53246-158">A6</span></span>
- <span data-ttu-id="53246-159">A7</span><span class="sxs-lookup"><span data-stu-id="53246-159">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53246-160">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="53246-160">-SmallIconName</span></span>
<span data-ttu-id="53246-161">Specifica il nome dell'icona piccola per il sistema operativo o l'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53246-161">Specifies the small icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="53246-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53246-162">CommonParameters</span></span>
<span data-ttu-id="53246-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53246-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53246-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53246-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53246-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53246-165">INPUTS</span></span>

## <span data-ttu-id="53246-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53246-166">OUTPUTS</span></span>

### <span data-ttu-id="53246-167">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="53246-167">OSImageContext</span></span>

## <span data-ttu-id="53246-168">Note</span><span class="sxs-lookup"><span data-stu-id="53246-168">NOTES</span></span>

## <span data-ttu-id="53246-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53246-169">RELATED LINKS</span></span>

[<span data-ttu-id="53246-170">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="53246-170">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="53246-171">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="53246-171">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="53246-172">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="53246-172">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="53246-173">Salva-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="53246-173">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="53246-174">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="53246-174">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="53246-175">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="53246-175">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="53246-176">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="53246-176">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


