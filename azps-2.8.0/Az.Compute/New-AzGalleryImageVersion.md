---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 80536a8bfce32d713649f3feab4d77b1662206b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675335"
---
# <span data-ttu-id="bbd64-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bbd64-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="bbd64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbd64-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd64-103">Creare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bbd64-103">Create a gallery image version.</span></span>

## <span data-ttu-id="bbd64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbd64-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-StorageAccountType <String>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbd64-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbd64-105">DESCRIPTION</span></span>
<span data-ttu-id="bbd64-106">Creare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bbd64-106">Create a gallery image version.</span></span>

## <span data-ttu-id="bbd64-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbd64-107">EXAMPLES</span></span>

### <span data-ttu-id="bbd64-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bbd64-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="bbd64-109">Creare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bbd64-109">Create a gallery image version.</span></span>

## <span data-ttu-id="bbd64-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbd64-110">PARAMETERS</span></span>

### <span data-ttu-id="bbd64-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbd64-111">-AsJob</span></span>
<span data-ttu-id="bbd64-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bbd64-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbd64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd64-113">-DefaultProfile</span></span>
<span data-ttu-id="bbd64-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd64-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbd64-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="bbd64-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="bbd64-116">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bbd64-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="bbd64-117">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="bbd64-117">-GalleryName</span></span>
<span data-ttu-id="bbd64-118">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bbd64-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="bbd64-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bbd64-119">-Location</span></span>
<span data-ttu-id="bbd64-120">Posizione delle risorse</span><span class="sxs-lookup"><span data-stu-id="bbd64-120">Resource location</span></span>

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

### <span data-ttu-id="bbd64-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbd64-121">-Name</span></span>
<span data-ttu-id="bbd64-122">Nome della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bbd64-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="bbd64-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="bbd64-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="bbd64-124">Data di fine della durata della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bbd64-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="bbd64-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="bbd64-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="bbd64-126">Se è impostato, le macchine virtuali distribuite dalla versione più recente della definizione di immagine non utilizzeranno questa versione di immagine.</span><span class="sxs-lookup"><span data-stu-id="bbd64-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="bbd64-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="bbd64-127">-ReplicaCount</span></span>
<span data-ttu-id="bbd64-128">Numero di repliche della versione di immagine da creare per area geografica.</span><span class="sxs-lookup"><span data-stu-id="bbd64-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="bbd64-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd64-129">-ResourceGroupName</span></span>
<span data-ttu-id="bbd64-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bbd64-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="bbd64-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="bbd64-131">-SourceImageId</span></span>
<span data-ttu-id="bbd64-132">ID dell'immagine di origine da cui verrà creata la versione di immagine.</span><span class="sxs-lookup"><span data-stu-id="bbd64-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="bbd64-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="bbd64-133">-StorageAccountType</span></span>
<span data-ttu-id="bbd64-134">Specifica il tipo di account di archiviazione da usare per archiviare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="bbd64-134">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="bbd64-135">Questa proprietà non è aggiornabile.</span><span class="sxs-lookup"><span data-stu-id="bbd64-135">This property is not updatable.</span></span> <span data-ttu-id="bbd64-136">I valori disponibili sono Standard_LRS e Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="bbd64-136">Available values are Standard_LRS and Standard_ZRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd64-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="bbd64-137">-Tag</span></span>
<span data-ttu-id="bbd64-138">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="bbd64-138">Resource tags</span></span>

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

### <span data-ttu-id="bbd64-139">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="bbd64-139">-TargetRegion</span></span>
<span data-ttu-id="bbd64-140">Aree di destinazione in cui verrà replicata la versione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="bbd64-140">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="bbd64-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bbd64-141">-Confirm</span></span>
<span data-ttu-id="bbd64-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbd64-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbd64-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbd64-143">-WhatIf</span></span>
<span data-ttu-id="bbd64-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbd64-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbd64-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbd64-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbd64-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd64-146">CommonParameters</span></span>
<span data-ttu-id="bbd64-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd64-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd64-148">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbd64-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd64-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbd64-149">INPUTS</span></span>

### <span data-ttu-id="bbd64-150">System. String</span><span class="sxs-lookup"><span data-stu-id="bbd64-150">System.String</span></span>

### <span data-ttu-id="bbd64-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bbd64-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bbd64-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bbd64-152">System.Int32</span></span>

### <span data-ttu-id="bbd64-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bbd64-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bbd64-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bbd64-154">System.DateTime</span></span>

### <span data-ttu-id="bbd64-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="bbd64-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="bbd64-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbd64-156">OUTPUTS</span></span>

### <span data-ttu-id="bbd64-157">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bbd64-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="bbd64-158">Note</span><span class="sxs-lookup"><span data-stu-id="bbd64-158">NOTES</span></span>

## <span data-ttu-id="bbd64-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbd64-159">RELATED LINKS</span></span>
