---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296274"
---
# <span data-ttu-id="32598-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="32598-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="32598-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32598-102">SYNOPSIS</span></span>
<span data-ttu-id="32598-103">Oggetto di distribuzione generico</span><span class="sxs-lookup"><span data-stu-id="32598-103">Generic distribution object</span></span>

## <span data-ttu-id="32598-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32598-104">SYNTAX</span></span>

### <span data-ttu-id="32598-105">ManagedImageDistributor (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32598-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="32598-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="32598-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="32598-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="32598-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="32598-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32598-108">DESCRIPTION</span></span>
<span data-ttu-id="32598-109">Oggetto di distribuzione generico</span><span class="sxs-lookup"><span data-stu-id="32598-109">Generic distribution object</span></span>

## <span data-ttu-id="32598-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32598-110">EXAMPLES</span></span>

### <span data-ttu-id="32598-111">Esempio 1: creare un distributore di immagini gestite</span><span class="sxs-lookup"><span data-stu-id="32598-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="32598-112">Questo comando crea un distributore di immagini gestite.</span><span class="sxs-lookup"><span data-stu-id="32598-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="32598-113">Esempio 2: creare un distributore VHD</span><span class="sxs-lookup"><span data-stu-id="32598-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="32598-114">Questo comando crea un distributore VHD.</span><span class="sxs-lookup"><span data-stu-id="32598-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="32598-115">Esempio 3: creare un distributore di immagini condivise</span><span class="sxs-lookup"><span data-stu-id="32598-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="32598-116">Questo comando crea un distributore di immagini condiviso.</span><span class="sxs-lookup"><span data-stu-id="32598-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="32598-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32598-117">PARAMETERS</span></span>

### <span data-ttu-id="32598-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="32598-118">-ArtifactTag</span></span>
<span data-ttu-id="32598-119">Tag che verranno applicati all'elemento dopo la creazione/aggiornamento da parte del server di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="32598-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

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

### <span data-ttu-id="32598-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="32598-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="32598-121">Contrassegno che indica se la versione di immagine creata deve essere esclusa dalla più recente.</span><span class="sxs-lookup"><span data-stu-id="32598-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="32598-122">Omettere di usare il valore predefinito (false).</span><span class="sxs-lookup"><span data-stu-id="32598-122">Omit to use the default (false).</span></span>

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

### <span data-ttu-id="32598-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="32598-123">-GalleryImageId</span></span>
<span data-ttu-id="32598-124">ID risorsa dell'immagine della raccolta immagini condivisa.</span><span class="sxs-lookup"><span data-stu-id="32598-124">Resource Id of the Shared Image Gallery image.</span></span>

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

### <span data-ttu-id="32598-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="32598-125">-ImageId</span></span>
<span data-ttu-id="32598-126">ID risorsa dell'immagine del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="32598-126">Resource Id of the Managed Disk Image.</span></span>

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

### <span data-ttu-id="32598-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="32598-127">-Location</span></span>
<span data-ttu-id="32598-128">La posizione di Azure per l'immagine deve corrispondere se l'immagine esiste già.</span><span class="sxs-lookup"><span data-stu-id="32598-128">Azure location for the image, should match if image already exists.</span></span>

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

### <span data-ttu-id="32598-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="32598-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="32598-130">Distribuire come immagine del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="32598-130">Distribute as a Managed Disk Image.</span></span>

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

### <span data-ttu-id="32598-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="32598-131">-ReplicationRegion</span></span>
<span data-ttu-id="32598-132">Elenco delle aree geografiche in cui verrà replicata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="32598-132">A list of regions that the image will be replicated to.</span></span>

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

### <span data-ttu-id="32598-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="32598-133">-RunOutputName</span></span>
<span data-ttu-id="32598-134">Il nome da usare per il RunOutput associato.</span><span class="sxs-lookup"><span data-stu-id="32598-134">The name to be used for the associated RunOutput.</span></span>

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

### <span data-ttu-id="32598-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="32598-135">-SharedImageDistributor</span></span>
<span data-ttu-id="32598-136">Distribuire tramite raccolta immagini condivise.</span><span class="sxs-lookup"><span data-stu-id="32598-136">Distribute via Shared Image Gallery.</span></span>

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

### <span data-ttu-id="32598-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="32598-137">-StorageAccountType</span></span>
<span data-ttu-id="32598-138">Tipo di account di archiviazione da usare per archiviare l'immagine condivisa.</span><span class="sxs-lookup"><span data-stu-id="32598-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="32598-139">Omettere di usare il valore predefinito (Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="32598-139">Omit to use the default (Standard_LRS).</span></span>

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

### <span data-ttu-id="32598-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="32598-140">-VhdDistributor</span></span>
<span data-ttu-id="32598-141">Distribuire tramite VHD in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="32598-141">Distribute via VHD in a storage account.</span></span>

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

### <span data-ttu-id="32598-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32598-142">CommonParameters</span></span>
<span data-ttu-id="32598-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32598-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32598-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32598-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32598-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32598-145">INPUTS</span></span>

## <span data-ttu-id="32598-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32598-146">OUTPUTS</span></span>

### <span data-ttu-id="32598-147">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="32598-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="32598-148">Note</span><span class="sxs-lookup"><span data-stu-id="32598-148">NOTES</span></span>

<span data-ttu-id="32598-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="32598-149">ALIASES</span></span>

## <span data-ttu-id="32598-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32598-150">RELATED LINKS</span></span>

