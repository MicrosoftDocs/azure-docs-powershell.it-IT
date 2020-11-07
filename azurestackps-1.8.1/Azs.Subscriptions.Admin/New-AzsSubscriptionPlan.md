---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a4c99f48087dcbac17dc10da3c647525670fe90
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859534"
---
# <span data-ttu-id="7046c-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="7046c-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="7046c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7046c-102">SYNOPSIS</span></span>
<span data-ttu-id="7046c-103">Crea un piano per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="7046c-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="7046c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7046c-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7046c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7046c-105">DESCRIPTION</span></span>
<span data-ttu-id="7046c-106">Crea un piano per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="7046c-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="7046c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7046c-107">EXAMPLES</span></span>

### <span data-ttu-id="7046c-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7046c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="7046c-109">Creare un piano per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="7046c-109">Create an subscription plan.</span></span>

## <span data-ttu-id="7046c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7046c-110">PARAMETERS</span></span>

### <span data-ttu-id="7046c-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="7046c-111">-AcquisitionId</span></span>
<span data-ttu-id="7046c-112">Identificatore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="7046c-112">Acquisition identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: $([Guid]::NewGuid())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7046c-113">-PlanId</span><span class="sxs-lookup"><span data-stu-id="7046c-113">-PlanId</span></span>
<span data-ttu-id="7046c-114">Identificatore piano nel contesto dell'abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="7046c-114">Plan identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7046c-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7046c-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="7046c-116">ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7046c-116">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7046c-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7046c-117">-Confirm</span></span>
<span data-ttu-id="7046c-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7046c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7046c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7046c-119">-WhatIf</span></span>
<span data-ttu-id="7046c-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7046c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7046c-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7046c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7046c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7046c-122">CommonParameters</span></span>
<span data-ttu-id="7046c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7046c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7046c-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7046c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7046c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7046c-125">INPUTS</span></span>

## <span data-ttu-id="7046c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7046c-126">OUTPUTS</span></span>

### <span data-ttu-id="7046c-127">Microsoft. AzureStack. Management. subscriptions. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="7046c-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="7046c-128">Note</span><span class="sxs-lookup"><span data-stu-id="7046c-128">NOTES</span></span>

## <span data-ttu-id="7046c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7046c-129">RELATED LINKS</span></span>

