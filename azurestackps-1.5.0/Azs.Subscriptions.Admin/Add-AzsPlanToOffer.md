---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e501feeea3509725b53c85007934c8e682de48a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685144"
---
# <span data-ttu-id="83b52-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="83b52-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="83b52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83b52-102">SYNOPSIS</span></span>
<span data-ttu-id="83b52-103">Collega un piano a un'offerta.</span><span class="sxs-lookup"><span data-stu-id="83b52-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="83b52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83b52-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83b52-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83b52-105">DESCRIPTION</span></span>
<span data-ttu-id="83b52-106">Collega un piano a un'offerta.</span><span class="sxs-lookup"><span data-stu-id="83b52-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="83b52-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83b52-107">EXAMPLES</span></span>

### <span data-ttu-id="83b52-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="83b52-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="83b52-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83b52-109">PARAMETERS</span></span>

### <span data-ttu-id="83b52-110">-Force</span><span class="sxs-lookup"><span data-stu-id="83b52-110">-Force</span></span>
<span data-ttu-id="83b52-111">Contrassegna per rimuovere l'elemento senza conferma.</span><span class="sxs-lookup"><span data-stu-id="83b52-111">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b52-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="83b52-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="83b52-113">Numero massimo di acquisizioni per gli abbonati</span><span class="sxs-lookup"><span data-stu-id="83b52-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b52-114">-Offername</span><span class="sxs-lookup"><span data-stu-id="83b52-114">-OfferName</span></span>
<span data-ttu-id="83b52-115">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="83b52-115">Name of an offer.</span></span>

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

### <span data-ttu-id="83b52-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="83b52-116">-PlanLinkType</span></span>
<span data-ttu-id="83b52-117">Tipo di collegamento piano.</span><span class="sxs-lookup"><span data-stu-id="83b52-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b52-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="83b52-118">-PlanName</span></span>
<span data-ttu-id="83b52-119">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="83b52-119">Name of the plan.</span></span>

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

### <span data-ttu-id="83b52-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b52-120">-ResourceGroupName</span></span>
<span data-ttu-id="83b52-121">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="83b52-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b52-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83b52-122">-Confirm</span></span>
<span data-ttu-id="83b52-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83b52-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83b52-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b52-124">-WhatIf</span></span>
<span data-ttu-id="83b52-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83b52-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83b52-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83b52-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83b52-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b52-127">CommonParameters</span></span>
<span data-ttu-id="83b52-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83b52-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b52-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b52-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b52-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83b52-130">INPUTS</span></span>

## <span data-ttu-id="83b52-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83b52-131">OUTPUTS</span></span>

## <span data-ttu-id="83b52-132">Note</span><span class="sxs-lookup"><span data-stu-id="83b52-132">NOTES</span></span>

## <span data-ttu-id="83b52-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83b52-133">RELATED LINKS</span></span>
