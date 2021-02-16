---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179734"
---
# <span data-ttu-id="7136e-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="7136e-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="7136e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7136e-102">SYNOPSIS</span></span>
<span data-ttu-id="7136e-103">Crea una voce managedRuleOverride per la voce RuleGroupOverrideGroup.</span><span class="sxs-lookup"><span data-stu-id="7136e-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="7136e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7136e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7136e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7136e-105">DESCRIPTION</span></span>
<span data-ttu-id="7136e-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** crea una voce ruleOverride.</span><span class="sxs-lookup"><span data-stu-id="7136e-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="7136e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7136e-107">EXAMPLES</span></span>

### <span data-ttu-id="7136e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7136e-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="7136e-109">Crea una voce ruleOverride con RuleId come $ruleId e State come Disabled.</span><span class="sxs-lookup"><span data-stu-id="7136e-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="7136e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7136e-110">PARAMETERS</span></span>

### <span data-ttu-id="7136e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7136e-111">-DefaultProfile</span></span>
<span data-ttu-id="7136e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7136e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7136e-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="7136e-113">-RuleId</span></span>
<span data-ttu-id="7136e-114">Specificare RuleId nella voce della regola di override.</span><span class="sxs-lookup"><span data-stu-id="7136e-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="7136e-115">-State</span><span class="sxs-lookup"><span data-stu-id="7136e-115">-State</span></span>
<span data-ttu-id="7136e-116">Specificare RuleId nella voce della regola di override.</span><span class="sxs-lookup"><span data-stu-id="7136e-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="7136e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7136e-117">CommonParameters</span></span>
<span data-ttu-id="7136e-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7136e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7136e-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7136e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7136e-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="7136e-120">INPUTS</span></span>

### <span data-ttu-id="7136e-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7136e-121">None</span></span>

## <span data-ttu-id="7136e-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7136e-122">OUTPUTS</span></span>

### <span data-ttu-id="7136e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="7136e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="7136e-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="7136e-124">NOTES</span></span>

## <span data-ttu-id="7136e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7136e-125">RELATED LINKS</span></span>
