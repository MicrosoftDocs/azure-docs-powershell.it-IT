---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: d905159ca62f34584f045a699621f6672507ffe1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030409"
---
# <span data-ttu-id="db3af-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="db3af-101">New-AzsSubscription</span></span>

## <span data-ttu-id="db3af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db3af-102">SYNOPSIS</span></span>
<span data-ttu-id="db3af-103">Creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="db3af-103">Create a subscription.</span></span>

## <span data-ttu-id="db3af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db3af-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db3af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db3af-105">DESCRIPTION</span></span>
<span data-ttu-id="db3af-106">Creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="db3af-106">Create a subscription.</span></span>

## <span data-ttu-id="db3af-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db3af-107">EXAMPLES</span></span>

### <span data-ttu-id="db3af-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="db3af-108">EXAMPLE 1</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="db3af-109">Creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="db3af-109">Create a subscription.</span></span>

## <span data-ttu-id="db3af-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db3af-110">PARAMETERS</span></span>

### <span data-ttu-id="db3af-111">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="db3af-111">-OfferId</span></span>
<span data-ttu-id="db3af-112">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="db3af-112">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="db3af-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db3af-113">-DisplayName</span></span>
<span data-ttu-id="db3af-114">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="db3af-114">Subscription name.</span></span>

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

### <span data-ttu-id="db3af-115">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="db3af-115">-TenantId</span></span>
<span data-ttu-id="db3af-116">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="db3af-116">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="db3af-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db3af-117">-SubscriptionId</span></span>
<span data-ttu-id="db3af-118">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="db3af-118">Subscription identifier.</span></span>

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

### <span data-ttu-id="db3af-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="db3af-119">-State</span></span>
<span data-ttu-id="db3af-120">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="db3af-120">Subscription state.</span></span>

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

### <span data-ttu-id="db3af-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="db3af-121">-Location</span></span>
<span data-ttu-id="db3af-122">Posizione in cui la risorsa è posizione.</span><span class="sxs-lookup"><span data-stu-id="db3af-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="db3af-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db3af-123">-WhatIf</span></span>
<span data-ttu-id="db3af-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db3af-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db3af-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db3af-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db3af-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db3af-126">-Confirm</span></span>
<span data-ttu-id="db3af-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db3af-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db3af-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db3af-128">CommonParameters</span></span>
<span data-ttu-id="db3af-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db3af-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db3af-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db3af-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db3af-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db3af-131">INPUTS</span></span>

## <span data-ttu-id="db3af-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db3af-132">OUTPUTS</span></span>

### <span data-ttu-id="db3af-133">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="db3af-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="db3af-134">Note</span><span class="sxs-lookup"><span data-stu-id="db3af-134">NOTES</span></span>

## <span data-ttu-id="db3af-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db3af-135">RELATED LINKS</span></span>
