---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192352"
---
# <span data-ttu-id="e0d46-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e0d46-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="e0d46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0d46-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d46-103">Crea la voce RuleGroupOverride in ManagedRuleSets per il criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="e0d46-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="e0d46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0d46-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0d46-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0d46-105">DESCRIPTION</span></span>
<span data-ttu-id="e0d46-106">La **nuova AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** crea una voce ruleGroupOverride in un managedRuleSet per un criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="e0d46-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="e0d46-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0d46-107">EXAMPLES</span></span>

### <span data-ttu-id="e0d46-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e0d46-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="e0d46-109">Crea una voce di RuleGroupOverride con il nome del gruppo come $ruleName e le regole come $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="e0d46-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="e0d46-110">Assegna lo stesso a $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="e0d46-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="e0d46-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0d46-111">PARAMETERS</span></span>

### <span data-ttu-id="e0d46-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d46-112">-DefaultProfile</span></span>
<span data-ttu-id="e0d46-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d46-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0d46-114">-Regola</span><span class="sxs-lookup"><span data-stu-id="e0d46-114">-Rule</span></span>
<span data-ttu-id="e0d46-115">Elenco di regole.</span><span class="sxs-lookup"><span data-stu-id="e0d46-115">List of Rules.</span></span>

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

### <span data-ttu-id="e0d46-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d46-116">-RuleGroupName</span></span>
<span data-ttu-id="e0d46-117">Specifica ruleGroupName in una voce di override RuleGroup.</span><span class="sxs-lookup"><span data-stu-id="e0d46-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="e0d46-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d46-118">CommonParameters</span></span>
<span data-ttu-id="e0d46-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0d46-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d46-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0d46-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d46-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0d46-121">INPUTS</span></span>

### <span data-ttu-id="e0d46-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e0d46-122">None</span></span>

## <span data-ttu-id="e0d46-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0d46-123">OUTPUTS</span></span>

### <span data-ttu-id="e0d46-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e0d46-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="e0d46-125">Note</span><span class="sxs-lookup"><span data-stu-id="e0d46-125">NOTES</span></span>

## <span data-ttu-id="e0d46-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0d46-126">RELATED LINKS</span></span>
