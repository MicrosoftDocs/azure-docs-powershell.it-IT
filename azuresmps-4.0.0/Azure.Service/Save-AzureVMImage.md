---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A1CE31E-0158-441E-BC2D-B5D21C9D9421
online version: ''
schema: 2.0.0
ms.openlocfilehash: a956aa7eaf383b0cf5cdb20b39d2f6b54e292f92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023409"
---
# <span data-ttu-id="7ae69-101">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7ae69-101">Save-AzureVMImage</span></span>

## <span data-ttu-id="7ae69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ae69-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae69-103">Acquisisce e salva l'immagine di una macchina virtuale di Azure arrestata.</span><span class="sxs-lookup"><span data-stu-id="7ae69-103">Captures and saves the image of a stopped Azure virtual machine.</span></span>

## <span data-ttu-id="7ae69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ae69-104">SYNTAX</span></span>

```
Save-AzureVMImage [-ServiceName] <String> [-Name] <String> [-ImageName] <String> [[-ImageLabel] <String>]
 [[-OSState] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7ae69-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ae69-105">DESCRIPTION</span></span>
<span data-ttu-id="7ae69-106">Il cmdlet **Save-AzureVMImage** acquisisce e salva l'immagine di una macchina virtuale di Azure arrestata.</span><span class="sxs-lookup"><span data-stu-id="7ae69-106">The **Save-AzureVMImage** cmdlet captures and saves the image of a stopped Azure virtual machine.</span></span>
<span data-ttu-id="7ae69-107">Per le macchine virtuali Windows, eseguire lo strumento Sysprep per preparare l'immagine prima che venga acquisita.</span><span class="sxs-lookup"><span data-stu-id="7ae69-107">For Windows virtual machines, run the Sysprep tool to prepare the image before it is captured.</span></span>
<span data-ttu-id="7ae69-108">Una volta acquisita l'immagine, la macchina virtuale viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="7ae69-108">After the image is captured, the virtual machine is deleted.</span></span>

## <span data-ttu-id="7ae69-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ae69-109">EXAMPLES</span></span>

### <span data-ttu-id="7ae69-110">Esempio 1: salvare una macchina virtuale esistente e quindi eliminarla da una distribuzione</span><span class="sxs-lookup"><span data-stu-id="7ae69-110">Example 1: Save an existing virtual machine and then delete it from a deployment</span></span>
```
PS C:\> Save-AzureVMImage -ServiceName "MyService" -Name "MyVM" -NewImageName "MyBaseImage" -NewImageLabel "MyBaseVM"
```

<span data-ttu-id="7ae69-111">Questo comando acquisisce una macchina virtuale esistente e la Elimina dalla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7ae69-111">This command captures an existing virtual machine and deletes it from the deployment.</span></span>

## <span data-ttu-id="7ae69-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ae69-112">PARAMETERS</span></span>

### <span data-ttu-id="7ae69-113">-ImageLabel</span><span class="sxs-lookup"><span data-stu-id="7ae69-113">-ImageLabel</span></span>
<span data-ttu-id="7ae69-114">Specifica l'etichetta dell'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7ae69-114">Specifies the label of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageLabel

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae69-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="7ae69-115">-ImageName</span></span>
<span data-ttu-id="7ae69-116">Specifica il nome dell'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7ae69-116">Specifies the name of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae69-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7ae69-117">-InformationAction</span></span>
<span data-ttu-id="7ae69-118">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="7ae69-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7ae69-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ae69-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7ae69-120">Continuare</span><span class="sxs-lookup"><span data-stu-id="7ae69-120">Continue</span></span>
- <span data-ttu-id="7ae69-121">Ignora</span><span class="sxs-lookup"><span data-stu-id="7ae69-121">Ignore</span></span>
- <span data-ttu-id="7ae69-122">Informarsi</span><span class="sxs-lookup"><span data-stu-id="7ae69-122">Inquire</span></span>
- <span data-ttu-id="7ae69-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7ae69-123">SilentlyContinue</span></span>
- <span data-ttu-id="7ae69-124">Stop</span><span class="sxs-lookup"><span data-stu-id="7ae69-124">Stop</span></span>
- <span data-ttu-id="7ae69-125">Sospensione</span><span class="sxs-lookup"><span data-stu-id="7ae69-125">Suspend</span></span>

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

### <span data-ttu-id="7ae69-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7ae69-126">-InformationVariable</span></span>
<span data-ttu-id="7ae69-127">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="7ae69-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7ae69-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ae69-128">-Name</span></span>
<span data-ttu-id="7ae69-129">Specifica il nome della macchina virtuale di origine.</span><span class="sxs-lookup"><span data-stu-id="7ae69-129">Specifies the name of the source virtual machine.</span></span>

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

### <span data-ttu-id="7ae69-130">-OSState</span><span class="sxs-lookup"><span data-stu-id="7ae69-130">-OSState</span></span>
<span data-ttu-id="7ae69-131">Specifica lo stato del sistema operativo per l'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7ae69-131">Specifies the operation system state for the virtual machine image.</span></span>
<span data-ttu-id="7ae69-132">Usa questo parametro se intendi acquisire un'immagine della macchina virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae69-132">Use this parameter if you intend to capture a virtual machine image to Azure.</span></span>

<span data-ttu-id="7ae69-133">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="7ae69-133">Valid values are:</span></span>

- <span data-ttu-id="7ae69-134">Generalizzata</span><span class="sxs-lookup"><span data-stu-id="7ae69-134">Generalized</span></span>
- <span data-ttu-id="7ae69-135">Specializzata</span><span class="sxs-lookup"><span data-stu-id="7ae69-135">Specialized</span></span>

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

### <span data-ttu-id="7ae69-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="7ae69-136">-Profile</span></span>
<span data-ttu-id="7ae69-137">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ae69-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7ae69-138">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="7ae69-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7ae69-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7ae69-139">-ServiceName</span></span>
<span data-ttu-id="7ae69-140">Specifica il nome del servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae69-140">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="7ae69-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae69-141">CommonParameters</span></span>
<span data-ttu-id="7ae69-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae69-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae69-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae69-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae69-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ae69-144">INPUTS</span></span>

## <span data-ttu-id="7ae69-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ae69-145">OUTPUTS</span></span>

## <span data-ttu-id="7ae69-146">Note</span><span class="sxs-lookup"><span data-stu-id="7ae69-146">NOTES</span></span>

## <span data-ttu-id="7ae69-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ae69-147">RELATED LINKS</span></span>

[<span data-ttu-id="7ae69-148">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7ae69-148">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="7ae69-149">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7ae69-149">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="7ae69-150">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7ae69-150">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="7ae69-151">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7ae69-151">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


