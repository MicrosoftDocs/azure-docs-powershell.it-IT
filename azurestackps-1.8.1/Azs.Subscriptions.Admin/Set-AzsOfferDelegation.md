---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1256fa41d7accc175e79bb531c62f76ace6482d8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859445"
---
# <span data-ttu-id="1bbfd-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="1bbfd-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="1bbfd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bbfd-102">SYNOPSIS</span></span>
<span data-ttu-id="1bbfd-103">Aggiorna la delega dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="1bbfd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bbfd-104">SYNTAX</span></span>

### <span data-ttu-id="1bbfd-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1bbfd-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bbfd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1bbfd-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bbfd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bbfd-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bbfd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bbfd-108">DESCRIPTION</span></span>
<span data-ttu-id="1bbfd-109">Aggiorna la delega dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="1bbfd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bbfd-110">EXAMPLES</span></span>

### <span data-ttu-id="1bbfd-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1bbfd-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="1bbfd-112">Aggiorna la delega dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="1bbfd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bbfd-113">PARAMETERS</span></span>

### <span data-ttu-id="1bbfd-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bbfd-114">-InputObject</span></span>
<span data-ttu-id="1bbfd-115">L'oggetto di input di tipo Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

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

### <span data-ttu-id="1bbfd-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1bbfd-116">-Location</span></span>
<span data-ttu-id="1bbfd-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-117">Location of the resource.</span></span>

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

### <span data-ttu-id="1bbfd-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bbfd-118">-Name</span></span>
<span data-ttu-id="1bbfd-119">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-119">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="1bbfd-120">-Offername</span><span class="sxs-lookup"><span data-stu-id="1bbfd-120">-OfferName</span></span>
<span data-ttu-id="1bbfd-121">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-121">Name of an offer.</span></span>

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

### <span data-ttu-id="1bbfd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bbfd-122">-ResourceGroupName</span></span>
<span data-ttu-id="1bbfd-123">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="1bbfd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bbfd-124">-ResourceId</span></span>
<span data-ttu-id="1bbfd-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-125">The resource id.</span></span>

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

### <span data-ttu-id="1bbfd-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1bbfd-126">-SubscriptionId</span></span>
<span data-ttu-id="1bbfd-127">Identificatore dell'abbonamento che riceve l'offerta delegata.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-127">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="1bbfd-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1bbfd-128">-Confirm</span></span>
<span data-ttu-id="1bbfd-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bbfd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bbfd-130">-WhatIf</span></span>
<span data-ttu-id="1bbfd-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bbfd-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bbfd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bbfd-133">CommonParameters</span></span>
<span data-ttu-id="1bbfd-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bbfd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bbfd-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bbfd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bbfd-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bbfd-136">INPUTS</span></span>

## <span data-ttu-id="1bbfd-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bbfd-137">OUTPUTS</span></span>

### <span data-ttu-id="1bbfd-138">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="1bbfd-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="1bbfd-139">Note</span><span class="sxs-lookup"><span data-stu-id="1bbfd-139">NOTES</span></span>

## <span data-ttu-id="1bbfd-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bbfd-140">RELATED LINKS</span></span>

