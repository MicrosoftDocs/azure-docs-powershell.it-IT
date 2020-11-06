---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 106293e9d959aefe25ae3e4b27519639a39193d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491209"
---
# <span data-ttu-id="aa337-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="aa337-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="aa337-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa337-102">SYNOPSIS</span></span>
<span data-ttu-id="aa337-103">Aggiorna l'abbonamento utente specificato</span><span class="sxs-lookup"><span data-stu-id="aa337-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="aa337-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa337-104">SYNTAX</span></span>

### <span data-ttu-id="aa337-105">Set (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa337-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa337-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa337-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa337-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="aa337-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa337-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa337-108">DESCRIPTION</span></span>
<span data-ttu-id="aa337-109">Aggiorna l'abbonamento utente specificato</span><span class="sxs-lookup"><span data-stu-id="aa337-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="aa337-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa337-110">EXAMPLES</span></span>

### <span data-ttu-id="aa337-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aa337-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="aa337-112">Aggiorna un abbonamento</span><span class="sxs-lookup"><span data-stu-id="aa337-112">Updates a subscription</span></span>

## <span data-ttu-id="aa337-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa337-113">PARAMETERS</span></span>

### <span data-ttu-id="aa337-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa337-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="aa337-115">Identificatore dell'abbonamento a DelegatedProvider padre.</span><span class="sxs-lookup"><span data-stu-id="aa337-115">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="aa337-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="aa337-116">-DisplayName</span></span>
<span data-ttu-id="aa337-117">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="aa337-117">Subscription name.</span></span>

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

### <span data-ttu-id="aa337-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="aa337-118">-ExternalReferenceId</span></span>
<span data-ttu-id="aa337-119">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="aa337-119">External reference identifier.</span></span>

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

### <span data-ttu-id="aa337-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa337-120">-InputObject</span></span>
<span data-ttu-id="aa337-121">L'oggetto di input di tipo Microsoft. AzureStack. Management. Network. admin. Models. quota.</span><span class="sxs-lookup"><span data-stu-id="aa337-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

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

### <span data-ttu-id="aa337-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="aa337-122">-Location</span></span>
<span data-ttu-id="aa337-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="aa337-123">Location of the resource.</span></span>

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

### <span data-ttu-id="aa337-124">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="aa337-124">-OfferId</span></span>
<span data-ttu-id="aa337-125">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="aa337-125">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="aa337-126">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="aa337-126">-Owner</span></span>
<span data-ttu-id="aa337-127">Proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="aa337-127">Subscription owner.</span></span>

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

### <span data-ttu-id="aa337-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa337-128">-ResourceId</span></span>
<span data-ttu-id="aa337-129">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="aa337-129">The resource ID.</span></span>

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

### <span data-ttu-id="aa337-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="aa337-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="aa337-131">Tipo di gestione risorse di routing.</span><span class="sxs-lookup"><span data-stu-id="aa337-131">Routing resource manager type.</span></span>

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

### <span data-ttu-id="aa337-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="aa337-132">-State</span></span>
<span data-ttu-id="aa337-133">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="aa337-133">Subscription state.</span></span>

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

### <span data-ttu-id="aa337-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa337-134">-SubscriptionId</span></span>
<span data-ttu-id="aa337-135">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="aa337-135">Subscription identifier.</span></span>

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

### <span data-ttu-id="aa337-136">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="aa337-136">-TenantId</span></span>
<span data-ttu-id="aa337-137">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="aa337-137">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="aa337-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa337-138">-Confirm</span></span>
<span data-ttu-id="aa337-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa337-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa337-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa337-140">-WhatIf</span></span>
<span data-ttu-id="aa337-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa337-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa337-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa337-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa337-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa337-143">CommonParameters</span></span>
<span data-ttu-id="aa337-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa337-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa337-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa337-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa337-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa337-146">INPUTS</span></span>

## <span data-ttu-id="aa337-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa337-147">OUTPUTS</span></span>

### <span data-ttu-id="aa337-148">Microsoft. AzureStack. Management. abbonamenti. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="aa337-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="aa337-149">Note</span><span class="sxs-lookup"><span data-stu-id="aa337-149">NOTES</span></span>

## <span data-ttu-id="aa337-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa337-150">RELATED LINKS</span></span>

