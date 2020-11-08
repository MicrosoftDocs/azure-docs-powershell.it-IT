---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029994"
---
# <span data-ttu-id="dbe27-101">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="dbe27-101">Get-AzureVMImage</span></span>

## <span data-ttu-id="dbe27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbe27-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe27-103">Ottiene le proprietà in uno o un elenco di sistemi operativi o un'immagine della macchina virtuale nel repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="dbe27-103">Gets the properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>

## <span data-ttu-id="dbe27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbe27-104">SYNTAX</span></span>

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dbe27-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbe27-105">DESCRIPTION</span></span>
<span data-ttu-id="dbe27-106">Il cmdlet **Get-AzureVMImage** ottiene le proprietà in uno o un elenco di sistemi operativi o un'immagine della macchina virtuale nel repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="dbe27-106">The **Get-AzureVMImage** cmdlet gets properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>
<span data-ttu-id="dbe27-107">Il cmdlet restituisce informazioni per tutte le immagini del repository o su un'immagine specifica se è disponibile il nome dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="dbe27-107">The cmdlet returns information for all images in the repository, or about a specific image if its image name is provided.</span></span>

## <span data-ttu-id="dbe27-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbe27-108">EXAMPLES</span></span>

### <span data-ttu-id="dbe27-109">Esempio 1: ottenere un oggetto immagine specifico dal repository di immagini corrente.</span><span class="sxs-lookup"><span data-stu-id="dbe27-109">Example 1: Get a specific image object from the current image repository.</span></span>
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

<span data-ttu-id="dbe27-110">Questo comando ottiene l'oggetto Image denominato Image001 dal repository di immagini corrente.</span><span class="sxs-lookup"><span data-stu-id="dbe27-110">This command gets the image object named Image001 from the current image repository.</span></span>

### <span data-ttu-id="dbe27-111">Esempio 2: ottenere tutte le immagini dal repository di immagini corrente</span><span class="sxs-lookup"><span data-stu-id="dbe27-111">Example 2: Get all images from the current image repository</span></span>
```
PS C:\> Get-AzureVMImage
```

<span data-ttu-id="dbe27-112">Questo comando recupera tutte le immagini dal repository di immagini corrente.</span><span class="sxs-lookup"><span data-stu-id="dbe27-112">This command retrieves all the images from the current image repository.</span></span>

### <span data-ttu-id="dbe27-113">Esempio 3: impostare il contesto dell'abbonamento e quindi ottenere tutte le immagini</span><span class="sxs-lookup"><span data-stu-id="dbe27-113">Example 3: Set the subscription context and then get all the images</span></span>
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

<span data-ttu-id="dbe27-114">Questo comando imposta il contesto di sottoscrizione e recupera tutte le immagini dal repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="dbe27-114">This command sets the subscription context and then retrieves all the images from the image repository.</span></span>

## <span data-ttu-id="dbe27-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbe27-115">PARAMETERS</span></span>

### <span data-ttu-id="dbe27-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="dbe27-116">-ImageName</span></span>
<span data-ttu-id="dbe27-117">Specifica il nome del sistema operativo o dell'immagine della macchina virtuale nel repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="dbe27-117">Specifies the name of the operating system or virtual machine image in the image repository.</span></span>
<span data-ttu-id="dbe27-118">Se non specifichi questo parametro, vengono restituite tutte le immagini.</span><span class="sxs-lookup"><span data-stu-id="dbe27-118">If you do not specify this parameter, all the images are returned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbe27-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dbe27-119">-InformationAction</span></span>
<span data-ttu-id="dbe27-120">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="dbe27-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dbe27-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbe27-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dbe27-122">Continuare</span><span class="sxs-lookup"><span data-stu-id="dbe27-122">Continue</span></span>
- <span data-ttu-id="dbe27-123">Ignora</span><span class="sxs-lookup"><span data-stu-id="dbe27-123">Ignore</span></span>
- <span data-ttu-id="dbe27-124">Informarsi</span><span class="sxs-lookup"><span data-stu-id="dbe27-124">Inquire</span></span>
- <span data-ttu-id="dbe27-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dbe27-125">SilentlyContinue</span></span>
- <span data-ttu-id="dbe27-126">Stop</span><span class="sxs-lookup"><span data-stu-id="dbe27-126">Stop</span></span>
- <span data-ttu-id="dbe27-127">Sospensione</span><span class="sxs-lookup"><span data-stu-id="dbe27-127">Suspend</span></span>

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

### <span data-ttu-id="dbe27-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dbe27-128">-InformationVariable</span></span>
<span data-ttu-id="dbe27-129">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="dbe27-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dbe27-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="dbe27-130">-Profile</span></span>
<span data-ttu-id="dbe27-131">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbe27-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dbe27-132">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="dbe27-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dbe27-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe27-133">CommonParameters</span></span>
<span data-ttu-id="dbe27-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbe27-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe27-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbe27-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe27-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbe27-136">INPUTS</span></span>

## <span data-ttu-id="dbe27-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbe27-137">OUTPUTS</span></span>

## <span data-ttu-id="dbe27-138">Note</span><span class="sxs-lookup"><span data-stu-id="dbe27-138">NOTES</span></span>

## <span data-ttu-id="dbe27-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbe27-139">RELATED LINKS</span></span>

[<span data-ttu-id="dbe27-140">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="dbe27-140">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="dbe27-141">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="dbe27-141">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="dbe27-142">Salva-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="dbe27-142">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="dbe27-143">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="dbe27-143">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


