---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473781"
---
# <span data-ttu-id="58fbc-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="58fbc-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="58fbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="58fbc-103">Descrive un'origine di immagine della macchina virtuale per la creazione, la personalizzazione e la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="58fbc-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="58fbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58fbc-104">SYNTAX</span></span>

### <span data-ttu-id="58fbc-105">ManagedImage (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58fbc-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="58fbc-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="58fbc-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="58fbc-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="58fbc-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="58fbc-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="58fbc-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="58fbc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58fbc-109">DESCRIPTION</span></span>
<span data-ttu-id="58fbc-110">Descrive un'origine di immagine della macchina virtuale per la creazione, la personalizzazione e la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="58fbc-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="58fbc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58fbc-111">EXAMPLES</span></span>

### <span data-ttu-id="58fbc-112">Esempio 1: creare un'origine immagine gestita</span><span class="sxs-lookup"><span data-stu-id="58fbc-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="58fbc-113">Questo comando crea una fonte di immagine gestita.</span><span class="sxs-lookup"><span data-stu-id="58fbc-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="58fbc-114">Esempio 2: creare un'origine di immagine condivisa</span><span class="sxs-lookup"><span data-stu-id="58fbc-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="58fbc-115">Questo comando crea un'origine di immagine condivisa.</span><span class="sxs-lookup"><span data-stu-id="58fbc-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="58fbc-116">Esempio 3: creare un'origine di immagine platfrom</span><span class="sxs-lookup"><span data-stu-id="58fbc-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="58fbc-117">Questo comando crea un'origine di immagine platfrom.</span><span class="sxs-lookup"><span data-stu-id="58fbc-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="58fbc-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58fbc-118">PARAMETERS</span></span>

### <span data-ttu-id="58fbc-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="58fbc-119">-ImageId</span></span>
<span data-ttu-id="58fbc-120">ID risorsa ARM dell'immagine gestita nell'abbonamento al cliente.</span><span class="sxs-lookup"><span data-stu-id="58fbc-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="58fbc-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="58fbc-121">-ImageVersionId</span></span>
<span data-ttu-id="58fbc-122">ID risorsa ARM della versione immagine nella raccolta immagini condivise.</span><span class="sxs-lookup"><span data-stu-id="58fbc-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="58fbc-123">-Offerta</span><span class="sxs-lookup"><span data-stu-id="58fbc-123">-Offer</span></span>
<span data-ttu-id="58fbc-124">Immagine offerta dalle [Immagini della raccolta di Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="58fbc-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="58fbc-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="58fbc-125">-PlanName</span></span>
<span data-ttu-id="58fbc-126">Nome del piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="58fbc-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="58fbc-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="58fbc-127">-PlanProduct</span></span>
<span data-ttu-id="58fbc-128">Prodotto del piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="58fbc-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="58fbc-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="58fbc-129">-PlanPublisher</span></span>
<span data-ttu-id="58fbc-130">Publisher del piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="58fbc-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="58fbc-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="58fbc-131">-Publisher</span></span>
<span data-ttu-id="58fbc-132">Immagine di Publisher nelle [Immagini della raccolta di Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="58fbc-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="58fbc-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="58fbc-133">-Sku</span></span>
<span data-ttu-id="58fbc-134">SKU immagine dalle [Immagini della raccolta di Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="58fbc-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="58fbc-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="58fbc-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="58fbc-136">Descrive un'origine immagine che rappresenta un'immagine gestita nell'abbonamento al cliente.</span><span class="sxs-lookup"><span data-stu-id="58fbc-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="58fbc-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="58fbc-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="58fbc-138">Descrive un'origine immagini dalle [Immagini della raccolta di Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="58fbc-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="58fbc-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="58fbc-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="58fbc-140">Descrive un'origine immagini che è una versione di immagine in una raccolta di immagini condivise.</span><span class="sxs-lookup"><span data-stu-id="58fbc-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="58fbc-141">-Versione</span><span class="sxs-lookup"><span data-stu-id="58fbc-141">-Version</span></span>
<span data-ttu-id="58fbc-142">Versione immagine dalle [Immagini della raccolta di Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="58fbc-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="58fbc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58fbc-143">CommonParameters</span></span>
<span data-ttu-id="58fbc-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58fbc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58fbc-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58fbc-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58fbc-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58fbc-146">INPUTS</span></span>

## <span data-ttu-id="58fbc-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58fbc-147">OUTPUTS</span></span>

### <span data-ttu-id="58fbc-148">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="58fbc-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="58fbc-149">Note</span><span class="sxs-lookup"><span data-stu-id="58fbc-149">NOTES</span></span>

<span data-ttu-id="58fbc-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="58fbc-150">ALIASES</span></span>

## <span data-ttu-id="58fbc-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58fbc-151">RELATED LINKS</span></span>

