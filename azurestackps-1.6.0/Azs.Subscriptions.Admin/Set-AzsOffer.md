---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 285b9509241e9035c007f871ac6395008a1f9cde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491217"
---
# <span data-ttu-id="2735f-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="2735f-101">Set-AzsOffer</span></span>

## <span data-ttu-id="2735f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2735f-102">SYNOPSIS</span></span>
<span data-ttu-id="2735f-103">Aggiornare l'offerta.</span><span class="sxs-lookup"><span data-stu-id="2735f-103">Update the offer.</span></span>

## <span data-ttu-id="2735f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2735f-104">SYNTAX</span></span>

### <span data-ttu-id="2735f-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2735f-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2735f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2735f-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2735f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2735f-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2735f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2735f-108">DESCRIPTION</span></span>
<span data-ttu-id="2735f-109">Aggiornare l'offerta.</span><span class="sxs-lookup"><span data-stu-id="2735f-109">Update the offer.</span></span>

## <span data-ttu-id="2735f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2735f-110">EXAMPLES</span></span>

### <span data-ttu-id="2735f-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2735f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="2735f-112">Aggiornare l'offerta.</span><span class="sxs-lookup"><span data-stu-id="2735f-112">Update the offer.</span></span>

## <span data-ttu-id="2735f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2735f-113">PARAMETERS</span></span>

### <span data-ttu-id="2735f-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="2735f-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="2735f-115">Riferimenti a piani per i componenti aggiuntivi che un tenant può acquistare facoltativamente come parte dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="2735f-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2735f-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="2735f-116">-BasePlanIds</span></span>
<span data-ttu-id="2735f-117">Identificatori dei piani di base che diventano disponibili per il tenant immediatamente quando un tenant sottoscrive l'offerta.</span><span class="sxs-lookup"><span data-stu-id="2735f-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2735f-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2735f-118">-Description</span></span>
<span data-ttu-id="2735f-119">Descrizione dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="2735f-119">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2735f-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2735f-120">-DisplayName</span></span>
<span data-ttu-id="2735f-121">Nome visualizzato dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="2735f-121">Display name of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2735f-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="2735f-122">-ExternalReferenceId</span></span>
<span data-ttu-id="2735f-123">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="2735f-123">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2735f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2735f-124">-InputObject</span></span>
<span data-ttu-id="2735f-125">L'oggetto di input di tipo Microsoft. AzureStack. Management. subscriptions. admin. Models. offer.</span><span class="sxs-lookup"><span data-stu-id="2735f-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

```yaml
Type: Offer
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2735f-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2735f-126">-Location</span></span>
<span data-ttu-id="2735f-127">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2735f-127">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2735f-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="2735f-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="2735f-129">Numero massimo di abbonamenti per account.</span><span class="sxs-lookup"><span data-stu-id="2735f-129">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2735f-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="2735f-130">-Name</span></span>
<span data-ttu-id="2735f-131">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="2735f-131">Name of an offer.</span></span>

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

### <span data-ttu-id="2735f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2735f-132">-ResourceGroupName</span></span>
<span data-ttu-id="2735f-133">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2735f-133">The resource group the resource is located under.</span></span>

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

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2735f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2735f-134">-ResourceId</span></span>
<span data-ttu-id="2735f-135">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="2735f-135">The resource id.</span></span>

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

### <span data-ttu-id="2735f-136">-Stato</span><span class="sxs-lookup"><span data-stu-id="2735f-136">-State</span></span>
<span data-ttu-id="2735f-137">Offrire lo stato di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="2735f-137">Offer accessibility state.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2735f-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="2735f-138">-SubscriptionCount</span></span>
<span data-ttu-id="2735f-139">Conteggio corrente dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2735f-139">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2735f-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2735f-140">-Confirm</span></span>
<span data-ttu-id="2735f-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2735f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2735f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2735f-142">-WhatIf</span></span>
<span data-ttu-id="2735f-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2735f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2735f-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2735f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2735f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2735f-145">CommonParameters</span></span>
<span data-ttu-id="2735f-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2735f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2735f-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2735f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2735f-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2735f-148">INPUTS</span></span>

## <span data-ttu-id="2735f-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2735f-149">OUTPUTS</span></span>

### <span data-ttu-id="2735f-150">Microsoft. AzureStack. Management. subscriptions. admin. Models. offer</span><span class="sxs-lookup"><span data-stu-id="2735f-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="2735f-151">Note</span><span class="sxs-lookup"><span data-stu-id="2735f-151">NOTES</span></span>

## <span data-ttu-id="2735f-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2735f-152">RELATED LINKS</span></span>
