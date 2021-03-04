---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: d8cb1e6f36433168d830c79c2bcbf8b5c259cf32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962686"
---
# <span data-ttu-id="13c0a-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="13c0a-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="13c0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="13c0a-103">Crea un ManagedRuleSet per il firewallPolicy</span><span class="sxs-lookup"><span data-stu-id="13c0a-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="13c0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13c0a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13c0a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="13c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="13c0a-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleSet** crea una regola gestita per un criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="13c0a-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="13c0a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13c0a-107">EXAMPLES</span></span>

### <span data-ttu-id="13c0a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="13c0a-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="13c0a-109">Crea un managedRuleSet con ruleSetType come $ruleSetType, ruleSetVersion as $ruleSetVersion e RuleGroupOverrides come elenco con intere come $ruleGroupOverride 1, $ruleGroupOverride 2 Il nuovo ManagedRuleSet viene assegnato a $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="13c0a-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="13c0a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13c0a-110">PARAMETERS</span></span>

### <span data-ttu-id="13c0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c0a-111">-DefaultProfile</span></span>
<span data-ttu-id="13c0a-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13c0a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13c0a-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="13c0a-113">-RuleGroupOverride</span></span>
<span data-ttu-id="13c0a-114">Override dei gruppi di regole.</span><span class="sxs-lookup"><span data-stu-id="13c0a-114">Rule Group Overrides.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c0a-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="13c0a-115">-RuleSetType</span></span>
<span data-ttu-id="13c0a-116">Specificare RuleSetType in un managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="13c0a-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="13c0a-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="13c0a-117">-RuleSetVersion</span></span>
<span data-ttu-id="13c0a-118">Specificare RuleSetVersion in un managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="13c0a-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="13c0a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c0a-119">CommonParameters</span></span>
<span data-ttu-id="13c0a-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13c0a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c0a-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13c0a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c0a-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="13c0a-122">INPUTS</span></span>

### <span data-ttu-id="13c0a-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="13c0a-123">None</span></span>

## <span data-ttu-id="13c0a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13c0a-124">OUTPUTS</span></span>

### <span data-ttu-id="13c0a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="13c0a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="13c0a-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="13c0a-126">NOTES</span></span>

## <span data-ttu-id="13c0a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13c0a-127">RELATED LINKS</span></span>
