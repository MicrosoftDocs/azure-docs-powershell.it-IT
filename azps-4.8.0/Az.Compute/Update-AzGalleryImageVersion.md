---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191026"
---
# <span data-ttu-id="41be6-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="41be6-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="41be6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41be6-102">SYNOPSIS</span></span>
<span data-ttu-id="41be6-103">Aggiornare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="41be6-103">Update a gallery image version.</span></span>

## <span data-ttu-id="41be6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41be6-104">SYNTAX</span></span>

### <span data-ttu-id="41be6-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41be6-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41be6-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="41be6-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41be6-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="41be6-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41be6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41be6-108">DESCRIPTION</span></span>
<span data-ttu-id="41be6-109">Aggiornare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="41be6-109">Update a gallery image version.</span></span>

## <span data-ttu-id="41be6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41be6-110">EXAMPLES</span></span>

### <span data-ttu-id="41be6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="41be6-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="41be6-112">Aggiornare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="41be6-112">Update a gallery image version.</span></span>

## <span data-ttu-id="41be6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41be6-113">PARAMETERS</span></span>

### <span data-ttu-id="41be6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41be6-114">-AsJob</span></span>
<span data-ttu-id="41be6-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="41be6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41be6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41be6-116">-DefaultProfile</span></span>
<span data-ttu-id="41be6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41be6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41be6-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="41be6-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="41be6-119">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="41be6-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="41be6-120">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="41be6-120">-GalleryName</span></span>
<span data-ttu-id="41be6-121">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="41be6-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="41be6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41be6-122">-InputObject</span></span>
<span data-ttu-id="41be6-123">Oggetto versione della raccolta immagini PS.</span><span class="sxs-lookup"><span data-stu-id="41be6-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="41be6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="41be6-124">-Name</span></span>
<span data-ttu-id="41be6-125">Nome della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="41be6-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="41be6-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="41be6-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="41be6-127">Data di fine della durata della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="41be6-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="41be6-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="41be6-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="41be6-129">Se è impostato, le macchine virtuali distribuite dalla versione più recente della definizione di immagine non utilizzeranno questa versione di immagine.</span><span class="sxs-lookup"><span data-stu-id="41be6-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="41be6-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="41be6-130">-ReplicaCount</span></span>
<span data-ttu-id="41be6-131">Numero di repliche della versione di immagine da creare per area geografica.</span><span class="sxs-lookup"><span data-stu-id="41be6-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="41be6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41be6-132">-ResourceGroupName</span></span>
<span data-ttu-id="41be6-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41be6-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="41be6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41be6-134">-ResourceId</span></span>
<span data-ttu-id="41be6-135">ID risorsa per la versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="41be6-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="41be6-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="41be6-136">-Tag</span></span>
<span data-ttu-id="41be6-137">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="41be6-137">Resource tags</span></span>

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

### <span data-ttu-id="41be6-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="41be6-138">-TargetRegion</span></span>
<span data-ttu-id="41be6-139">Aree di destinazione in cui verrà replicata la versione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="41be6-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="41be6-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="41be6-140">-Confirm</span></span>
<span data-ttu-id="41be6-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41be6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41be6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41be6-142">-WhatIf</span></span>
<span data-ttu-id="41be6-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41be6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41be6-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41be6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41be6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41be6-145">CommonParameters</span></span>
<span data-ttu-id="41be6-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41be6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41be6-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41be6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41be6-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41be6-148">INPUTS</span></span>

### <span data-ttu-id="41be6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="41be6-149">System.String</span></span>

### <span data-ttu-id="41be6-150">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="41be6-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="41be6-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="41be6-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="41be6-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="41be6-152">System.Int32</span></span>

### <span data-ttu-id="41be6-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="41be6-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="41be6-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="41be6-154">System.DateTime</span></span>

### <span data-ttu-id="41be6-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="41be6-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="41be6-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41be6-156">OUTPUTS</span></span>

### <span data-ttu-id="41be6-157">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="41be6-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="41be6-158">Note</span><span class="sxs-lookup"><span data-stu-id="41be6-158">NOTES</span></span>

## <span data-ttu-id="41be6-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41be6-159">RELATED LINKS</span></span>