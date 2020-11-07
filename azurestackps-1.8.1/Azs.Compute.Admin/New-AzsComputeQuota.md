---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffd2667f8c07c5b0594abe38f6cee5d40ce91a49
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859717"
---
# <span data-ttu-id="56c01-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="56c01-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="56c01-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56c01-102">SYNOPSIS</span></span>
<span data-ttu-id="56c01-103">Creare una nuova quota di calcolo usata per limitare le risorse di calcolo.</span><span class="sxs-lookup"><span data-stu-id="56c01-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="56c01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56c01-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56c01-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56c01-105">DESCRIPTION</span></span>
<span data-ttu-id="56c01-106">Creare una nuova quota di calcolo.</span><span class="sxs-lookup"><span data-stu-id="56c01-106">Create a new compute quota.</span></span>

## <span data-ttu-id="56c01-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56c01-107">EXAMPLES</span></span>

### <span data-ttu-id="56c01-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="56c01-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="56c01-109">Creare una nuova quota di calcolo.</span><span class="sxs-lookup"><span data-stu-id="56c01-109">Create a new compute quota.</span></span>

## <span data-ttu-id="56c01-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56c01-110">PARAMETERS</span></span>

### <span data-ttu-id="56c01-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="56c01-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="56c01-112">Numero di set di disponibilità consentiti.</span><span class="sxs-lookup"><span data-stu-id="56c01-112">Number  of availability sets allowed.</span></span>

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

### <span data-ttu-id="56c01-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="56c01-113">-CoresCount</span></span>
<span data-ttu-id="56c01-114">Numero di core consentiti.</span><span class="sxs-lookup"><span data-stu-id="56c01-114">Number  of cores allowed.</span></span>

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

### <span data-ttu-id="56c01-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="56c01-115">-Location</span></span>
<span data-ttu-id="56c01-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="56c01-116">Location of the resource.</span></span>

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

### <span data-ttu-id="56c01-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="56c01-117">-Name</span></span>
<span data-ttu-id="56c01-118">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="56c01-118">Name of the quota.</span></span>

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

### <span data-ttu-id="56c01-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="56c01-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="56c01-120">Dimensioni per i dischi gestiti standard e gli snapshot consentiti.</span><span class="sxs-lookup"><span data-stu-id="56c01-120">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="56c01-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="56c01-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="56c01-122">Dimensioni per i dischi gestiti standard e gli snapshot consentiti.</span><span class="sxs-lookup"><span data-stu-id="56c01-122">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="56c01-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="56c01-123">-VirtualMachineCount</span></span>
<span data-ttu-id="56c01-124">Numero di macchine virtuali consentite.</span><span class="sxs-lookup"><span data-stu-id="56c01-124">Number  of virtual machines allowed.</span></span>

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

### <span data-ttu-id="56c01-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="56c01-125">-VmScaleSetCount</span></span>
<span data-ttu-id="56c01-126">Numero di set di proporzioni consentiti.</span><span class="sxs-lookup"><span data-stu-id="56c01-126">Number  of scale sets allowed.</span></span>

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

### <span data-ttu-id="56c01-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56c01-127">-Confirm</span></span>
<span data-ttu-id="56c01-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56c01-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56c01-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56c01-129">-WhatIf</span></span>
<span data-ttu-id="56c01-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56c01-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56c01-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56c01-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56c01-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c01-132">CommonParameters</span></span>
<span data-ttu-id="56c01-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c01-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c01-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56c01-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c01-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56c01-135">INPUTS</span></span>

## <span data-ttu-id="56c01-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56c01-136">OUTPUTS</span></span>

### <span data-ttu-id="56c01-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="56c01-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="56c01-138">Note</span><span class="sxs-lookup"><span data-stu-id="56c01-138">NOTES</span></span>

## <span data-ttu-id="56c01-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56c01-139">RELATED LINKS</span></span>

