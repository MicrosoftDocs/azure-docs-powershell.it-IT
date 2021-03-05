---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: a106435739d7e4ec358038be476cc3f2ba8cd09d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013038"
---
# <span data-ttu-id="4028e-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="4028e-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="4028e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4028e-102">SYNOPSIS</span></span>
<span data-ttu-id="4028e-103">Descrive un'origine immagine di una macchina virtuale per la creazione, la personalizzazione e la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4028e-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="4028e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4028e-104">SYNTAX</span></span>

### <span data-ttu-id="4028e-105">ManagedImage (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4028e-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="4028e-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="4028e-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="4028e-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="4028e-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4028e-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="4028e-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="4028e-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4028e-109">DESCRIPTION</span></span>
<span data-ttu-id="4028e-110">Descrive un'origine immagine di una macchina virtuale per la creazione, la personalizzazione e la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4028e-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="4028e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4028e-111">EXAMPLES</span></span>

### <span data-ttu-id="4028e-112">Esempio 1: Creare un'origine immagine gestita</span><span class="sxs-lookup"><span data-stu-id="4028e-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="4028e-113">Questo comando crea un'origine immagine gestita.</span><span class="sxs-lookup"><span data-stu-id="4028e-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="4028e-114">Esempio 2: Creare un'origine immagine condivisa</span><span class="sxs-lookup"><span data-stu-id="4028e-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="4028e-115">Questo comando crea un'origine immagine condivisa.</span><span class="sxs-lookup"><span data-stu-id="4028e-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="4028e-116">Esempio 3: Creare un elemento da un'origine immagine</span><span class="sxs-lookup"><span data-stu-id="4028e-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="4028e-117">Questo comando crea una platfrom origine dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="4028e-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="4028e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4028e-118">PARAMETERS</span></span>

### <span data-ttu-id="4028e-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="4028e-119">-ImageId</span></span>
<span data-ttu-id="4028e-120">ARM ID risorsa dell'immagine gestita nella sottoscrizione del cliente.</span><span class="sxs-lookup"><span data-stu-id="4028e-120">ARM resource id of the managed image in customer subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4028e-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="4028e-121">-ImageVersionId</span></span>
<span data-ttu-id="4028e-122">ARM ID risorsa della versione dell'immagine nella raccolta immagini condivisa.</span><span class="sxs-lookup"><span data-stu-id="4028e-122">ARM resource id of the image version in the shared image gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4028e-123">-Offerta</span><span class="sxs-lookup"><span data-stu-id="4028e-123">-Offer</span></span>
<span data-ttu-id="4028e-124">Offerta di immagini dalla [Raccolta immagini di Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="4028e-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4028e-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="4028e-125">-PlanName</span></span>
<span data-ttu-id="4028e-126">Nome del piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="4028e-126">Name of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4028e-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="4028e-127">-PlanProduct</span></span>
<span data-ttu-id="4028e-128">Prodotto del piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="4028e-128">Product of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4028e-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="4028e-129">-PlanPublisher</span></span>
<span data-ttu-id="4028e-130">Autore del piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="4028e-130">Publisher of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4028e-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4028e-131">-Publisher</span></span>
<span data-ttu-id="4028e-132">Image Publisher in [Azure Gallery Images.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="4028e-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4028e-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="4028e-133">-Sku</span></span>
<span data-ttu-id="4028e-134">SKU immagine da [Immagini raccolta Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="4028e-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4028e-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="4028e-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="4028e-136">Descrive un'origine immagine, che è un'immagine gestita nella sottoscrizione del cliente.</span><span class="sxs-lookup"><span data-stu-id="4028e-136">Describes an image source that is a managed image in customer subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4028e-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="4028e-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="4028e-138">Descrive un'origine immagine dalle [immagini della Raccolta di Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="4028e-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4028e-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="4028e-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="4028e-140">Descrive un'origine immagine che rappresenta una versione di immagine in una raccolta immagini condivisa.</span><span class="sxs-lookup"><span data-stu-id="4028e-140">Describes an image source that is an image version in a shared image gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4028e-141">-Version</span><span class="sxs-lookup"><span data-stu-id="4028e-141">-Version</span></span>
<span data-ttu-id="4028e-142">Versione dell'immagine da [Immagini della Raccolta di Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="4028e-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4028e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4028e-143">CommonParameters</span></span>
<span data-ttu-id="4028e-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4028e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4028e-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4028e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4028e-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="4028e-146">INPUTS</span></span>

## <span data-ttu-id="4028e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4028e-147">OUTPUTS</span></span>

### <span data-ttu-id="4028e-148">Microsoft.Azure.PowerShell.Cmdlets.ImageMag.Models.Api20200214.IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="4028e-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="4028e-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="4028e-149">NOTES</span></span>

<span data-ttu-id="4028e-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4028e-150">ALIASES</span></span>

## <span data-ttu-id="4028e-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4028e-151">RELATED LINKS</span></span>

