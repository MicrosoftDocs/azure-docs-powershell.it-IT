---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022770"
---
# <span data-ttu-id="19dde-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="19dde-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="19dde-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19dde-102">SYNOPSIS</span></span>
<span data-ttu-id="19dde-103">Crea un ManagedRuleSet per firewallPolicy</span><span class="sxs-lookup"><span data-stu-id="19dde-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="19dde-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19dde-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19dde-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19dde-105">DESCRIPTION</span></span>
<span data-ttu-id="19dde-106">Il **nuovo AzApplicationGatewayFirewallPolicyManagedRuleSet** crea una regole gestite per un criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="19dde-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="19dde-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19dde-107">EXAMPLES</span></span>

### <span data-ttu-id="19dde-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="19dde-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="19dde-109">Crea un ManagedRuleSet con ruleSetType come $ruleSetType, ruleSetVersion come $ruleSetVersion e RuleGroupOverrides come elenco con interi come $ruleGroupOverride 1, $ruleGroupOverride 2 viene assegnato il nuovo ManagedRuleSet a $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="19dde-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="19dde-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19dde-110">PARAMETERS</span></span>

### <span data-ttu-id="19dde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19dde-111">-DefaultProfile</span></span>
<span data-ttu-id="19dde-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19dde-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19dde-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="19dde-113">-RuleGroupOverride</span></span>
<span data-ttu-id="19dde-114">Override del gruppo di regole.</span><span class="sxs-lookup"><span data-stu-id="19dde-114">Rule Group Overrides.</span></span>

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

### <span data-ttu-id="19dde-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="19dde-115">-RuleSetType</span></span>
<span data-ttu-id="19dde-116">Specificare il RuleSetType in un managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="19dde-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="19dde-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="19dde-117">-RuleSetVersion</span></span>
<span data-ttu-id="19dde-118">Specificare il RuleSetVersion in un managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="19dde-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="19dde-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dde-119">CommonParameters</span></span>
<span data-ttu-id="19dde-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19dde-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dde-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19dde-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dde-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19dde-122">INPUTS</span></span>

### <span data-ttu-id="19dde-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="19dde-123">None</span></span>

## <span data-ttu-id="19dde-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19dde-124">OUTPUTS</span></span>

### <span data-ttu-id="19dde-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="19dde-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="19dde-126">Note</span><span class="sxs-lookup"><span data-stu-id="19dde-126">NOTES</span></span>

## <span data-ttu-id="19dde-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19dde-127">RELATED LINKS</span></span>
