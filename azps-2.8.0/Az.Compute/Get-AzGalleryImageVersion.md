---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: cd09679117a964cc28e24d28f4097d511304a9a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675432"
---
# <span data-ttu-id="0aa63-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0aa63-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="0aa63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0aa63-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa63-103">Ottenere o elencare le versioni delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="0aa63-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="0aa63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0aa63-104">SYNTAX</span></span>

### <span data-ttu-id="0aa63-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0aa63-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0aa63-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0aa63-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0aa63-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0aa63-107">DESCRIPTION</span></span>
<span data-ttu-id="0aa63-108">Ottenere o elencare le versioni delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="0aa63-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="0aa63-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0aa63-109">EXAMPLES</span></span>

### <span data-ttu-id="0aa63-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0aa63-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -ImageDefinitionName image1 -GalleryImageVersionName 1.0.0

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="0aa63-111">Ottenere la versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="0aa63-111">Get the gallery image version.</span></span>

### <span data-ttu-id="0aa63-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0aa63-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -ImageDefinitionName image1 -GalleryImageVersionName 1*

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="0aa63-113">Ottenere le versioni delle immagini della raccolta che iniziano con "1".</span><span class="sxs-lookup"><span data-stu-id="0aa63-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="0aa63-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0aa63-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -ImageDefinitionName image1

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="0aa63-115">Ottenere tutte le versioni delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="0aa63-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="0aa63-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0aa63-116">PARAMETERS</span></span>

### <span data-ttu-id="0aa63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa63-117">-DefaultProfile</span></span>
<span data-ttu-id="0aa63-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aa63-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="0aa63-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="0aa63-120">Mostra lo stato di replica.</span><span class="sxs-lookup"><span data-stu-id="0aa63-120">Show replication status.</span></span>

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

### <span data-ttu-id="0aa63-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0aa63-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="0aa63-122">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="0aa63-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="0aa63-123">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="0aa63-123">-GalleryName</span></span>
<span data-ttu-id="0aa63-124">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="0aa63-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="0aa63-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="0aa63-125">-Name</span></span>
<span data-ttu-id="0aa63-126">Nome della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="0aa63-126">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0aa63-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aa63-127">-ResourceGroupName</span></span>
<span data-ttu-id="0aa63-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0aa63-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="0aa63-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0aa63-129">-ResourceId</span></span>
<span data-ttu-id="0aa63-130">ID risorsa per la versione dell'immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="0aa63-130">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="0aa63-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa63-131">CommonParameters</span></span>
<span data-ttu-id="0aa63-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aa63-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa63-133">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0aa63-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa63-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0aa63-134">INPUTS</span></span>

### <span data-ttu-id="0aa63-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0aa63-135">System.String</span></span>

### <span data-ttu-id="0aa63-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0aa63-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0aa63-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0aa63-137">OUTPUTS</span></span>

### <span data-ttu-id="0aa63-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0aa63-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="0aa63-139">Note</span><span class="sxs-lookup"><span data-stu-id="0aa63-139">NOTES</span></span>

## <span data-ttu-id="0aa63-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0aa63-140">RELATED LINKS</span></span>
