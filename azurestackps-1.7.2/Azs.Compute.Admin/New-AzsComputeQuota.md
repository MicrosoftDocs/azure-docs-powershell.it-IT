---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc92bcc617c771c15330d1a24e8ed24466f7ffc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857542"
---
# <span data-ttu-id="e754e-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="e754e-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="e754e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e754e-102">SYNOPSIS</span></span>
<span data-ttu-id="e754e-103">Creare una nuova quota di calcolo usata per limitare le risorse di calcolo.</span><span class="sxs-lookup"><span data-stu-id="e754e-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="e754e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e754e-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e754e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e754e-105">DESCRIPTION</span></span>
<span data-ttu-id="e754e-106">Creare una nuova quota di calcolo.</span><span class="sxs-lookup"><span data-stu-id="e754e-106">Create a new compute quota.</span></span>

## <span data-ttu-id="e754e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e754e-107">EXAMPLES</span></span>

### <span data-ttu-id="e754e-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e754e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="e754e-109">Creare una nuova quota di calcolo.</span><span class="sxs-lookup"><span data-stu-id="e754e-109">Create a new compute quota.</span></span>

## <span data-ttu-id="e754e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e754e-110">PARAMETERS</span></span>

### <span data-ttu-id="e754e-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="e754e-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="e754e-112">Numero di set di disponibilità consentiti.</span><span class="sxs-lookup"><span data-stu-id="e754e-112">Number  of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e754e-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="e754e-113">-CoresCount</span></span>
<span data-ttu-id="e754e-114">Numero di core consentiti.</span><span class="sxs-lookup"><span data-stu-id="e754e-114">Number  of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: 3
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e754e-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e754e-115">-Location</span></span>
<span data-ttu-id="e754e-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e754e-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e754e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e754e-117">-Name</span></span>
<span data-ttu-id="e754e-118">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="e754e-118">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e754e-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="e754e-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="e754e-120">Dimensioni per i dischi gestiti standard e gli snapshot consentiti.</span><span class="sxs-lookup"><span data-stu-id="e754e-120">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e754e-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="e754e-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="e754e-122">Dimensioni per i dischi gestiti standard e gli snapshot consentiti.</span><span class="sxs-lookup"><span data-stu-id="e754e-122">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e754e-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="e754e-123">-VirtualMachineCount</span></span>
<span data-ttu-id="e754e-124">Numero di macchine virtuali consentite.</span><span class="sxs-lookup"><span data-stu-id="e754e-124">Number  of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e754e-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="e754e-125">-VmScaleSetCount</span></span>
<span data-ttu-id="e754e-126">Numero di set di proporzioni consentiti.</span><span class="sxs-lookup"><span data-stu-id="e754e-126">Number  of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e754e-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e754e-127">-Confirm</span></span>
<span data-ttu-id="e754e-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e754e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e754e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e754e-129">-WhatIf</span></span>
<span data-ttu-id="e754e-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e754e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e754e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e754e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e754e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e754e-132">CommonParameters</span></span>
<span data-ttu-id="e754e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e754e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e754e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e754e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e754e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e754e-135">INPUTS</span></span>

## <span data-ttu-id="e754e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e754e-136">OUTPUTS</span></span>

### <span data-ttu-id="e754e-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="e754e-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="e754e-138">Note</span><span class="sxs-lookup"><span data-stu-id="e754e-138">NOTES</span></span>

## <span data-ttu-id="e754e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e754e-139">RELATED LINKS</span></span>

