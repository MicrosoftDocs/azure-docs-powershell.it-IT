---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f5c0050f6a1e226f5b5513e11d70fac1844ecda
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859206"
---
# <span data-ttu-id="0cbf3-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="0cbf3-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="0cbf3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0cbf3-102">SYNOPSIS</span></span>
<span data-ttu-id="0cbf3-103">Scollegare un piano da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="0cbf3-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="0cbf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0cbf3-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cbf3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cbf3-105">DESCRIPTION</span></span>
<span data-ttu-id="0cbf3-106">Scollegare un piano da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="0cbf3-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="0cbf3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0cbf3-107">EXAMPLES</span></span>

### <span data-ttu-id="0cbf3-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0cbf3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="0cbf3-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0cbf3-109">PARAMETERS</span></span>

### <span data-ttu-id="0cbf3-110">-Force</span><span class="sxs-lookup"><span data-stu-id="0cbf3-110">-Force</span></span>
<span data-ttu-id="0cbf3-111">Contrassegna per rimuovere l'elemento senza conferma.</span><span class="sxs-lookup"><span data-stu-id="0cbf3-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="0cbf3-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="0cbf3-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="0cbf3-113">Numero massimo di acquisizioni per gli abbonati</span><span class="sxs-lookup"><span data-stu-id="0cbf3-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cbf3-114">-Offername</span><span class="sxs-lookup"><span data-stu-id="0cbf3-114">-OfferName</span></span>
<span data-ttu-id="0cbf3-115">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="0cbf3-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cbf3-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="0cbf3-116">-PlanLinkType</span></span>
<span data-ttu-id="0cbf3-117">Tipo di collegamento piano.</span><span class="sxs-lookup"><span data-stu-id="0cbf3-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="0cbf3-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="0cbf3-118">-PlanName</span></span>
<span data-ttu-id="0cbf3-119">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="0cbf3-119">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cbf3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cbf3-120">-ResourceGroupName</span></span>
<span data-ttu-id="0cbf3-121">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0cbf3-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cbf3-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0cbf3-122">-Confirm</span></span>
<span data-ttu-id="0cbf3-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cbf3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cbf3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cbf3-124">-WhatIf</span></span>
<span data-ttu-id="0cbf3-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0cbf3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cbf3-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0cbf3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cbf3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cbf3-127">CommonParameters</span></span>
<span data-ttu-id="0cbf3-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cbf3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cbf3-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cbf3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cbf3-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0cbf3-130">INPUTS</span></span>

## <span data-ttu-id="0cbf3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0cbf3-131">OUTPUTS</span></span>

## <span data-ttu-id="0cbf3-132">Note</span><span class="sxs-lookup"><span data-stu-id="0cbf3-132">NOTES</span></span>

## <span data-ttu-id="0cbf3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0cbf3-133">RELATED LINKS</span></span>

