---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030408"
---
# <span data-ttu-id="32865-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="32865-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="32865-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32865-102">SYNOPSIS</span></span>
<span data-ttu-id="32865-103">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="32865-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="32865-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32865-104">SYNTAX</span></span>

### <span data-ttu-id="32865-105">Set (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32865-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32865-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="32865-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32865-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="32865-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32865-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32865-108">DESCRIPTION</span></span>
<span data-ttu-id="32865-109">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="32865-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="32865-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32865-110">EXAMPLES</span></span>

### <span data-ttu-id="32865-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="32865-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="32865-112">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="32865-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="32865-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32865-113">PARAMETERS</span></span>

### <span data-ttu-id="32865-114">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="32865-114">-OfferId</span></span>
<span data-ttu-id="32865-115">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="32865-115">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32865-116">-Digitare</span><span class="sxs-lookup"><span data-stu-id="32865-116">-Type</span></span>
<span data-ttu-id="32865-117">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="32865-117">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32865-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="32865-118">-Tags</span></span>
<span data-ttu-id="32865-119">Elenco di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="32865-119">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32865-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32865-120">-SubscriptionId</span></span>
<span data-ttu-id="32865-121">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="32865-121">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32865-122">-Stato</span><span class="sxs-lookup"><span data-stu-id="32865-122">-State</span></span>
<span data-ttu-id="32865-123">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="32865-123">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32865-124">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="32865-124">-TenantId</span></span>
<span data-ttu-id="32865-125">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="32865-125">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32865-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="32865-126">-DisplayName</span></span>
<span data-ttu-id="32865-127">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="32865-127">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32865-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="32865-128">-Location</span></span>
<span data-ttu-id="32865-129">Posizione in cui la risorsa è posizione.</span><span class="sxs-lookup"><span data-stu-id="32865-129">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32865-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32865-130">-ResourceId</span></span>
<span data-ttu-id="32865-131">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="32865-131">The resource ID.</span></span>

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

### <span data-ttu-id="32865-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32865-132">-InputObject</span></span>
<span data-ttu-id="32865-133">Posbbily della quota di rete modificata restituita da Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="32865-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

```yaml
Type: SubscriptionModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32865-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32865-134">-WhatIf</span></span>
<span data-ttu-id="32865-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32865-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32865-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32865-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32865-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32865-137">-Confirm</span></span>
<span data-ttu-id="32865-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32865-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32865-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32865-139">CommonParameters</span></span>
<span data-ttu-id="32865-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32865-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32865-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32865-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32865-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32865-142">INPUTS</span></span>

## <span data-ttu-id="32865-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32865-143">OUTPUTS</span></span>

### <span data-ttu-id="32865-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="32865-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="32865-145">Note</span><span class="sxs-lookup"><span data-stu-id="32865-145">NOTES</span></span>

## <span data-ttu-id="32865-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32865-146">RELATED LINKS</span></span>
