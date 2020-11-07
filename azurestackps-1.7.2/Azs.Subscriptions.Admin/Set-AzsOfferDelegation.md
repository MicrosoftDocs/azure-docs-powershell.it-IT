---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e0c752c3ffd266a3615fdd5a1f5193e0202b29a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858365"
---
# <span data-ttu-id="c4279-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c4279-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="c4279-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4279-102">SYNOPSIS</span></span>
<span data-ttu-id="c4279-103">Aggiorna la delega dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="c4279-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="c4279-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4279-104">SYNTAX</span></span>

### <span data-ttu-id="c4279-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4279-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4279-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c4279-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4279-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4279-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4279-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4279-108">DESCRIPTION</span></span>
<span data-ttu-id="c4279-109">Aggiorna la delega dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="c4279-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="c4279-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4279-110">EXAMPLES</span></span>

### <span data-ttu-id="c4279-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4279-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="c4279-112">Aggiorna la delega dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="c4279-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="c4279-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4279-113">PARAMETERS</span></span>

### <span data-ttu-id="c4279-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4279-114">-InputObject</span></span>
<span data-ttu-id="c4279-115">L'oggetto di input di tipo Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation.</span><span class="sxs-lookup"><span data-stu-id="c4279-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

```yaml
Type: OfferDelegation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4279-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c4279-116">-Location</span></span>
<span data-ttu-id="c4279-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4279-117">Location of the resource.</span></span>

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

### <span data-ttu-id="c4279-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4279-118">-Name</span></span>
<span data-ttu-id="c4279-119">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="c4279-119">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4279-120">-Offername</span><span class="sxs-lookup"><span data-stu-id="c4279-120">-OfferName</span></span>
<span data-ttu-id="c4279-121">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="c4279-121">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4279-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4279-122">-ResourceGroupName</span></span>
<span data-ttu-id="c4279-123">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4279-123">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4279-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4279-124">-ResourceId</span></span>
<span data-ttu-id="c4279-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4279-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4279-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4279-126">-SubscriptionId</span></span>
<span data-ttu-id="c4279-127">Identificatore dell'abbonamento che riceve l'offerta delegata.</span><span class="sxs-lookup"><span data-stu-id="c4279-127">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="c4279-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4279-128">-Confirm</span></span>
<span data-ttu-id="c4279-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4279-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4279-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4279-130">-WhatIf</span></span>
<span data-ttu-id="c4279-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4279-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4279-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4279-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4279-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4279-133">CommonParameters</span></span>
<span data-ttu-id="c4279-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4279-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4279-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4279-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4279-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4279-136">INPUTS</span></span>

## <span data-ttu-id="c4279-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4279-137">OUTPUTS</span></span>

### <span data-ttu-id="c4279-138">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c4279-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="c4279-139">Note</span><span class="sxs-lookup"><span data-stu-id="c4279-139">NOTES</span></span>

## <span data-ttu-id="c4279-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4279-140">RELATED LINKS</span></span>

