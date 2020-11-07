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
ms.locfileid: "93858689"
---
# <span data-ttu-id="6533a-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="6533a-101">Set-AzsPlan</span></span>

## <span data-ttu-id="6533a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6533a-102">SYNOPSIS</span></span>
<span data-ttu-id="6533a-103">Aggiorna il piano specificato</span><span class="sxs-lookup"><span data-stu-id="6533a-103">Updates the specified plan</span></span>

## <span data-ttu-id="6533a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6533a-104">SYNTAX</span></span>

### <span data-ttu-id="6533a-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6533a-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6533a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6533a-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6533a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6533a-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6533a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6533a-108">DESCRIPTION</span></span>
<span data-ttu-id="6533a-109">Aggiorna il piano specificato</span><span class="sxs-lookup"><span data-stu-id="6533a-109">Updates the specified plan</span></span>

## <span data-ttu-id="6533a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6533a-110">EXAMPLES</span></span>

### <span data-ttu-id="6533a-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6533a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="6533a-112">Aggiorna il piano specificato</span><span class="sxs-lookup"><span data-stu-id="6533a-112">Updates the specified plan</span></span>

## <span data-ttu-id="6533a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6533a-113">PARAMETERS</span></span>

### <span data-ttu-id="6533a-114">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="6533a-114">-Description</span></span>
<span data-ttu-id="6533a-115">Descrizione del piano.</span><span class="sxs-lookup"><span data-stu-id="6533a-115">Description of the plan.</span></span>

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

### <span data-ttu-id="6533a-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6533a-116">-DisplayName</span></span>
<span data-ttu-id="6533a-117">Nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="6533a-117">Display name.</span></span>

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

### <span data-ttu-id="6533a-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="6533a-118">-ExternalReferenceId</span></span>
<span data-ttu-id="6533a-119">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="6533a-119">External reference identifier.</span></span>

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

### <span data-ttu-id="6533a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6533a-120">-InputObject</span></span>
<span data-ttu-id="6533a-121">L'oggetto di input di tipo Microsoft. AzureStack. Management. subscriptions. admin. Models. Plan.</span><span class="sxs-lookup"><span data-stu-id="6533a-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

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

### <span data-ttu-id="6533a-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6533a-122">-Location</span></span>
<span data-ttu-id="6533a-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6533a-123">Location of the resource.</span></span>

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

### <span data-ttu-id="6533a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6533a-124">-Name</span></span>
<span data-ttu-id="6533a-125">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="6533a-125">Name of the plan.</span></span>

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

### <span data-ttu-id="6533a-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="6533a-126">-QuotaIds</span></span>
<span data-ttu-id="6533a-127">Identificatori di quota nel piano.</span><span class="sxs-lookup"><span data-stu-id="6533a-127">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="6533a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6533a-128">-ResourceGroupName</span></span>
<span data-ttu-id="6533a-129">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6533a-129">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6533a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6533a-130">-ResourceId</span></span>
<span data-ttu-id="6533a-131">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="6533a-131">The resource id.</span></span>

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

### <span data-ttu-id="6533a-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="6533a-132">-SkuIds</span></span>
<span data-ttu-id="6533a-133">Identificatori SKU.</span><span class="sxs-lookup"><span data-stu-id="6533a-133">SKU identifiers.</span></span>

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

### <span data-ttu-id="6533a-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="6533a-134">-SubscriptionCount</span></span>
<span data-ttu-id="6533a-135">Conteggio abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="6533a-135">Subscription count.</span></span>

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

### <span data-ttu-id="6533a-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6533a-136">-Confirm</span></span>
<span data-ttu-id="6533a-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6533a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6533a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6533a-138">-WhatIf</span></span>
<span data-ttu-id="6533a-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6533a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6533a-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6533a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6533a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6533a-141">CommonParameters</span></span>
<span data-ttu-id="6533a-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6533a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6533a-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6533a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6533a-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6533a-144">INPUTS</span></span>

## <span data-ttu-id="6533a-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6533a-145">OUTPUTS</span></span>

### <span data-ttu-id="6533a-146">Microsoft. AzureStack. Management. subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="6533a-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="6533a-147">Note</span><span class="sxs-lookup"><span data-stu-id="6533a-147">NOTES</span></span>

## <span data-ttu-id="6533a-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6533a-148">RELATED LINKS</span></span>

