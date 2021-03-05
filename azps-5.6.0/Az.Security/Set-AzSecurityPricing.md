---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: f55c42178daacdbf2be80982fb151514372d2d3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986494"
---
# <span data-ttu-id="e1dd7-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="e1dd7-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="e1dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1dd7-102">SYNOPSIS</span></span>

<span data-ttu-id="e1dd7-103">Abilita o disabilita i piani di Azure Defender per una sottoscrizione nel Centro sicurezza di Azure.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="e1dd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1dd7-104">SYNTAX</span></span>

### <span data-ttu-id="e1dd7-105">SubscriptionLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="e1dd7-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1dd7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e1dd7-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1dd7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1dd7-107">DESCRIPTION</span></span>

<span data-ttu-id="e1dd7-108">Abilitare o disabilitare uno qualsiasi dei piani di Azure Defender per una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="e1dd7-109">Per informazioni dettagliate su Azure Defender e sui piani disponibili, vedere [Introduzione ad Azure Defender.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="e1dd7-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="e1dd7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1dd7-110">EXAMPLES</span></span>

### <span data-ttu-id="e1dd7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1dd7-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="e1dd7-112">Abilita **Azure Defender per i server** per la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="e1dd7-113">"Standard" fa riferimento allo stato "Attivo" di un piano di Azure Defender, come mostrato nell'area prezzi e impostazioni del Centro sicurezza di Azure del portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="e1dd7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1dd7-114">PARAMETERS</span></span>

### <span data-ttu-id="e1dd7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1dd7-115">-DefaultProfile</span></span>

<span data-ttu-id="e1dd7-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1dd7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1dd7-117">-InputObject</span></span>

<span data-ttu-id="e1dd7-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-118">Input Object.</span></span>

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

### <span data-ttu-id="e1dd7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e1dd7-119">-Name</span></span>

<span data-ttu-id="e1dd7-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-120">Resource name.</span></span>

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

### <span data-ttu-id="e1dd7-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="e1dd7-121">-PricingTier</span></span>

<span data-ttu-id="e1dd7-122">Pricing Tier.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="e1dd7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1dd7-123">-Confirm</span></span>

<span data-ttu-id="e1dd7-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1dd7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1dd7-125">-WhatIf</span></span>

<span data-ttu-id="e1dd7-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1dd7-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1dd7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1dd7-128">CommonParameters</span></span>

<span data-ttu-id="e1dd7-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1dd7-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1dd7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1dd7-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1dd7-131">INPUTS</span></span>

### <span data-ttu-id="e1dd7-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="e1dd7-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="e1dd7-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1dd7-133">OUTPUTS</span></span>

### <span data-ttu-id="e1dd7-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="e1dd7-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="e1dd7-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1dd7-135">NOTES</span></span>

## <span data-ttu-id="e1dd7-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1dd7-136">RELATED LINKS</span></span>
