---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348f7dc1f4719e70a73902b59cf335bb22015bec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030598"
---
# <span data-ttu-id="2d7c7-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="2d7c7-101">New-AzsPlan</span></span>

## <span data-ttu-id="2d7c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d7c7-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7c7-103">Crea un nuovo piano</span><span class="sxs-lookup"><span data-stu-id="2d7c7-103">Creates a new plan</span></span>

## <span data-ttu-id="2d7c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d7c7-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d7c7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d7c7-105">DESCRIPTION</span></span>
<span data-ttu-id="2d7c7-106">Crea un nuovo piano</span><span class="sxs-lookup"><span data-stu-id="2d7c7-106">Creates a new plan</span></span>

## <span data-ttu-id="2d7c7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d7c7-107">EXAMPLES</span></span>

### <span data-ttu-id="2d7c7-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2d7c7-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="2d7c7-109">Crea un nuovo piano</span><span class="sxs-lookup"><span data-stu-id="2d7c7-109">Creates a new plan</span></span>

## <span data-ttu-id="2d7c7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d7c7-110">PARAMETERS</span></span>

### <span data-ttu-id="2d7c7-111">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d7c7-111">-Description</span></span>
<span data-ttu-id="2d7c7-112">Descrizione del piano.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-112">Description of the plan.</span></span>

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

### <span data-ttu-id="2d7c7-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2d7c7-113">-DisplayName</span></span>
<span data-ttu-id="2d7c7-114">Nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-114">Display name.</span></span>

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

### <span data-ttu-id="2d7c7-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="2d7c7-115">-ExternalReferenceId</span></span>
<span data-ttu-id="2d7c7-116">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-116">External reference identifier.</span></span>

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

### <span data-ttu-id="2d7c7-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2d7c7-117">-Location</span></span>
<span data-ttu-id="2d7c7-118">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-118">Location of the resource.</span></span>

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

### <span data-ttu-id="2d7c7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d7c7-119">-Name</span></span>
<span data-ttu-id="2d7c7-120">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-120">Name of the plan.</span></span>

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

### <span data-ttu-id="2d7c7-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="2d7c7-121">-QuotaIds</span></span>
<span data-ttu-id="2d7c7-122">Identificatori di quota nel piano.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-122">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d7c7-124">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="2d7c7-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="2d7c7-125">-SkuIds</span></span>
<span data-ttu-id="2d7c7-126">Identificatori SKU.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-126">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7c7-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="2d7c7-127">-SubscriptionCount</span></span>
<span data-ttu-id="2d7c7-128">Conteggio abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-128">Subscription count.</span></span>

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

### <span data-ttu-id="2d7c7-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d7c7-129">-Confirm</span></span>
<span data-ttu-id="2d7c7-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d7c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d7c7-131">-WhatIf</span></span>
<span data-ttu-id="2d7c7-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d7c7-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d7c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7c7-134">CommonParameters</span></span>
<span data-ttu-id="2d7c7-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d7c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7c7-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d7c7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7c7-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d7c7-137">INPUTS</span></span>

## <span data-ttu-id="2d7c7-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d7c7-138">OUTPUTS</span></span>

### <span data-ttu-id="2d7c7-139">Microsoft. AzureStack. Management. subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="2d7c7-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="2d7c7-140">Note</span><span class="sxs-lookup"><span data-stu-id="2d7c7-140">NOTES</span></span>

## <span data-ttu-id="2d7c7-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d7c7-141">RELATED LINKS</span></span>

