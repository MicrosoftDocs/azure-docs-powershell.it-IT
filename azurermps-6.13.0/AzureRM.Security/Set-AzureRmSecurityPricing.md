---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
ms.openlocfilehash: f5b23c9221fe8d344e9220590283ab7799a0a3fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514811"
---
# <span data-ttu-id="3eddb-101">Set-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="3eddb-101">Set-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="3eddb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3eddb-102">SYNOPSIS</span></span>
<span data-ttu-id="3eddb-103">Imposta il prezzo di Azure Security Center Tier per un ambito.</span><span class="sxs-lookup"><span data-stu-id="3eddb-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eddb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3eddb-104">SYNTAX</span></span>

### <span data-ttu-id="3eddb-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3eddb-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eddb-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="3eddb-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String> -PricingTier <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eddb-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3eddb-107">InputObject</span></span>
```
Set-AzureRmSecurityPricing -InputObject <PSAddPricingInputObject> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eddb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3eddb-108">DESCRIPTION</span></span>
<span data-ttu-id="3eddb-109">Imposta il prezzo di Azure Security Center Tier per un ambito.</span><span class="sxs-lookup"><span data-stu-id="3eddb-109">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="3eddb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3eddb-110">EXAMPLES</span></span>

### <span data-ttu-id="3eddb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3eddb-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="3eddb-112">Imposta il livello di valutazione di Azure Security Center di Subscription su "standard"</span><span class="sxs-lookup"><span data-stu-id="3eddb-112">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="3eddb-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3eddb-113">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="3eddb-114">Imposta il livello di valutazione "myService1" del gruppo di risorse Azure Security Center per i prezzi "standard"</span><span class="sxs-lookup"><span data-stu-id="3eddb-114">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="3eddb-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3eddb-115">PARAMETERS</span></span>

### <span data-ttu-id="3eddb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eddb-116">-DefaultProfile</span></span>
<span data-ttu-id="3eddb-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3eddb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eddb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eddb-118">-InputObject</span></span>
<span data-ttu-id="3eddb-119">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="3eddb-119">Input Object.</span></span>

```yaml
Type: PSAddPricingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eddb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3eddb-120">-Name</span></span>
<span data-ttu-id="3eddb-121">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="3eddb-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eddb-122">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="3eddb-122">-PricingTier</span></span>
<span data-ttu-id="3eddb-123">Livello di prezzo.</span><span class="sxs-lookup"><span data-stu-id="3eddb-123">Pricing Tier.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eddb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eddb-124">-ResourceGroupName</span></span>
<span data-ttu-id="3eddb-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3eddb-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eddb-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3eddb-126">-Confirm</span></span>
<span data-ttu-id="3eddb-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eddb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eddb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eddb-128">-WhatIf</span></span>
<span data-ttu-id="3eddb-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3eddb-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3eddb-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3eddb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eddb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eddb-131">CommonParameters</span></span>
<span data-ttu-id="3eddb-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eddb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eddb-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eddb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eddb-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3eddb-134">INPUTS</span></span>

### <span data-ttu-id="3eddb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3eddb-135">System.String</span></span>
<span data-ttu-id="3eddb-136">Microsoft. Azure. Commands. Security. Cmdlets. pricings. PSAddPricingInputObject</span><span class="sxs-lookup"><span data-stu-id="3eddb-136">Microsoft.Azure.Commands.Security.Cmdlets.Pricings.PSAddPricingInputObject</span></span>

## <span data-ttu-id="3eddb-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3eddb-137">OUTPUTS</span></span>

### <span data-ttu-id="3eddb-138">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="3eddb-138">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="3eddb-139">Note</span><span class="sxs-lookup"><span data-stu-id="3eddb-139">NOTES</span></span>

## <span data-ttu-id="3eddb-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3eddb-140">RELATED LINKS</span></span>
