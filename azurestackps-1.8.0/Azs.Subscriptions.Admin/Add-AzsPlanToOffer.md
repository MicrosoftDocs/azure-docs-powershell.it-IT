---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7d51bef12f0f7808aff3fda819ac614e0bb1c9
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859289"
---
# <span data-ttu-id="518e4-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="518e4-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="518e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="518e4-102">SYNOPSIS</span></span>
<span data-ttu-id="518e4-103">Collega un piano a un'offerta.</span><span class="sxs-lookup"><span data-stu-id="518e4-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="518e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="518e4-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="518e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="518e4-105">DESCRIPTION</span></span>
<span data-ttu-id="518e4-106">Collega un piano a un'offerta.</span><span class="sxs-lookup"><span data-stu-id="518e4-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="518e4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="518e4-107">EXAMPLES</span></span>

### <span data-ttu-id="518e4-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="518e4-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="518e4-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="518e4-109">PARAMETERS</span></span>

### <span data-ttu-id="518e4-110">-Force</span><span class="sxs-lookup"><span data-stu-id="518e4-110">-Force</span></span>
<span data-ttu-id="518e4-111">Contrassegna per rimuovere l'elemento senza conferma.</span><span class="sxs-lookup"><span data-stu-id="518e4-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="518e4-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="518e4-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="518e4-113">Numero massimo di acquisizioni per gli abbonati</span><span class="sxs-lookup"><span data-stu-id="518e4-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="518e4-114">-Offername</span><span class="sxs-lookup"><span data-stu-id="518e4-114">-OfferName</span></span>
<span data-ttu-id="518e4-115">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="518e4-115">Name of an offer.</span></span>

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

### <span data-ttu-id="518e4-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="518e4-116">-PlanLinkType</span></span>
<span data-ttu-id="518e4-117">Tipo di collegamento piano.</span><span class="sxs-lookup"><span data-stu-id="518e4-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="518e4-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="518e4-118">-PlanName</span></span>
<span data-ttu-id="518e4-119">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="518e4-119">Name of the plan.</span></span>

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

### <span data-ttu-id="518e4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="518e4-120">-ResourceGroupName</span></span>
<span data-ttu-id="518e4-121">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="518e4-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="518e4-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="518e4-122">-Confirm</span></span>
<span data-ttu-id="518e4-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="518e4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="518e4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="518e4-124">-WhatIf</span></span>
<span data-ttu-id="518e4-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="518e4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="518e4-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="518e4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="518e4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="518e4-127">CommonParameters</span></span>
<span data-ttu-id="518e4-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="518e4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="518e4-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="518e4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="518e4-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="518e4-130">INPUTS</span></span>

## <span data-ttu-id="518e4-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="518e4-131">OUTPUTS</span></span>

## <span data-ttu-id="518e4-132">Note</span><span class="sxs-lookup"><span data-stu-id="518e4-132">NOTES</span></span>

## <span data-ttu-id="518e4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="518e4-133">RELATED LINKS</span></span>

