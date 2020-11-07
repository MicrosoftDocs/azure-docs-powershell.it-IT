---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f5c0050f6a1e226f5b5513e11d70fac1844ecda
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859466"
---
# <span data-ttu-id="71b13-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="71b13-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="71b13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71b13-102">SYNOPSIS</span></span>
<span data-ttu-id="71b13-103">Scollegare un piano da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="71b13-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="71b13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71b13-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71b13-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71b13-105">DESCRIPTION</span></span>
<span data-ttu-id="71b13-106">Scollegare un piano da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="71b13-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="71b13-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71b13-107">EXAMPLES</span></span>

### <span data-ttu-id="71b13-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="71b13-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="71b13-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71b13-109">PARAMETERS</span></span>

### <span data-ttu-id="71b13-110">-Force</span><span class="sxs-lookup"><span data-stu-id="71b13-110">-Force</span></span>
<span data-ttu-id="71b13-111">Contrassegna per rimuovere l'elemento senza conferma.</span><span class="sxs-lookup"><span data-stu-id="71b13-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="71b13-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="71b13-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="71b13-113">Numero massimo di acquisizioni per gli abbonati</span><span class="sxs-lookup"><span data-stu-id="71b13-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="71b13-114">-Offername</span><span class="sxs-lookup"><span data-stu-id="71b13-114">-OfferName</span></span>
<span data-ttu-id="71b13-115">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="71b13-115">Name of an offer.</span></span>

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

### <span data-ttu-id="71b13-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="71b13-116">-PlanLinkType</span></span>
<span data-ttu-id="71b13-117">Tipo di collegamento piano.</span><span class="sxs-lookup"><span data-stu-id="71b13-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="71b13-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="71b13-118">-PlanName</span></span>
<span data-ttu-id="71b13-119">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="71b13-119">Name of the plan.</span></span>

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

### <span data-ttu-id="71b13-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71b13-120">-ResourceGroupName</span></span>
<span data-ttu-id="71b13-121">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="71b13-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="71b13-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71b13-122">-Confirm</span></span>
<span data-ttu-id="71b13-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71b13-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71b13-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71b13-124">-WhatIf</span></span>
<span data-ttu-id="71b13-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71b13-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71b13-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71b13-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71b13-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b13-127">CommonParameters</span></span>
<span data-ttu-id="71b13-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b13-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b13-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71b13-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b13-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71b13-130">INPUTS</span></span>

## <span data-ttu-id="71b13-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71b13-131">OUTPUTS</span></span>

## <span data-ttu-id="71b13-132">Note</span><span class="sxs-lookup"><span data-stu-id="71b13-132">NOTES</span></span>

## <span data-ttu-id="71b13-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71b13-133">RELATED LINKS</span></span>

