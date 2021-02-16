---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179774"
---
# <span data-ttu-id="083a8-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="083a8-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="083a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="083a8-102">SYNOPSIS</span></span>
<span data-ttu-id="083a8-103">Creare ManagedRules per i criteri del firewall.</span><span class="sxs-lookup"><span data-stu-id="083a8-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="083a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="083a8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="083a8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="083a8-105">DESCRIPTION</span></span>
<span data-ttu-id="083a8-106">**New-AzApplicationGatewayFirewallPolicyManagedRule** crea una regola gestita per un criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="083a8-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="083a8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="083a8-107">EXAMPLES</span></span>

### <span data-ttu-id="083a8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="083a8-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="083a8-109">Il comando crea regole gestite un elenco di ManagedRuleSet con $managedRuleSet e un elenco di esclusioni con voci come $exclusion 1, $exclusion 2.</span><span class="sxs-lookup"><span data-stu-id="083a8-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="083a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="083a8-110">PARAMETERS</span></span>

### <span data-ttu-id="083a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083a8-111">-DefaultProfile</span></span>
<span data-ttu-id="083a8-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="083a8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="083a8-113">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="083a8-113">-Exclusion</span></span>
<span data-ttu-id="083a8-114">Elenco delle voci di esclusione.</span><span class="sxs-lookup"><span data-stu-id="083a8-114">List of Exclusion Entry.</span></span>

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

### <span data-ttu-id="083a8-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="083a8-115">-ManagedRuleSet</span></span>
<span data-ttu-id="083a8-116">Elenco dei set di regole gestiti.</span><span class="sxs-lookup"><span data-stu-id="083a8-116">List of Managed ruleSets.</span></span>

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

### <span data-ttu-id="083a8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083a8-117">CommonParameters</span></span>
<span data-ttu-id="083a8-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083a8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083a8-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="083a8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083a8-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="083a8-120">INPUTS</span></span>

### <span data-ttu-id="083a8-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="083a8-121">None</span></span>

## <span data-ttu-id="083a8-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="083a8-122">OUTPUTS</span></span>

### <span data-ttu-id="083a8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="083a8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="083a8-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="083a8-124">NOTES</span></span>

## <span data-ttu-id="083a8-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="083a8-125">RELATED LINKS</span></span>
