---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: d258c561a4c9c8a0baa5a233f8ff55439b5b357d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684665"
---
# <span data-ttu-id="6ecab-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="6ecab-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="6ecab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ecab-102">SYNOPSIS</span></span>
<span data-ttu-id="6ecab-103">Aggiornare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="6ecab-103">Update a gallery image version.</span></span>

## <span data-ttu-id="6ecab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ecab-104">SYNTAX</span></span>

### <span data-ttu-id="6ecab-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ecab-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-Tag <Hashtable>] [-ReplicaCount <Int32>]
 [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ecab-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6ecab-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-Tag <Hashtable>] [-ReplicaCount <Int32>]
 [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ecab-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="6ecab-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob] [-Tag <Hashtable>]
 [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ecab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ecab-108">DESCRIPTION</span></span>
<span data-ttu-id="6ecab-109">Aggiornare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="6ecab-109">Update a gallery image version.</span></span>

## <span data-ttu-id="6ecab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ecab-110">EXAMPLES</span></span>

### <span data-ttu-id="6ecab-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ecab-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="6ecab-112">Aggiornare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="6ecab-112">Update a gallery image version.</span></span>

## <span data-ttu-id="6ecab-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ecab-113">PARAMETERS</span></span>

### <span data-ttu-id="6ecab-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ecab-114">-AsJob</span></span>
<span data-ttu-id="6ecab-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6ecab-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ecab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ecab-116">-DefaultProfile</span></span>
<span data-ttu-id="6ecab-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ecab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ecab-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6ecab-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="6ecab-119">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="6ecab-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="6ecab-120">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="6ecab-120">-GalleryName</span></span>
<span data-ttu-id="6ecab-121">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="6ecab-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="6ecab-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ecab-122">-InputObject</span></span>
<span data-ttu-id="6ecab-123">Oggetto versione della raccolta immagini PS.</span><span class="sxs-lookup"><span data-stu-id="6ecab-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="6ecab-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ecab-124">-Name</span></span>
<span data-ttu-id="6ecab-125">Nome della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="6ecab-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="6ecab-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="6ecab-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="6ecab-127">Data di fine della durata della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="6ecab-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="6ecab-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="6ecab-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="6ecab-129">Se è impostato, le macchine virtuali distribuite dalla versione più recente della definizione di immagine non utilizzeranno questa versione di immagine.</span><span class="sxs-lookup"><span data-stu-id="6ecab-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="6ecab-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="6ecab-130">-ReplicaCount</span></span>
<span data-ttu-id="6ecab-131">Numero di repliche della versione di immagine da creare per area geografica.</span><span class="sxs-lookup"><span data-stu-id="6ecab-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="6ecab-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ecab-132">-ResourceGroupName</span></span>
<span data-ttu-id="6ecab-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6ecab-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="6ecab-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ecab-134">-ResourceId</span></span>
<span data-ttu-id="6ecab-135">ID risorsa per la versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="6ecab-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="6ecab-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ecab-136">-Tag</span></span>
<span data-ttu-id="6ecab-137">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="6ecab-137">Resource tags</span></span>

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

### <span data-ttu-id="6ecab-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="6ecab-138">-TargetRegion</span></span>
<span data-ttu-id="6ecab-139">Aree di destinazione in cui verrà replicata la versione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="6ecab-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="6ecab-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ecab-140">-Confirm</span></span>
<span data-ttu-id="6ecab-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ecab-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ecab-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ecab-142">-WhatIf</span></span>
<span data-ttu-id="6ecab-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ecab-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ecab-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ecab-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ecab-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ecab-145">CommonParameters</span></span>
<span data-ttu-id="6ecab-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ecab-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ecab-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ecab-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ecab-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ecab-148">INPUTS</span></span>

### <span data-ttu-id="6ecab-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6ecab-149">System.String</span></span>

### <span data-ttu-id="6ecab-150">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="6ecab-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="6ecab-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6ecab-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6ecab-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6ecab-152">System.Int32</span></span>

### <span data-ttu-id="6ecab-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6ecab-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6ecab-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="6ecab-154">System.DateTime</span></span>

### <span data-ttu-id="6ecab-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="6ecab-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="6ecab-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ecab-156">OUTPUTS</span></span>

### <span data-ttu-id="6ecab-157">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="6ecab-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="6ecab-158">Note</span><span class="sxs-lookup"><span data-stu-id="6ecab-158">NOTES</span></span>

## <span data-ttu-id="6ecab-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ecab-159">RELATED LINKS</span></span>