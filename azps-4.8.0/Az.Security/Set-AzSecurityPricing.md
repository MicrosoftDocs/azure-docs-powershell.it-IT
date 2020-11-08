---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: e9dfe0e7ed4612ca99a2decf3aa91b521a7e9664
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188835"
---
# <span data-ttu-id="06fb0-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="06fb0-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="06fb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="06fb0-103">Imposta il prezzo di Azure Security Center Tier per un ambito.</span><span class="sxs-lookup"><span data-stu-id="06fb0-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="06fb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06fb0-104">SYNTAX</span></span>

### <span data-ttu-id="06fb0-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06fb0-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06fb0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="06fb0-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06fb0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06fb0-107">DESCRIPTION</span></span>
<span data-ttu-id="06fb0-108">Imposta il prezzo di Azure Security Center Tier per un ambito.</span><span class="sxs-lookup"><span data-stu-id="06fb0-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="06fb0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06fb0-109">EXAMPLES</span></span>

### <span data-ttu-id="06fb0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="06fb0-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="06fb0-111">Imposta il livello di valutazione di Azure Security Center di Subscription su "standard"</span><span class="sxs-lookup"><span data-stu-id="06fb0-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>


## <span data-ttu-id="06fb0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06fb0-112">PARAMETERS</span></span>

### <span data-ttu-id="06fb0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06fb0-113">-DefaultProfile</span></span>
<span data-ttu-id="06fb0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06fb0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06fb0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06fb0-115">-InputObject</span></span>
<span data-ttu-id="06fb0-116">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="06fb0-116">Input Object.</span></span>

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

### <span data-ttu-id="06fb0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="06fb0-117">-Name</span></span>
<span data-ttu-id="06fb0-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="06fb0-118">Resource name.</span></span>

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

### <span data-ttu-id="06fb0-119">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="06fb0-119">-PricingTier</span></span>
<span data-ttu-id="06fb0-120">Livello di prezzo.</span><span class="sxs-lookup"><span data-stu-id="06fb0-120">Pricing Tier.</span></span>

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

### <span data-ttu-id="06fb0-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06fb0-121">-Confirm</span></span>
<span data-ttu-id="06fb0-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06fb0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06fb0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06fb0-123">-WhatIf</span></span>
<span data-ttu-id="06fb0-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06fb0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06fb0-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06fb0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06fb0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06fb0-126">CommonParameters</span></span>
<span data-ttu-id="06fb0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06fb0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06fb0-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06fb0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06fb0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06fb0-129">INPUTS</span></span>

### <span data-ttu-id="06fb0-130">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="06fb0-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="06fb0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06fb0-131">OUTPUTS</span></span>

### <span data-ttu-id="06fb0-132">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="06fb0-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="06fb0-133">Note</span><span class="sxs-lookup"><span data-stu-id="06fb0-133">NOTES</span></span>

## <span data-ttu-id="06fb0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06fb0-134">RELATED LINKS</span></span>
