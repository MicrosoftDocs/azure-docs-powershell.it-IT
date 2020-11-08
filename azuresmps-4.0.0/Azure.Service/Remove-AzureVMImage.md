---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029916"
---
# <span data-ttu-id="34f40-101">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="34f40-101">Remove-AzureVMImage</span></span>

## <span data-ttu-id="34f40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34f40-102">SYNOPSIS</span></span>
<span data-ttu-id="34f40-103">Rimuove un'immagine del sistema operativo dal repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="34f40-103">Removes an operating system image from the image repository.</span></span>

## <span data-ttu-id="34f40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34f40-104">SYNTAX</span></span>

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="34f40-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34f40-105">DESCRIPTION</span></span>
<span data-ttu-id="34f40-106">Il cmdlet **Remove-AzureVMImage** rimuove un'immagine del sistema operativo dal repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="34f40-106">The **Remove-AzureVMImage** cmdlet removes an operating system image from the image repository.</span></span>
<span data-ttu-id="34f40-107">Per impostazione predefinita, questo cmdlet non elimina il BLOB di immagini fisiche associato dall'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="34f40-107">By default, this cmdlet does not delete the associated physical image blob from the storage account.</span></span>
<span data-ttu-id="34f40-108">Per eliminare il disco rigido virtuale associato (VHD), usare il parametro **DeleteVHD** .</span><span class="sxs-lookup"><span data-stu-id="34f40-108">To delete the associated virtual hard drive (VHD), use the **DeleteVHD** parameter.</span></span>

## <span data-ttu-id="34f40-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34f40-109">EXAMPLES</span></span>

### <span data-ttu-id="34f40-110">Esempio 1: rimuovere un'immagine dal repository di immagini</span><span class="sxs-lookup"><span data-stu-id="34f40-110">Example 1: Remove an image from the image repository</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

<span data-ttu-id="34f40-111">Questo comando rimuove l'immagine denominata Image001 dal repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="34f40-111">This command removes the image named Image001 from the image repository.</span></span>

### <span data-ttu-id="34f40-112">Esempio 2: rimuovere un'immagine dal repository di immagini e anche dal VHD</span><span class="sxs-lookup"><span data-stu-id="34f40-112">Example 2: Remove an image from the image repository and also the VHD</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

<span data-ttu-id="34f40-113">Questo comando rimuove l'immagine denominata Image001 dal repository di immagini ed elimina anche l'immagine del VHD fisico dall'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="34f40-113">This command removes the image named Image001 from the image repository and also deletes the physical VHD image from the storage account.</span></span>

### <span data-ttu-id="34f40-114">Esempio 3: impostare un contesto di sottoscrizione e quindi rimuovere tutte le immagini</span><span class="sxs-lookup"><span data-stu-id="34f40-114">Example 3: Set a subscription context and then remove all the images</span></span>
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

<span data-ttu-id="34f40-115">Questo comando imposta il contesto di sottoscrizione e quindi rimuove tutte le immagini dal repository di immagini la cui etichetta include il nome beta.</span><span class="sxs-lookup"><span data-stu-id="34f40-115">This command sets the subscription context and then removes all the images from the image repository whose Label includes the name Beta.</span></span>

## <span data-ttu-id="34f40-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34f40-116">PARAMETERS</span></span>

### <span data-ttu-id="34f40-117">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="34f40-117">-DeleteVHD</span></span>
<span data-ttu-id="34f40-118">Indica che questo cmdlet elimina il BLOB di immagine del VHD fisico dall'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="34f40-118">Indicates that this cmdlet deletes the physical VHD image blob from the storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f40-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="34f40-119">-ImageName</span></span>
<span data-ttu-id="34f40-120">Specifica il sistema operativo o l'immagine della macchina virtuale da rimuovere dal repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="34f40-120">Specifies the operating system or virtual machine image to remove from the image repository.</span></span>

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

### <span data-ttu-id="34f40-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="34f40-121">-InformationAction</span></span>
<span data-ttu-id="34f40-122">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="34f40-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="34f40-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="34f40-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="34f40-124">Continuare</span><span class="sxs-lookup"><span data-stu-id="34f40-124">Continue</span></span>
- <span data-ttu-id="34f40-125">Ignora</span><span class="sxs-lookup"><span data-stu-id="34f40-125">Ignore</span></span>
- <span data-ttu-id="34f40-126">Informarsi</span><span class="sxs-lookup"><span data-stu-id="34f40-126">Inquire</span></span>
- <span data-ttu-id="34f40-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="34f40-127">SilentlyContinue</span></span>
- <span data-ttu-id="34f40-128">Stop</span><span class="sxs-lookup"><span data-stu-id="34f40-128">Stop</span></span>
- <span data-ttu-id="34f40-129">Sospensione</span><span class="sxs-lookup"><span data-stu-id="34f40-129">Suspend</span></span>

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

### <span data-ttu-id="34f40-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="34f40-130">-InformationVariable</span></span>
<span data-ttu-id="34f40-131">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="34f40-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="34f40-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="34f40-132">-Profile</span></span>
<span data-ttu-id="34f40-133">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f40-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="34f40-134">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="34f40-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34f40-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f40-135">CommonParameters</span></span>
<span data-ttu-id="34f40-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34f40-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f40-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34f40-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f40-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34f40-138">INPUTS</span></span>

## <span data-ttu-id="34f40-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34f40-139">OUTPUTS</span></span>

## <span data-ttu-id="34f40-140">Note</span><span class="sxs-lookup"><span data-stu-id="34f40-140">NOTES</span></span>

## <span data-ttu-id="34f40-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34f40-141">RELATED LINKS</span></span>

[<span data-ttu-id="34f40-142">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="34f40-142">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="34f40-143">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="34f40-143">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="34f40-144">Salva-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="34f40-144">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="34f40-145">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="34f40-145">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


