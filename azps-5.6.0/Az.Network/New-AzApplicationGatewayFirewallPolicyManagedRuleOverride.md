---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: 31c12fd53c8aa6c886ab5e26a8c35996045335e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992640"
---
# <span data-ttu-id="8a2d8-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="8a2d8-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="8a2d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a2d8-102">SYNOPSIS</span></span>
<span data-ttu-id="8a2d8-103">Crea una voce managedRuleOverride per la voce RuleGroupOverrideGroup.</span><span class="sxs-lookup"><span data-stu-id="8a2d8-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="8a2d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a2d8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a2d8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8a2d8-105">DESCRIPTION</span></span>
<span data-ttu-id="8a2d8-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** crea una voce ruleOverride.</span><span class="sxs-lookup"><span data-stu-id="8a2d8-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="8a2d8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a2d8-107">EXAMPLES</span></span>

### <span data-ttu-id="8a2d8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8a2d8-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="8a2d8-109">Crea una voce ruleOverride con RuleId come $ruleId e State come Disabled.</span><span class="sxs-lookup"><span data-stu-id="8a2d8-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="8a2d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a2d8-110">PARAMETERS</span></span>

### <span data-ttu-id="8a2d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a2d8-111">-DefaultProfile</span></span>
<span data-ttu-id="8a2d8-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a2d8-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="8a2d8-113">-RuleId</span></span>
<span data-ttu-id="8a2d8-114">Specificare RuleId nella voce della regola di override.</span><span class="sxs-lookup"><span data-stu-id="8a2d8-114">Specify the RuleId in override rule entry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2d8-115">-State</span><span class="sxs-lookup"><span data-stu-id="8a2d8-115">-State</span></span>
<span data-ttu-id="8a2d8-116">Specificare RuleId nella voce della regola di override.</span><span class="sxs-lookup"><span data-stu-id="8a2d8-116">Specify the RuleId in override rule entry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled

Required: False
Position: Named
Default value: Disabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2d8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a2d8-117">CommonParameters</span></span>
<span data-ttu-id="8a2d8-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a2d8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a2d8-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8a2d8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a2d8-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="8a2d8-120">INPUTS</span></span>

### <span data-ttu-id="8a2d8-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8a2d8-121">None</span></span>

## <span data-ttu-id="8a2d8-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a2d8-122">OUTPUTS</span></span>

### <span data-ttu-id="8a2d8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="8a2d8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="8a2d8-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="8a2d8-124">NOTES</span></span>

## <span data-ttu-id="8a2d8-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a2d8-125">RELATED LINKS</span></span>
