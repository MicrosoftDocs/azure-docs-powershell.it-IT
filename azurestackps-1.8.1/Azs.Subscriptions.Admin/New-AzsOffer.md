---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cce59bbbef69f10f39478d784d688a4f1de312fb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859565"
---
# <span data-ttu-id="44750-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="44750-101">New-AzsOffer</span></span>

## <span data-ttu-id="44750-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44750-102">SYNOPSIS</span></span>
<span data-ttu-id="44750-103">Crea una nuova offerta.</span><span class="sxs-lookup"><span data-stu-id="44750-103">Creates a new offer.</span></span>

## <span data-ttu-id="44750-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44750-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44750-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44750-105">DESCRIPTION</span></span>
<span data-ttu-id="44750-106">Creare o aggiornare l'offerta.</span><span class="sxs-lookup"><span data-stu-id="44750-106">Create or update the offer.</span></span>

## <span data-ttu-id="44750-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44750-107">EXAMPLES</span></span>

### <span data-ttu-id="44750-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="44750-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="44750-109">Crea una nuova offerta.</span><span class="sxs-lookup"><span data-stu-id="44750-109">Creates a new offer.</span></span>

## <span data-ttu-id="44750-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44750-110">PARAMETERS</span></span>

### <span data-ttu-id="44750-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="44750-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="44750-112">Riferimenti a piani per i componenti aggiuntivi che un tenant può acquistare facoltativamente come parte dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="44750-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44750-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="44750-113">-BasePlanIds</span></span>
<span data-ttu-id="44750-114">Identificatori dei piani di base che diventano disponibili per il tenant immediatamente quando un tenant sottoscrive l'offerta.</span><span class="sxs-lookup"><span data-stu-id="44750-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44750-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="44750-115">-Description</span></span>
<span data-ttu-id="44750-116">Descrizione dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="44750-116">Description of offer.</span></span>

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

### <span data-ttu-id="44750-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="44750-117">-DisplayName</span></span>
<span data-ttu-id="44750-118">Nome visualizzato dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="44750-118">Display name of offer.</span></span>

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

### <span data-ttu-id="44750-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="44750-119">-ExternalReferenceId</span></span>
<span data-ttu-id="44750-120">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="44750-120">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44750-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="44750-121">-Location</span></span>
<span data-ttu-id="44750-122">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="44750-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44750-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="44750-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="44750-124">Numero massimo di abbonamenti per account.</span><span class="sxs-lookup"><span data-stu-id="44750-124">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44750-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="44750-125">-Name</span></span>
<span data-ttu-id="44750-126">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="44750-126">Name of an offer.</span></span>

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

### <span data-ttu-id="44750-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44750-127">-ResourceGroupName</span></span>
<span data-ttu-id="44750-128">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="44750-128">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44750-129">-Stato</span><span class="sxs-lookup"><span data-stu-id="44750-129">-State</span></span>
<span data-ttu-id="44750-130">Offrire lo stato di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="44750-130">Offer accessibility state.</span></span>
<span data-ttu-id="44750-131">Il valore predefinito è private.</span><span class="sxs-lookup"><span data-stu-id="44750-131">Default value is Private.</span></span>
<span data-ttu-id="44750-132">Questo parametro sarà deprecato in una versione futura</span><span class="sxs-lookup"><span data-stu-id="44750-132">This parameter will be deprecated in a future release</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: Private
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44750-133">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="44750-133">-SubscriptionCount</span></span>
<span data-ttu-id="44750-134">Conteggio corrente dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="44750-134">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44750-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44750-135">-Confirm</span></span>
<span data-ttu-id="44750-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44750-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44750-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44750-137">-WhatIf</span></span>
<span data-ttu-id="44750-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44750-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44750-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44750-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44750-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44750-140">CommonParameters</span></span>
<span data-ttu-id="44750-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44750-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44750-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44750-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44750-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44750-143">INPUTS</span></span>

## <span data-ttu-id="44750-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44750-144">OUTPUTS</span></span>

### <span data-ttu-id="44750-145">Microsoft. AzureStack. Management. subscriptions. admin. Models. offer</span><span class="sxs-lookup"><span data-stu-id="44750-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="44750-146">Note</span><span class="sxs-lookup"><span data-stu-id="44750-146">NOTES</span></span>

## <span data-ttu-id="44750-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44750-147">RELATED LINKS</span></span>

