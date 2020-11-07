---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb23765090b0edfd14fa355b9809a2385900396e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858766"
---
# <span data-ttu-id="0bc54-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="0bc54-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="0bc54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bc54-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc54-103">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0bc54-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="0bc54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bc54-104">SYNTAX</span></span>

### <span data-ttu-id="0bc54-105">Set (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0bc54-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bc54-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bc54-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bc54-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0bc54-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bc54-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bc54-108">DESCRIPTION</span></span>
<span data-ttu-id="0bc54-109">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0bc54-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="0bc54-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bc54-110">EXAMPLES</span></span>

### <span data-ttu-id="0bc54-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0bc54-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="0bc54-112">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0bc54-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="0bc54-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bc54-113">PARAMETERS</span></span>

### <span data-ttu-id="0bc54-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0bc54-114">-DisplayName</span></span>
<span data-ttu-id="0bc54-115">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0bc54-115">Subscription name.</span></span>

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

### <span data-ttu-id="0bc54-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bc54-116">-InputObject</span></span>
<span data-ttu-id="0bc54-117">Posbbily della quota di rete modificata restituita da Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="0bc54-117">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="0bc54-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0bc54-118">-Location</span></span>
<span data-ttu-id="0bc54-119">Posizione in cui la risorsa è posizione.</span><span class="sxs-lookup"><span data-stu-id="0bc54-119">Location where resource is location.</span></span>

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

### <span data-ttu-id="0bc54-120">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="0bc54-120">-OfferId</span></span>
<span data-ttu-id="0bc54-121">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="0bc54-121">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="0bc54-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bc54-122">-ResourceId</span></span>
<span data-ttu-id="0bc54-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="0bc54-123">The resource ID.</span></span>

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

### <span data-ttu-id="0bc54-124">-Stato</span><span class="sxs-lookup"><span data-stu-id="0bc54-124">-State</span></span>
<span data-ttu-id="0bc54-125">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0bc54-125">Subscription state.</span></span>

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

### <span data-ttu-id="0bc54-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0bc54-126">-SubscriptionId</span></span>
<span data-ttu-id="0bc54-127">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0bc54-127">Subscription identifier.</span></span>

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

### <span data-ttu-id="0bc54-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="0bc54-128">-Tags</span></span>
<span data-ttu-id="0bc54-129">Elenco di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="0bc54-129">List of key-value pairs.</span></span>

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

### <span data-ttu-id="0bc54-130">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="0bc54-130">-TenantId</span></span>
<span data-ttu-id="0bc54-131">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="0bc54-131">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="0bc54-132">-Digitare</span><span class="sxs-lookup"><span data-stu-id="0bc54-132">-Type</span></span>
<span data-ttu-id="0bc54-133">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0bc54-133">Type of resource.</span></span>

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

### <span data-ttu-id="0bc54-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0bc54-134">-Confirm</span></span>
<span data-ttu-id="0bc54-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bc54-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bc54-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bc54-136">-WhatIf</span></span>
<span data-ttu-id="0bc54-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0bc54-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bc54-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0bc54-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bc54-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc54-139">CommonParameters</span></span>
<span data-ttu-id="0bc54-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bc54-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc54-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bc54-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc54-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bc54-142">INPUTS</span></span>

## <span data-ttu-id="0bc54-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bc54-143">OUTPUTS</span></span>

### <span data-ttu-id="0bc54-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="0bc54-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="0bc54-145">Note</span><span class="sxs-lookup"><span data-stu-id="0bc54-145">NOTES</span></span>

## <span data-ttu-id="0bc54-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bc54-146">RELATED LINKS</span></span>

