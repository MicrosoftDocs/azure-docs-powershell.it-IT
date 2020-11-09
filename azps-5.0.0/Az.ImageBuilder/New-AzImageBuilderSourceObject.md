---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296268"
---
# <span data-ttu-id="bd514-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="bd514-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="bd514-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd514-102">SYNOPSIS</span></span>
<span data-ttu-id="bd514-103">Descrive un'origine di immagine della macchina virtuale per la creazione, la personalizzazione e la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="bd514-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="bd514-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd514-104">SYNTAX</span></span>

### <span data-ttu-id="bd514-105">ManagedImage (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bd514-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="bd514-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="bd514-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="bd514-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="bd514-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd514-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="bd514-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="bd514-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd514-109">DESCRIPTION</span></span>
<span data-ttu-id="bd514-110">Descrive un'origine di immagine della macchina virtuale per la creazione, la personalizzazione e la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="bd514-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="bd514-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd514-111">EXAMPLES</span></span>

### <span data-ttu-id="bd514-112">Esempio 1: creare un'origine immagine gestita</span><span class="sxs-lookup"><span data-stu-id="bd514-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="bd514-113">Questo comando crea una fonte di immagine gestita.</span><span class="sxs-lookup"><span data-stu-id="bd514-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="bd514-114">Esempio 2: creare un'origine di immagine condivisa</span><span class="sxs-lookup"><span data-stu-id="bd514-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="bd514-115">Questo comando crea un'origine di immagine condivisa.</span><span class="sxs-lookup"><span data-stu-id="bd514-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="bd514-116">Esempio 3: creare un'origine di immagine platfrom</span><span class="sxs-lookup"><span data-stu-id="bd514-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="bd514-117">Questo comando crea un'origine di immagine platfrom.</span><span class="sxs-lookup"><span data-stu-id="bd514-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="bd514-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd514-118">PARAMETERS</span></span>

### <span data-ttu-id="bd514-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="bd514-119">-ImageId</span></span>
<span data-ttu-id="bd514-120">ID risorsa ARM dell'immagine gestita nell'abbonamento al cliente.</span><span class="sxs-lookup"><span data-stu-id="bd514-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="bd514-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="bd514-121">-ImageVersionId</span></span>
<span data-ttu-id="bd514-122">ID risorsa ARM della versione immagine nella raccolta immagini condivise.</span><span class="sxs-lookup"><span data-stu-id="bd514-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="bd514-123">-Offerta</span><span class="sxs-lookup"><span data-stu-id="bd514-123">-Offer</span></span>
<span data-ttu-id="bd514-124">Immagine offerta dalle [Immagini della raccolta di Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="bd514-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="bd514-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="bd514-125">-PlanName</span></span>
<span data-ttu-id="bd514-126">Nome del piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="bd514-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="bd514-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="bd514-127">-PlanProduct</span></span>
<span data-ttu-id="bd514-128">Prodotto del piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="bd514-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="bd514-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="bd514-129">-PlanPublisher</span></span>
<span data-ttu-id="bd514-130">Publisher del piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="bd514-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="bd514-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="bd514-131">-Publisher</span></span>
<span data-ttu-id="bd514-132">Immagine di Publisher nelle [Immagini della raccolta di Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="bd514-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="bd514-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="bd514-133">-Sku</span></span>
<span data-ttu-id="bd514-134">SKU immagine dalle [Immagini della raccolta di Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="bd514-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="bd514-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="bd514-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="bd514-136">Descrive un'origine immagine che rappresenta un'immagine gestita nell'abbonamento al cliente.</span><span class="sxs-lookup"><span data-stu-id="bd514-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="bd514-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="bd514-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="bd514-138">Descrive un'origine immagini dalle [Immagini della raccolta di Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="bd514-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="bd514-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="bd514-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="bd514-140">Descrive un'origine immagini che è una versione di immagine in una raccolta di immagini condivise.</span><span class="sxs-lookup"><span data-stu-id="bd514-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="bd514-141">-Versione</span><span class="sxs-lookup"><span data-stu-id="bd514-141">-Version</span></span>
<span data-ttu-id="bd514-142">Versione immagine dalle [Immagini della raccolta di Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="bd514-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="bd514-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd514-143">CommonParameters</span></span>
<span data-ttu-id="bd514-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd514-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd514-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd514-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd514-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd514-146">INPUTS</span></span>

## <span data-ttu-id="bd514-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd514-147">OUTPUTS</span></span>

### <span data-ttu-id="bd514-148">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="bd514-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="bd514-149">Note</span><span class="sxs-lookup"><span data-stu-id="bd514-149">NOTES</span></span>

<span data-ttu-id="bd514-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bd514-150">ALIASES</span></span>

## <span data-ttu-id="bd514-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd514-151">RELATED LINKS</span></span>

