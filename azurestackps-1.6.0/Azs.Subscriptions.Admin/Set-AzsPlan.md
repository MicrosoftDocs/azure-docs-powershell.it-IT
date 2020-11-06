---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f03365a81fc53af14e3fc9e686504ef3e4387c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491210"
---
# <span data-ttu-id="41f45-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="41f45-101">Set-AzsPlan</span></span>

## <span data-ttu-id="41f45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41f45-102">SYNOPSIS</span></span>
<span data-ttu-id="41f45-103">Aggiorna il piano specificato</span><span class="sxs-lookup"><span data-stu-id="41f45-103">Updates the specified plan</span></span>

## <span data-ttu-id="41f45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41f45-104">SYNTAX</span></span>

### <span data-ttu-id="41f45-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41f45-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41f45-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="41f45-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41f45-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="41f45-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41f45-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41f45-108">DESCRIPTION</span></span>
<span data-ttu-id="41f45-109">Aggiorna il piano specificato</span><span class="sxs-lookup"><span data-stu-id="41f45-109">Updates the specified plan</span></span>

## <span data-ttu-id="41f45-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41f45-110">EXAMPLES</span></span>

### <span data-ttu-id="41f45-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="41f45-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="41f45-112">Aggiorna il piano specificato</span><span class="sxs-lookup"><span data-stu-id="41f45-112">Updates the specified plan</span></span>

## <span data-ttu-id="41f45-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41f45-113">PARAMETERS</span></span>

### <span data-ttu-id="41f45-114">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="41f45-114">-Description</span></span>
<span data-ttu-id="41f45-115">Descrizione del piano.</span><span class="sxs-lookup"><span data-stu-id="41f45-115">Description of the plan.</span></span>

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

### <span data-ttu-id="41f45-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="41f45-116">-DisplayName</span></span>
<span data-ttu-id="41f45-117">Nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="41f45-117">Display name.</span></span>

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

### <span data-ttu-id="41f45-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="41f45-118">-ExternalReferenceId</span></span>
<span data-ttu-id="41f45-119">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="41f45-119">External reference identifier.</span></span>

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

### <span data-ttu-id="41f45-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41f45-120">-InputObject</span></span>
<span data-ttu-id="41f45-121">L'oggetto di input di tipo Microsoft. AzureStack. Management. subscriptions. admin. Models. Plan.</span><span class="sxs-lookup"><span data-stu-id="41f45-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

```yaml
Type: Plan
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41f45-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="41f45-122">-Location</span></span>
<span data-ttu-id="41f45-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="41f45-123">Location of the resource.</span></span>

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

### <span data-ttu-id="41f45-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="41f45-124">-Name</span></span>
<span data-ttu-id="41f45-125">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="41f45-125">Name of the plan.</span></span>

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

### <span data-ttu-id="41f45-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="41f45-126">-QuotaIds</span></span>
<span data-ttu-id="41f45-127">Identificatori di quota nel piano.</span><span class="sxs-lookup"><span data-stu-id="41f45-127">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="41f45-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f45-128">-ResourceGroupName</span></span>
<span data-ttu-id="41f45-129">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="41f45-129">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="41f45-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41f45-130">-ResourceId</span></span>
<span data-ttu-id="41f45-131">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="41f45-131">The resource id.</span></span>

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

### <span data-ttu-id="41f45-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="41f45-132">-SkuIds</span></span>
<span data-ttu-id="41f45-133">Identificatori SKU.</span><span class="sxs-lookup"><span data-stu-id="41f45-133">SKU identifiers.</span></span>

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

### <span data-ttu-id="41f45-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="41f45-134">-SubscriptionCount</span></span>
<span data-ttu-id="41f45-135">Conteggio abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="41f45-135">Subscription count.</span></span>

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

### <span data-ttu-id="41f45-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="41f45-136">-Confirm</span></span>
<span data-ttu-id="41f45-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41f45-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41f45-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41f45-138">-WhatIf</span></span>
<span data-ttu-id="41f45-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41f45-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41f45-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41f45-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41f45-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f45-141">CommonParameters</span></span>
<span data-ttu-id="41f45-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41f45-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f45-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41f45-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f45-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41f45-144">INPUTS</span></span>

## <span data-ttu-id="41f45-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41f45-145">OUTPUTS</span></span>

### <span data-ttu-id="41f45-146">Microsoft. AzureStack. Management. subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="41f45-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="41f45-147">Note</span><span class="sxs-lookup"><span data-stu-id="41f45-147">NOTES</span></span>

## <span data-ttu-id="41f45-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41f45-148">RELATED LINKS</span></span>

