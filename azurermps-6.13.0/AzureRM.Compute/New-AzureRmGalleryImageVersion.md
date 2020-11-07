---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
ms.openlocfilehash: f27c861386e7a570fe72a5266362bee7fed39e5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688148"
---
# <span data-ttu-id="50744-101">New-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="50744-101">New-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="50744-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50744-102">SYNOPSIS</span></span>
<span data-ttu-id="50744-103">Creare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="50744-103">Create a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50744-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50744-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50744-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50744-105">DESCRIPTION</span></span>
<span data-ttu-id="50744-106">Creare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="50744-106">Create a gallery image version.</span></span>

## <span data-ttu-id="50744-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50744-107">EXAMPLES</span></span>

### <span data-ttu-id="50744-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50744-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="50744-109">Creare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="50744-109">Create a gallery image version.</span></span>

## <span data-ttu-id="50744-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50744-110">PARAMETERS</span></span>

### <span data-ttu-id="50744-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50744-111">-AsJob</span></span>
<span data-ttu-id="50744-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="50744-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50744-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50744-113">-DefaultProfile</span></span>
<span data-ttu-id="50744-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50744-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50744-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="50744-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="50744-116">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="50744-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50744-117">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="50744-117">-GalleryName</span></span>
<span data-ttu-id="50744-118">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="50744-118">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50744-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="50744-119">-Location</span></span>
<span data-ttu-id="50744-120">Posizione delle risorse</span><span class="sxs-lookup"><span data-stu-id="50744-120">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50744-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="50744-121">-Name</span></span>
<span data-ttu-id="50744-122">Nome della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="50744-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50744-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="50744-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="50744-124">Data di fine della durata della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="50744-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="50744-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="50744-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="50744-126">Se è impostato, le macchine virtuali distribuite dalla versione più recente della definizione di immagine non utilizzeranno questa versione di immagine.</span><span class="sxs-lookup"><span data-stu-id="50744-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="50744-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="50744-127">-ReplicaCount</span></span>
<span data-ttu-id="50744-128">Numero di repliche della versione di immagine da creare per area geografica.</span><span class="sxs-lookup"><span data-stu-id="50744-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="50744-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50744-129">-ResourceGroupName</span></span>
<span data-ttu-id="50744-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50744-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50744-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="50744-131">-SourceImageId</span></span>
<span data-ttu-id="50744-132">ID dell'immagine di origine da cui verrà creata la versione di immagine.</span><span class="sxs-lookup"><span data-stu-id="50744-132">The ID of the source image from which the Image Version is going to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50744-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="50744-133">-Tag</span></span>
<span data-ttu-id="50744-134">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="50744-134">Resource tags</span></span>

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

### <span data-ttu-id="50744-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="50744-135">-TargetRegion</span></span>
<span data-ttu-id="50744-136">Aree di destinazione in cui verrà replicata la versione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="50744-136">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="50744-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50744-137">-Confirm</span></span>
<span data-ttu-id="50744-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50744-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50744-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50744-139">-WhatIf</span></span>
<span data-ttu-id="50744-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50744-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50744-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50744-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50744-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50744-142">CommonParameters</span></span>
<span data-ttu-id="50744-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50744-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50744-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50744-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50744-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50744-145">INPUTS</span></span>

### <span data-ttu-id="50744-146">System. String</span><span class="sxs-lookup"><span data-stu-id="50744-146">System.String</span></span>

### <span data-ttu-id="50744-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="50744-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="50744-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="50744-148">System.Int32</span></span>

### <span data-ttu-id="50744-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="50744-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="50744-150">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="50744-150">System.DateTime</span></span>

### <span data-ttu-id="50744-151">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="50744-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="50744-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50744-152">OUTPUTS</span></span>

### <span data-ttu-id="50744-153">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="50744-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="50744-154">Note</span><span class="sxs-lookup"><span data-stu-id="50744-154">NOTES</span></span>

## <span data-ttu-id="50744-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50744-155">RELATED LINKS</span></span>
