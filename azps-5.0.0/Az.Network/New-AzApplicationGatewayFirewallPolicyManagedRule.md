---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193215"
---
# <span data-ttu-id="81bdd-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="81bdd-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="81bdd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="81bdd-103">Creare ManagedRules per il criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="81bdd-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="81bdd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81bdd-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81bdd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="81bdd-106">Il **nuovo AzApplicationGatewayFirewallPolicyManagedRule** crea una regole gestite per un criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="81bdd-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="81bdd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81bdd-107">EXAMPLES</span></span>

### <span data-ttu-id="81bdd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="81bdd-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="81bdd-109">Il comando crea regole gestite un elenco di ManagedRuleSet con $managedRuleSet e un elenco di esclusione con le voci come $exclusion 1, $exclusion 2.</span><span class="sxs-lookup"><span data-stu-id="81bdd-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="81bdd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81bdd-110">PARAMETERS</span></span>

### <span data-ttu-id="81bdd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bdd-111">-DefaultProfile</span></span>
<span data-ttu-id="81bdd-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81bdd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81bdd-113">-Esclusione</span><span class="sxs-lookup"><span data-stu-id="81bdd-113">-Exclusion</span></span>
<span data-ttu-id="81bdd-114">Elenco di voci di esclusione.</span><span class="sxs-lookup"><span data-stu-id="81bdd-114">List of Exclusion Entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bdd-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="81bdd-115">-ManagedRuleSet</span></span>
<span data-ttu-id="81bdd-116">Elenco di ruleSet gestiti.</span><span class="sxs-lookup"><span data-stu-id="81bdd-116">List of Managed ruleSets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bdd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bdd-117">CommonParameters</span></span>
<span data-ttu-id="81bdd-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81bdd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bdd-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81bdd-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bdd-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81bdd-120">INPUTS</span></span>

### <span data-ttu-id="81bdd-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="81bdd-121">None</span></span>

## <span data-ttu-id="81bdd-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81bdd-122">OUTPUTS</span></span>

### <span data-ttu-id="81bdd-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="81bdd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="81bdd-124">Note</span><span class="sxs-lookup"><span data-stu-id="81bdd-124">NOTES</span></span>

## <span data-ttu-id="81bdd-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81bdd-125">RELATED LINKS</span></span>