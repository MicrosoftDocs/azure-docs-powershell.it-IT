---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8da912ed9751231a44c34b27df36abc62d55c4ab
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859689"
---
# <span data-ttu-id="8a938-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="8a938-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="8a938-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a938-102">SYNOPSIS</span></span>
<span data-ttu-id="8a938-103">Aggiornare una quota di calcolo esistente usando i parametri forniti.</span><span class="sxs-lookup"><span data-stu-id="8a938-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="8a938-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a938-104">SYNTAX</span></span>

### <span data-ttu-id="8a938-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a938-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a938-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a938-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a938-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8a938-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a938-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a938-108">DESCRIPTION</span></span>
<span data-ttu-id="8a938-109">Aggiornare una quota di calcolo esistente.</span><span class="sxs-lookup"><span data-stu-id="8a938-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="8a938-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a938-110">EXAMPLES</span></span>

### <span data-ttu-id="8a938-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8a938-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="8a938-112">Aggiornare una quota di calcolo.</span><span class="sxs-lookup"><span data-stu-id="8a938-112">Update a compute quota.</span></span>

## <span data-ttu-id="8a938-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a938-113">PARAMETERS</span></span>

### <span data-ttu-id="8a938-114">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="8a938-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="8a938-115">Numero di set di disponibilità consentiti.</span><span class="sxs-lookup"><span data-stu-id="8a938-115">Number of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a938-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="8a938-116">-CoresCount</span></span>
<span data-ttu-id="8a938-117">Numero di core consentiti.</span><span class="sxs-lookup"><span data-stu-id="8a938-117">Number of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a938-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a938-118">-InputObject</span></span>
<span data-ttu-id="8a938-119">La quota di calcolo eventualmente modificata restituita restituisce get-AzsComputeQuota.</span><span class="sxs-lookup"><span data-stu-id="8a938-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

```yaml
Type: ComputeQuotaObject
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a938-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8a938-120">-Location</span></span>
<span data-ttu-id="8a938-121">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8a938-121">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a938-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a938-122">-Name</span></span>
<span data-ttu-id="8a938-123">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="8a938-123">The name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a938-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="8a938-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="8a938-125">Dimensioni per i dischi gestiti standard e gli snapshot consentiti.</span><span class="sxs-lookup"><span data-stu-id="8a938-125">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a938-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a938-126">-ResourceId</span></span>
<span data-ttu-id="8a938-127">ID di quota Compute ARM.</span><span class="sxs-lookup"><span data-stu-id="8a938-127">The ARM compute quota id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a938-128">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="8a938-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="8a938-129">Dimensioni per i dischi gestiti standard e gli snapshot consentiti.</span><span class="sxs-lookup"><span data-stu-id="8a938-129">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a938-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="8a938-130">-VirtualMachineCount</span></span>
<span data-ttu-id="8a938-131">Numero di macchine virtuali consentite.</span><span class="sxs-lookup"><span data-stu-id="8a938-131">Number of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a938-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="8a938-132">-VmScaleSetCount</span></span>
<span data-ttu-id="8a938-133">Numero di set di proporzioni consentiti.</span><span class="sxs-lookup"><span data-stu-id="8a938-133">Number of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a938-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a938-134">-Confirm</span></span>
<span data-ttu-id="8a938-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a938-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a938-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a938-136">-WhatIf</span></span>
<span data-ttu-id="8a938-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a938-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a938-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a938-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a938-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a938-139">CommonParameters</span></span>
<span data-ttu-id="8a938-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a938-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a938-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a938-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a938-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a938-142">INPUTS</span></span>

## <span data-ttu-id="8a938-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a938-143">OUTPUTS</span></span>

### <span data-ttu-id="8a938-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="8a938-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="8a938-145">Note</span><span class="sxs-lookup"><span data-stu-id="8a938-145">NOTES</span></span>

## <span data-ttu-id="8a938-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a938-146">RELATED LINKS</span></span>

