---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 8ef13dd067cd0cf1161e3aa58b52a961fe90a949
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032585"
---
# <span data-ttu-id="bc4a3-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bc4a3-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="bc4a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="bc4a3-103">Creare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-103">Create a gallery image version.</span></span>

## <span data-ttu-id="bc4a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc4a3-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc4a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc4a3-105">DESCRIPTION</span></span>
<span data-ttu-id="bc4a3-106">Creare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-106">Create a gallery image version.</span></span>

## <span data-ttu-id="bc4a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc4a3-107">EXAMPLES</span></span>

### <span data-ttu-id="bc4a3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bc4a3-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="bc4a3-109">Creare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-109">Create a gallery image version.</span></span>

### <span data-ttu-id="bc4a3-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bc4a3-110">Example 2</span></span>
```powershell
PS C:\> $osDiskImageEncryption = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES'}
PS C:\> $dataDiskImageEncryption1 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES1';Lun=1}
PS C:\> $dataDiskImageEncryption2 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES2';Lun=2}
PS C:\> $dataDiskImageEncryptions = @($dataDiskImageEncryption1,$dataDiskImageEncryption2)
PS C:\> $encryption1 = @{OSDiskImage=$osDiskImageEncryption;DataDiskImages=$dataDiskImageEncryptions}
PS C:\> $region1 = @{Name='West US';ReplicaCount=1;StorageAccountType=Standard_LRS;Encryption=$encryption1}
PS C:\> $targetRegions = @{$region1}
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $SourceImageId -ReplicaCount 2 -StorageAccountType Standard_LRS -PublishingProfileExcludeFromLatest -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegion
```

<span data-ttu-id="bc4a3-111">Creare una versione di immagine della raccolta con crittografia immagine disco.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="bc4a3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc4a3-112">PARAMETERS</span></span>

### <span data-ttu-id="bc4a3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc4a3-113">-AsJob</span></span>
<span data-ttu-id="bc4a3-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bc4a3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc4a3-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="bc4a3-115">-DataDiskImage</span></span>
<span data-ttu-id="bc4a3-116">Immagini disco dati.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-116">Data disk images.</span></span>   <span data-ttu-id="bc4a3-117">ad esempio, @ {source = @ {ID =<source_id>}; Lun = 1; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="bc4a3-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryDataDiskImage[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc4a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc4a3-118">-DefaultProfile</span></span>
<span data-ttu-id="bc4a3-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc4a3-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="bc4a3-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="bc4a3-121">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="bc4a3-122">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="bc4a3-122">-GalleryName</span></span>
<span data-ttu-id="bc4a3-123">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="bc4a3-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bc4a3-124">-Location</span></span>
<span data-ttu-id="bc4a3-125">Posizione delle risorse</span><span class="sxs-lookup"><span data-stu-id="bc4a3-125">Resource location</span></span>

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

### <span data-ttu-id="bc4a3-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc4a3-126">-Name</span></span>
<span data-ttu-id="bc4a3-127">Nome della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="bc4a3-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="bc4a3-128">-OSDiskImage</span></span>
<span data-ttu-id="bc4a3-129">Immagine del disco OS ad esempio @ {source = @ {ID =<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="bc4a3-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryOSDiskImage
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc4a3-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="bc4a3-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="bc4a3-131">Data di fine della durata della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-131">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="bc4a3-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="bc4a3-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="bc4a3-133">Se è impostato, le macchine virtuali distribuite dalla versione più recente della definizione di immagine non utilizzeranno questa versione di immagine.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="bc4a3-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="bc4a3-134">-ReplicaCount</span></span>
<span data-ttu-id="bc4a3-135">Numero di repliche della versione di immagine da creare per area geografica.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="bc4a3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc4a3-136">-ResourceGroupName</span></span>
<span data-ttu-id="bc4a3-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="bc4a3-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="bc4a3-138">-SourceImageId</span></span>
<span data-ttu-id="bc4a3-139">ID dell'immagine di origine da cui verrà creata la versione di immagine.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="bc4a3-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="bc4a3-140">-StorageAccountType</span></span>
<span data-ttu-id="bc4a3-141">Specifica il tipo di account di archiviazione da usare per archiviare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="bc4a3-142">Questa proprietà non è aggiornabile.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-142">This property is not updatable.</span></span> <span data-ttu-id="bc4a3-143">I valori disponibili sono Standard_LRS, Standard_ZRS e Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

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

### <span data-ttu-id="bc4a3-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="bc4a3-144">-Tag</span></span>
<span data-ttu-id="bc4a3-145">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="bc4a3-145">Resource tags</span></span>

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

### <span data-ttu-id="bc4a3-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="bc4a3-146">-TargetRegion</span></span>
<span data-ttu-id="bc4a3-147">Aree di destinazione in cui verrà replicata la versione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-147">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="bc4a3-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc4a3-148">-Confirm</span></span>
<span data-ttu-id="bc4a3-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc4a3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc4a3-150">-WhatIf</span></span>
<span data-ttu-id="bc4a3-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc4a3-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc4a3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc4a3-153">CommonParameters</span></span>
<span data-ttu-id="bc4a3-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc4a3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc4a3-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc4a3-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc4a3-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc4a3-156">INPUTS</span></span>

### <span data-ttu-id="bc4a3-157">System. String</span><span class="sxs-lookup"><span data-stu-id="bc4a3-157">System.String</span></span>

### <span data-ttu-id="bc4a3-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc4a3-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bc4a3-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bc4a3-159">System.Int32</span></span>

### <span data-ttu-id="bc4a3-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bc4a3-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bc4a3-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bc4a3-161">System.DateTime</span></span>

### <span data-ttu-id="bc4a3-162">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="bc4a3-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="bc4a3-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc4a3-163">OUTPUTS</span></span>

### <span data-ttu-id="bc4a3-164">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bc4a3-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="bc4a3-165">Note</span><span class="sxs-lookup"><span data-stu-id="bc4a3-165">NOTES</span></span>

## <span data-ttu-id="bc4a3-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc4a3-166">RELATED LINKS</span></span>
