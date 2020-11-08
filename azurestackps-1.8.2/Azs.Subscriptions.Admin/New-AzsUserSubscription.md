---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d4b7abdeb085c7cfee6444c4afeeb6a3e79d99e9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030541"
---
# <span data-ttu-id="8ae48-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="8ae48-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="8ae48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ae48-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae48-103">Creare un nuovo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8ae48-103">Create a new subscription.</span></span>

## <span data-ttu-id="8ae48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ae48-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ae48-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ae48-105">DESCRIPTION</span></span>
<span data-ttu-id="8ae48-106">Creare un nuovo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8ae48-106">Create a new subscription.</span></span>

## <span data-ttu-id="8ae48-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ae48-107">EXAMPLES</span></span>

### <span data-ttu-id="8ae48-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ae48-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="8ae48-109">Crea un nuovo abbonamento utente</span><span class="sxs-lookup"><span data-stu-id="8ae48-109">Creates a new user subscription</span></span>

## <span data-ttu-id="8ae48-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ae48-110">PARAMETERS</span></span>

### <span data-ttu-id="8ae48-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ae48-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="8ae48-112">Identificatore dell'abbonamento a DelegatedProvider padre.</span><span class="sxs-lookup"><span data-stu-id="8ae48-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae48-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8ae48-113">-DisplayName</span></span>
<span data-ttu-id="8ae48-114">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8ae48-114">Subscription name.</span></span>

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

### <span data-ttu-id="8ae48-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="8ae48-115">-ExternalReferenceId</span></span>
<span data-ttu-id="8ae48-116">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="8ae48-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae48-117">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="8ae48-117">-OfferId</span></span>
<span data-ttu-id="8ae48-118">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="8ae48-118">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="8ae48-119">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="8ae48-119">-Owner</span></span>
<span data-ttu-id="8ae48-120">Proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8ae48-120">Subscription owner.</span></span>

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

### <span data-ttu-id="8ae48-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="8ae48-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="8ae48-122">Tipo di gestione risorse di routing.</span><span class="sxs-lookup"><span data-stu-id="8ae48-122">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae48-123">-Stato</span><span class="sxs-lookup"><span data-stu-id="8ae48-123">-State</span></span>
<span data-ttu-id="8ae48-124">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8ae48-124">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae48-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ae48-125">-SubscriptionId</span></span>
<span data-ttu-id="8ae48-126">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8ae48-126">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae48-127">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="8ae48-127">-TenantId</span></span>
<span data-ttu-id="8ae48-128">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="8ae48-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="8ae48-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8ae48-129">-Confirm</span></span>
<span data-ttu-id="8ae48-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ae48-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ae48-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ae48-131">-WhatIf</span></span>
<span data-ttu-id="8ae48-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ae48-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ae48-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ae48-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ae48-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae48-134">CommonParameters</span></span>
<span data-ttu-id="8ae48-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ae48-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae48-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ae48-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae48-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ae48-137">INPUTS</span></span>

## <span data-ttu-id="8ae48-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ae48-138">OUTPUTS</span></span>

### <span data-ttu-id="8ae48-139">Microsoft. AzureStack. Management. abbonamenti. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="8ae48-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="8ae48-140">Note</span><span class="sxs-lookup"><span data-stu-id="8ae48-140">NOTES</span></span>

## <span data-ttu-id="8ae48-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ae48-141">RELATED LINKS</span></span>

