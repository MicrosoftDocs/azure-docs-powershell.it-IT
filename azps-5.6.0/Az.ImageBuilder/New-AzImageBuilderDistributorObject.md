---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 3421eec7fa723767db0dc896d0c3c40e7c5cbebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013053"
---
# <span data-ttu-id="e9637-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="e9637-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="e9637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9637-102">SYNOPSIS</span></span>
<span data-ttu-id="e9637-103">Oggetto di distribuzione generico</span><span class="sxs-lookup"><span data-stu-id="e9637-103">Generic distribution object</span></span>

## <span data-ttu-id="e9637-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9637-104">SYNTAX</span></span>

### <span data-ttu-id="e9637-105">ManagedImageDistributor (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e9637-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="e9637-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="e9637-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="e9637-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="e9637-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="e9637-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e9637-108">DESCRIPTION</span></span>
<span data-ttu-id="e9637-109">Oggetto di distribuzione generico</span><span class="sxs-lookup"><span data-stu-id="e9637-109">Generic distribution object</span></span>

## <span data-ttu-id="e9637-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9637-110">EXAMPLES</span></span>

### <span data-ttu-id="e9637-111">Esempio 1: Creare un distributore di immagini gestite</span><span class="sxs-lookup"><span data-stu-id="e9637-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="e9637-112">Questo comando crea un distributore di immagini gestite.</span><span class="sxs-lookup"><span data-stu-id="e9637-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="e9637-113">Esempio 2: Creare un distributore VHD</span><span class="sxs-lookup"><span data-stu-id="e9637-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="e9637-114">Questo comando crea un distributore VHD.</span><span class="sxs-lookup"><span data-stu-id="e9637-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="e9637-115">Esempio 3: Creare un distributore di immagini condiviso</span><span class="sxs-lookup"><span data-stu-id="e9637-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="e9637-116">Questo comando crea un distributore di immagini condiviso.</span><span class="sxs-lookup"><span data-stu-id="e9637-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="e9637-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9637-117">PARAMETERS</span></span>

### <span data-ttu-id="e9637-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="e9637-118">-ArtifactTag</span></span>
<span data-ttu-id="e9637-119">Tag che verranno applicati all'elemento dopo che è stato creato/aggiornato dal distributore.</span><span class="sxs-lookup"><span data-stu-id="e9637-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9637-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="e9637-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="e9637-121">Contrassegno che indica se la versione dell'immagine creata deve essere esclusa dalla versione più recente.</span><span class="sxs-lookup"><span data-stu-id="e9637-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="e9637-122">Ometti di usare il valore predefinito (false).</span><span class="sxs-lookup"><span data-stu-id="e9637-122">Omit to use the default (false).</span></span>

```yaml
Type: System.Boolean
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9637-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="e9637-123">-GalleryImageId</span></span>
<span data-ttu-id="e9637-124">ID risorsa dell'immagine raccolta immagini condivise.</span><span class="sxs-lookup"><span data-stu-id="e9637-124">Resource Id of the Shared Image Gallery image.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9637-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="e9637-125">-ImageId</span></span>
<span data-ttu-id="e9637-126">ID risorsa dell'immagine del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="e9637-126">Resource Id of the Managed Disk Image.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9637-127">-Location</span><span class="sxs-lookup"><span data-stu-id="e9637-127">-Location</span></span>
<span data-ttu-id="e9637-128">La posizione di Azure per l'immagine deve corrispondere se l'immagine esiste già.</span><span class="sxs-lookup"><span data-stu-id="e9637-128">Azure location for the image, should match if image already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9637-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="e9637-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="e9637-130">Distribuisci come immagine disco gestito.</span><span class="sxs-lookup"><span data-stu-id="e9637-130">Distribute as a Managed Disk Image.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9637-131">-ReplicaRegione</span><span class="sxs-lookup"><span data-stu-id="e9637-131">-ReplicationRegion</span></span>
<span data-ttu-id="e9637-132">Elenco di aree geografiche in cui verrà replicata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="e9637-132">A list of regions that the image will be replicated to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9637-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="e9637-133">-RunOutputName</span></span>
<span data-ttu-id="e9637-134">Nome da usare per il runOutput associato.</span><span class="sxs-lookup"><span data-stu-id="e9637-134">The name to be used for the associated RunOutput.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9637-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="e9637-135">-SharedImageDistributor</span></span>
<span data-ttu-id="e9637-136">Distribuisci tramite raccolta immagini condivisa.</span><span class="sxs-lookup"><span data-stu-id="e9637-136">Distribute via Shared Image Gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9637-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e9637-137">-StorageAccountType</span></span>
<span data-ttu-id="e9637-138">Tipo di account di archiviazione da usare per archiviare l'immagine condivisa.</span><span class="sxs-lookup"><span data-stu-id="e9637-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="e9637-139">Ometti di usare il valore predefinito (Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="e9637-139">Omit to use the default (Standard_LRS).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.SharedImageStorageAccountType
Parameter Sets: SharedImageDistributor
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9637-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="e9637-140">-VhdDistributor</span></span>
<span data-ttu-id="e9637-141">Distribuire tramite disco rigido virtuale in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e9637-141">Distribute via VHD in a storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VhdDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9637-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9637-142">CommonParameters</span></span>
<span data-ttu-id="e9637-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9637-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9637-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9637-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9637-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="e9637-145">INPUTS</span></span>

## <span data-ttu-id="e9637-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9637-146">OUTPUTS</span></span>

### <span data-ttu-id="e9637-147">Microsoft.Azure.PowerShell.Cmdlets.ImageMag.Models.Api20200214.IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="e9637-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="e9637-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="e9637-148">NOTES</span></span>

<span data-ttu-id="e9637-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e9637-149">ALIASES</span></span>

## <span data-ttu-id="e9637-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9637-150">RELATED LINKS</span></span>

