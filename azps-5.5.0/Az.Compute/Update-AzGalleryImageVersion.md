---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181534"
---
# <span data-ttu-id="2db49-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2db49-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="2db49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2db49-102">SYNOPSIS</span></span>
<span data-ttu-id="2db49-103">Aggiornare la versione di un'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="2db49-103">Update a gallery image version.</span></span>

## <span data-ttu-id="2db49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2db49-104">SYNTAX</span></span>

### <span data-ttu-id="2db49-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="2db49-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db49-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2db49-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db49-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2db49-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2db49-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2db49-108">DESCRIPTION</span></span>
<span data-ttu-id="2db49-109">Aggiornare la versione di un'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="2db49-109">Update a gallery image version.</span></span>

## <span data-ttu-id="2db49-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2db49-110">EXAMPLES</span></span>

### <span data-ttu-id="2db49-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2db49-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="2db49-112">Aggiornare la versione di un'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="2db49-112">Update a gallery image version.</span></span>

## <span data-ttu-id="2db49-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2db49-113">PARAMETERS</span></span>

### <span data-ttu-id="2db49-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2db49-114">-AsJob</span></span>
<span data-ttu-id="2db49-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2db49-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db49-116">-DefaultProfile</span></span>
<span data-ttu-id="2db49-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2db49-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="2db49-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="2db49-119">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="2db49-119">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="2db49-120">-GalleryName</span></span>
<span data-ttu-id="2db49-121">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="2db49-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2db49-122">-InputObject</span></span>
<span data-ttu-id="2db49-123">Oggetto versione immagine raccolta PS.</span><span class="sxs-lookup"><span data-stu-id="2db49-123">The PS Gallery Image Version Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2db49-124">-Name</span></span>
<span data-ttu-id="2db49-125">Nome della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="2db49-125">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="2db49-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="2db49-127">Data di fine del ciclo di vita della raccolta Immagine Versione.</span><span class="sxs-lookup"><span data-stu-id="2db49-127">The end of life date of the gallery Image Version.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="2db49-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="2db49-129">Se è impostato, le macchine virtuali distribuite dall'ultima versione della definizione dell'immagine non userà questa versione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2db49-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="2db49-130">-ReplicaCount</span></span>
<span data-ttu-id="2db49-131">Numero di replica della versione dell'immagine da creare in base all'area geografica.</span><span class="sxs-lookup"><span data-stu-id="2db49-131">The number of replicas of the Image Version to be created per region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db49-132">-ResourceGroupName</span></span>
<span data-ttu-id="2db49-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2db49-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2db49-134">-ResourceId</span></span>
<span data-ttu-id="2db49-135">ID della risorsa per la versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="2db49-135">The resource ID for the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="2db49-136">-Tag</span></span>
<span data-ttu-id="2db49-137">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="2db49-137">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="2db49-138">-TargetRegion</span></span>
<span data-ttu-id="2db49-139">Le aree di destinazione in cui verrà replicata la versione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2db49-139">The target regions where the Image Version is going to be replicated to.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2db49-140">-Confirm</span></span>
<span data-ttu-id="2db49-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2db49-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db49-142">-WhatIf</span></span>
<span data-ttu-id="2db49-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2db49-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2db49-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2db49-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db49-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db49-145">CommonParameters</span></span>
<span data-ttu-id="2db49-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2db49-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db49-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2db49-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db49-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="2db49-148">INPUTS</span></span>

### <span data-ttu-id="2db49-149">System.String</span><span class="sxs-lookup"><span data-stu-id="2db49-149">System.String</span></span>

### <span data-ttu-id="2db49-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2db49-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="2db49-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2db49-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2db49-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2db49-152">System.Int32</span></span>

### <span data-ttu-id="2db49-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2db49-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2db49-154">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="2db49-154">System.DateTime</span></span>

### <span data-ttu-id="2db49-155">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="2db49-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="2db49-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2db49-156">OUTPUTS</span></span>

### <span data-ttu-id="2db49-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2db49-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="2db49-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="2db49-158">NOTES</span></span>

## <span data-ttu-id="2db49-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2db49-159">RELATED LINKS</span></span>
