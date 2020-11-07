---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ef53ac2d32d71a68b7fe342f5d2d0cafc2a193f8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859489"
---
# <span data-ttu-id="7bc6f-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="7bc6f-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="7bc6f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7bc6f-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc6f-103">Aggiorna l'abbonamento utente specificato</span><span class="sxs-lookup"><span data-stu-id="7bc6f-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="7bc6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bc6f-104">SYNTAX</span></span>

### <span data-ttu-id="7bc6f-105">Set (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7bc6f-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bc6f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bc6f-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bc6f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7bc6f-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bc6f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bc6f-108">DESCRIPTION</span></span>
<span data-ttu-id="7bc6f-109">Aggiorna l'abbonamento utente specificato</span><span class="sxs-lookup"><span data-stu-id="7bc6f-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="7bc6f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bc6f-110">EXAMPLES</span></span>

### <span data-ttu-id="7bc6f-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7bc6f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="7bc6f-112">Aggiorna un abbonamento</span><span class="sxs-lookup"><span data-stu-id="7bc6f-112">Updates a subscription</span></span>

## <span data-ttu-id="7bc6f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7bc6f-113">PARAMETERS</span></span>

### <span data-ttu-id="7bc6f-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bc6f-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="7bc6f-115">Identificatore dell'abbonamento a DelegatedProvider padre.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-115">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="7bc6f-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7bc6f-116">-DisplayName</span></span>
<span data-ttu-id="7bc6f-117">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-117">Subscription name.</span></span>

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

### <span data-ttu-id="7bc6f-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="7bc6f-118">-ExternalReferenceId</span></span>
<span data-ttu-id="7bc6f-119">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-119">External reference identifier.</span></span>

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

### <span data-ttu-id="7bc6f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bc6f-120">-InputObject</span></span>
<span data-ttu-id="7bc6f-121">L'oggetto di input di tipo Microsoft. AzureStack. Management. Network. admin. Models. quota.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

```yaml
Type: Subscription
Parameter Sets: InputObject
Aliases: Subscription

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc6f-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7bc6f-122">-Location</span></span>
<span data-ttu-id="7bc6f-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-123">Location of the resource.</span></span>

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

### <span data-ttu-id="7bc6f-124">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="7bc6f-124">-OfferId</span></span>
<span data-ttu-id="7bc6f-125">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-125">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="7bc6f-126">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="7bc6f-126">-Owner</span></span>
<span data-ttu-id="7bc6f-127">Proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-127">Subscription owner.</span></span>

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

### <span data-ttu-id="7bc6f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bc6f-128">-ResourceId</span></span>
<span data-ttu-id="7bc6f-129">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-129">The resource ID.</span></span>

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

### <span data-ttu-id="7bc6f-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="7bc6f-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="7bc6f-131">Tipo di gestione risorse di routing.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-131">Routing resource manager type.</span></span>

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

### <span data-ttu-id="7bc6f-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="7bc6f-132">-State</span></span>
<span data-ttu-id="7bc6f-133">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-133">Subscription state.</span></span>

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

### <span data-ttu-id="7bc6f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bc6f-134">-SubscriptionId</span></span>
<span data-ttu-id="7bc6f-135">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-135">Subscription identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc6f-136">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="7bc6f-136">-TenantId</span></span>
<span data-ttu-id="7bc6f-137">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-137">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="7bc6f-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7bc6f-138">-Confirm</span></span>
<span data-ttu-id="7bc6f-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bc6f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bc6f-140">-WhatIf</span></span>
<span data-ttu-id="7bc6f-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bc6f-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bc6f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc6f-143">CommonParameters</span></span>
<span data-ttu-id="7bc6f-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc6f-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc6f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc6f-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7bc6f-146">INPUTS</span></span>

## <span data-ttu-id="7bc6f-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bc6f-147">OUTPUTS</span></span>

### <span data-ttu-id="7bc6f-148">Microsoft. AzureStack. Management. abbonamenti. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="7bc6f-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="7bc6f-149">Note</span><span class="sxs-lookup"><span data-stu-id="7bc6f-149">NOTES</span></span>

## <span data-ttu-id="7bc6f-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bc6f-150">RELATED LINKS</span></span>

