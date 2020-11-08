---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: af51b5d864591f868db2ae588eed1d727fc53239
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021713"
---
# <span data-ttu-id="ef344-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="ef344-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="ef344-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef344-102">SYNOPSIS</span></span>
<span data-ttu-id="ef344-103">Imposta il prezzo di Azure Security Center Tier per un ambito.</span><span class="sxs-lookup"><span data-stu-id="ef344-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="ef344-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef344-104">SYNTAX</span></span>

### <span data-ttu-id="ef344-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef344-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef344-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ef344-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef344-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef344-107">DESCRIPTION</span></span>
<span data-ttu-id="ef344-108">Imposta il prezzo di Azure Security Center Tier per un ambito.</span><span class="sxs-lookup"><span data-stu-id="ef344-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="ef344-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef344-109">EXAMPLES</span></span>

### <span data-ttu-id="ef344-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef344-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="ef344-111">Imposta il livello di valutazione di Azure Security Center di Subscription su "standard"</span><span class="sxs-lookup"><span data-stu-id="ef344-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="ef344-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ef344-112">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="ef344-113">Imposta il livello di valutazione "myService1" del gruppo di risorse Azure Security Center per i prezzi "standard"</span><span class="sxs-lookup"><span data-stu-id="ef344-113">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="ef344-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef344-114">PARAMETERS</span></span>

### <span data-ttu-id="ef344-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef344-115">-DefaultProfile</span></span>
<span data-ttu-id="ef344-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef344-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef344-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef344-117">-InputObject</span></span>
<span data-ttu-id="ef344-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="ef344-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef344-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef344-119">-Name</span></span>
<span data-ttu-id="ef344-120">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="ef344-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef344-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="ef344-121">-PricingTier</span></span>
<span data-ttu-id="ef344-122">Livello di prezzo.</span><span class="sxs-lookup"><span data-stu-id="ef344-122">Pricing Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef344-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ef344-123">-Confirm</span></span>
<span data-ttu-id="ef344-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef344-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef344-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef344-125">-WhatIf</span></span>
<span data-ttu-id="ef344-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef344-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef344-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef344-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef344-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef344-128">CommonParameters</span></span>
<span data-ttu-id="ef344-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef344-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef344-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef344-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef344-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef344-131">INPUTS</span></span>

### <span data-ttu-id="ef344-132">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="ef344-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="ef344-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef344-133">OUTPUTS</span></span>

### <span data-ttu-id="ef344-134">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="ef344-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="ef344-135">Note</span><span class="sxs-lookup"><span data-stu-id="ef344-135">NOTES</span></span>

## <span data-ttu-id="ef344-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef344-136">RELATED LINKS</span></span>
