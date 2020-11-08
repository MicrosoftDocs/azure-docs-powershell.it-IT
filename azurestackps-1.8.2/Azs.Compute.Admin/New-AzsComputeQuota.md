---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffd2667f8c07c5b0594abe38f6cee5d40ce91a49
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030253"
---
# <span data-ttu-id="b66ef-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="b66ef-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="b66ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b66ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b66ef-103">Creare una nuova quota di calcolo usata per limitare le risorse di calcolo.</span><span class="sxs-lookup"><span data-stu-id="b66ef-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="b66ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b66ef-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b66ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b66ef-105">DESCRIPTION</span></span>
<span data-ttu-id="b66ef-106">Creare una nuova quota di calcolo.</span><span class="sxs-lookup"><span data-stu-id="b66ef-106">Create a new compute quota.</span></span>

## <span data-ttu-id="b66ef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b66ef-107">EXAMPLES</span></span>

### <span data-ttu-id="b66ef-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b66ef-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="b66ef-109">Creare una nuova quota di calcolo.</span><span class="sxs-lookup"><span data-stu-id="b66ef-109">Create a new compute quota.</span></span>

## <span data-ttu-id="b66ef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b66ef-110">PARAMETERS</span></span>

### <span data-ttu-id="b66ef-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="b66ef-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="b66ef-112">Numero di set di disponibilità consentiti.</span><span class="sxs-lookup"><span data-stu-id="b66ef-112">Number  of availability sets allowed.</span></span>

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

### <span data-ttu-id="b66ef-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="b66ef-113">-CoresCount</span></span>
<span data-ttu-id="b66ef-114">Numero di core consentiti.</span><span class="sxs-lookup"><span data-stu-id="b66ef-114">Number  of cores allowed.</span></span>

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

### <span data-ttu-id="b66ef-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b66ef-115">-Location</span></span>
<span data-ttu-id="b66ef-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b66ef-116">Location of the resource.</span></span>

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

### <span data-ttu-id="b66ef-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b66ef-117">-Name</span></span>
<span data-ttu-id="b66ef-118">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="b66ef-118">Name of the quota.</span></span>

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

### <span data-ttu-id="b66ef-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="b66ef-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="b66ef-120">Dimensioni per i dischi gestiti standard e gli snapshot consentiti.</span><span class="sxs-lookup"><span data-stu-id="b66ef-120">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="b66ef-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="b66ef-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="b66ef-122">Dimensioni per i dischi gestiti standard e gli snapshot consentiti.</span><span class="sxs-lookup"><span data-stu-id="b66ef-122">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="b66ef-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="b66ef-123">-VirtualMachineCount</span></span>
<span data-ttu-id="b66ef-124">Numero di macchine virtuali consentite.</span><span class="sxs-lookup"><span data-stu-id="b66ef-124">Number  of virtual machines allowed.</span></span>

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

### <span data-ttu-id="b66ef-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="b66ef-125">-VmScaleSetCount</span></span>
<span data-ttu-id="b66ef-126">Numero di set di proporzioni consentiti.</span><span class="sxs-lookup"><span data-stu-id="b66ef-126">Number  of scale sets allowed.</span></span>

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

### <span data-ttu-id="b66ef-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b66ef-127">-Confirm</span></span>
<span data-ttu-id="b66ef-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b66ef-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b66ef-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b66ef-129">-WhatIf</span></span>
<span data-ttu-id="b66ef-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b66ef-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b66ef-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b66ef-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b66ef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b66ef-132">CommonParameters</span></span>
<span data-ttu-id="b66ef-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b66ef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b66ef-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b66ef-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b66ef-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b66ef-135">INPUTS</span></span>

## <span data-ttu-id="b66ef-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b66ef-136">OUTPUTS</span></span>

### <span data-ttu-id="b66ef-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="b66ef-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="b66ef-138">Note</span><span class="sxs-lookup"><span data-stu-id="b66ef-138">NOTES</span></span>

## <span data-ttu-id="b66ef-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b66ef-139">RELATED LINKS</span></span>

