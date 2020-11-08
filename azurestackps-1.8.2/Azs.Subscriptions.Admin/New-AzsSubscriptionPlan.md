---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a4c99f48087dcbac17dc10da3c647525670fe90
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030373"
---
# <span data-ttu-id="a86d3-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="a86d3-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="a86d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a86d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a86d3-103">Crea un piano per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="a86d3-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="a86d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a86d3-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a86d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a86d3-105">DESCRIPTION</span></span>
<span data-ttu-id="a86d3-106">Crea un piano per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="a86d3-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="a86d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a86d3-107">EXAMPLES</span></span>

### <span data-ttu-id="a86d3-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a86d3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="a86d3-109">Creare un piano per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="a86d3-109">Create an subscription plan.</span></span>

## <span data-ttu-id="a86d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a86d3-110">PARAMETERS</span></span>

### <span data-ttu-id="a86d3-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="a86d3-111">-AcquisitionId</span></span>
<span data-ttu-id="a86d3-112">Identificatore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a86d3-112">Acquisition identifier.</span></span>

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

### <span data-ttu-id="a86d3-113">-PlanId</span><span class="sxs-lookup"><span data-stu-id="a86d3-113">-PlanId</span></span>
<span data-ttu-id="a86d3-114">Identificatore piano nel contesto dell'abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="a86d3-114">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="a86d3-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a86d3-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="a86d3-116">ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a86d3-116">The target subscription ID.</span></span>

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

### <span data-ttu-id="a86d3-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a86d3-117">-Confirm</span></span>
<span data-ttu-id="a86d3-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a86d3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a86d3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a86d3-119">-WhatIf</span></span>
<span data-ttu-id="a86d3-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a86d3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a86d3-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a86d3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a86d3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86d3-122">CommonParameters</span></span>
<span data-ttu-id="a86d3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a86d3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a86d3-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a86d3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86d3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a86d3-125">INPUTS</span></span>

## <span data-ttu-id="a86d3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a86d3-126">OUTPUTS</span></span>

### <span data-ttu-id="a86d3-127">Microsoft. AzureStack. Management. subscriptions. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="a86d3-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="a86d3-128">Note</span><span class="sxs-lookup"><span data-stu-id="a86d3-128">NOTES</span></span>

## <span data-ttu-id="a86d3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a86d3-129">RELATED LINKS</span></span>

