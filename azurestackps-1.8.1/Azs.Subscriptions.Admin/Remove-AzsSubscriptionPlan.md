---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b2f5117224318eae53b8b11f4af58c736ac800b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859462"
---
# <span data-ttu-id="1329a-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="1329a-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="1329a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1329a-102">SYNOPSIS</span></span>
<span data-ttu-id="1329a-103">Elimina un piano per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="1329a-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="1329a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1329a-104">SYNTAX</span></span>

### <span data-ttu-id="1329a-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1329a-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1329a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1329a-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1329a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1329a-107">DESCRIPTION</span></span>
<span data-ttu-id="1329a-108">Elimina un piano per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="1329a-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="1329a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1329a-109">EXAMPLES</span></span>

### <span data-ttu-id="1329a-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1329a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="1329a-111">Eliminare un piano per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="1329a-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="1329a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1329a-112">PARAMETERS</span></span>

### <span data-ttu-id="1329a-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="1329a-113">-AcquisitionId</span></span>
<span data-ttu-id="1329a-114">Identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="1329a-114">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1329a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1329a-115">-Force</span></span>
<span data-ttu-id="1329a-116">Contrassegna per rimuovere l'elemento senza conferma.</span><span class="sxs-lookup"><span data-stu-id="1329a-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="1329a-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1329a-117">-ResourceId</span></span>
<span data-ttu-id="1329a-118">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1329a-118">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1329a-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1329a-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="1329a-120">ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1329a-120">The target subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1329a-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1329a-121">-Confirm</span></span>
<span data-ttu-id="1329a-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1329a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1329a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1329a-123">-WhatIf</span></span>
<span data-ttu-id="1329a-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1329a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1329a-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1329a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1329a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1329a-126">CommonParameters</span></span>
<span data-ttu-id="1329a-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1329a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1329a-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1329a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1329a-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1329a-129">INPUTS</span></span>

## <span data-ttu-id="1329a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1329a-130">OUTPUTS</span></span>

## <span data-ttu-id="1329a-131">Note</span><span class="sxs-lookup"><span data-stu-id="1329a-131">NOTES</span></span>

## <span data-ttu-id="1329a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1329a-132">RELATED LINKS</span></span>

