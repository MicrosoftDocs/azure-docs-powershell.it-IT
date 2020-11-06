---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 617a7ac7d949eb54ab08b0d0cb06c0fca3ba79bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491341"
---
# <span data-ttu-id="1a65a-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="1a65a-101">New-AzsSubscription</span></span>

## <span data-ttu-id="1a65a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a65a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a65a-103">Creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1a65a-103">Create a subscription.</span></span>

## <span data-ttu-id="1a65a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a65a-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a65a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a65a-105">DESCRIPTION</span></span>
<span data-ttu-id="1a65a-106">Creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1a65a-106">Create a subscription.</span></span>

## <span data-ttu-id="1a65a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a65a-107">EXAMPLES</span></span>

### <span data-ttu-id="1a65a-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1a65a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="1a65a-109">Creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1a65a-109">Create a subscription.</span></span>

## <span data-ttu-id="1a65a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a65a-110">PARAMETERS</span></span>

### <span data-ttu-id="1a65a-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1a65a-111">-DisplayName</span></span>
<span data-ttu-id="1a65a-112">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1a65a-112">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a65a-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1a65a-113">-Location</span></span>
<span data-ttu-id="1a65a-114">Posizione in cui la risorsa è posizione.</span><span class="sxs-lookup"><span data-stu-id="1a65a-114">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a65a-115">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="1a65a-115">-OfferId</span></span>
<span data-ttu-id="1a65a-116">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="1a65a-116">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="1a65a-117">-Stato</span><span class="sxs-lookup"><span data-stu-id="1a65a-117">-State</span></span>
<span data-ttu-id="1a65a-118">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="1a65a-118">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a65a-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1a65a-119">-SubscriptionId</span></span>
<span data-ttu-id="1a65a-120">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1a65a-120">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a65a-121">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="1a65a-121">-TenantId</span></span>
<span data-ttu-id="1a65a-122">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="1a65a-122">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a65a-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1a65a-123">-Confirm</span></span>
<span data-ttu-id="1a65a-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a65a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a65a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a65a-125">-WhatIf</span></span>
<span data-ttu-id="1a65a-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a65a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a65a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a65a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a65a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a65a-128">CommonParameters</span></span>
<span data-ttu-id="1a65a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a65a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a65a-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a65a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a65a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a65a-131">INPUTS</span></span>

## <span data-ttu-id="1a65a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a65a-132">OUTPUTS</span></span>

### <span data-ttu-id="1a65a-133">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="1a65a-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="1a65a-134">Note</span><span class="sxs-lookup"><span data-stu-id="1a65a-134">NOTES</span></span>

## <span data-ttu-id="1a65a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a65a-135">RELATED LINKS</span></span>

