---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179750"
---
# <span data-ttu-id="05794-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="05794-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="05794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05794-102">SYNOPSIS</span></span>
<span data-ttu-id="05794-103">Crea la voce RuleGroupOverride in ManagedRuleSets per il criterio del firewall.</span><span class="sxs-lookup"><span data-stu-id="05794-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="05794-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05794-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05794-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05794-105">DESCRIPTION</span></span>
<span data-ttu-id="05794-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** crea una voce ruleGroupOverride in un managedRuleSet per un criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="05794-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="05794-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05794-107">EXAMPLES</span></span>

### <span data-ttu-id="05794-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="05794-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="05794-109">Crea una voce RuleGroupOverride con il nome del gruppo $ruleName e Rules come $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="05794-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="05794-110">Assegna lo stesso valore a $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="05794-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="05794-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05794-111">PARAMETERS</span></span>

### <span data-ttu-id="05794-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05794-112">-DefaultProfile</span></span>
<span data-ttu-id="05794-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05794-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05794-114">-Rule</span><span class="sxs-lookup"><span data-stu-id="05794-114">-Rule</span></span>
<span data-ttu-id="05794-115">Elenco delle regole.</span><span class="sxs-lookup"><span data-stu-id="05794-115">List of Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05794-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="05794-116">-RuleGroupName</span></span>
<span data-ttu-id="05794-117">Specificare ruleGroupName in una voce RuleGroup.</span><span class="sxs-lookup"><span data-stu-id="05794-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="05794-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05794-118">CommonParameters</span></span>
<span data-ttu-id="05794-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05794-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05794-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="05794-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05794-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="05794-121">INPUTS</span></span>

### <span data-ttu-id="05794-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="05794-122">None</span></span>

## <span data-ttu-id="05794-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05794-123">OUTPUTS</span></span>

### <span data-ttu-id="05794-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="05794-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="05794-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="05794-125">NOTES</span></span>

## <span data-ttu-id="05794-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05794-126">RELATED LINKS</span></span>
