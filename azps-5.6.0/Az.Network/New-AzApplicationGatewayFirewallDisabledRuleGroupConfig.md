---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5a96ea5ac1ded346e289d44f54762909d5f96e31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952190"
---
# <span data-ttu-id="5cbbe-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="5cbbe-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="5cbbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cbbe-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbbe-103">Crea una nuova configurazione di gruppo di regole disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5cbbe-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="5cbbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cbbe-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cbbe-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5cbbe-105">DESCRIPTION</span></span>
<span data-ttu-id="5cbbe-106">Il cmdlet **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** crea una nuova configurazione di gruppo di regole disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5cbbe-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="5cbbe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cbbe-107">EXAMPLES</span></span>

### <span data-ttu-id="5cbbe-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5cbbe-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="5cbbe-109">Il comando crea una nuova configurazione di gruppo di regole disabilitata per il gruppo di regole "REQUEST-942-APPLICATION-ATTACK-SQLI" con la regola 942130 e la regola 942140 disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5cbbe-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="5cbbe-110">La nuova configurazione del gruppo di regole disabilitata viene salvata in $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="5cbbe-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="5cbbe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cbbe-111">PARAMETERS</span></span>

### <span data-ttu-id="5cbbe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbbe-112">-DefaultProfile</span></span>
<span data-ttu-id="5cbbe-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbbe-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cbbe-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="5cbbe-114">-RuleGroupName</span></span>
<span data-ttu-id="5cbbe-115">Nome del gruppo di regole che verrà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="5cbbe-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="5cbbe-116">-Rules</span><span class="sxs-lookup"><span data-stu-id="5cbbe-116">-Rules</span></span>
<span data-ttu-id="5cbbe-117">L'elenco delle regole che verranno disabilitate.</span><span class="sxs-lookup"><span data-stu-id="5cbbe-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="5cbbe-118">Se Null, tutte le regole del gruppo di regole verranno disabilitate.</span><span class="sxs-lookup"><span data-stu-id="5cbbe-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbbe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbbe-119">CommonParameters</span></span>
<span data-ttu-id="5cbbe-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbbe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbbe-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cbbe-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbbe-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="5cbbe-122">INPUTS</span></span>

### <span data-ttu-id="5cbbe-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5cbbe-123">None</span></span>

## <span data-ttu-id="5cbbe-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cbbe-124">OUTPUTS</span></span>

### <span data-ttu-id="5cbbe-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="5cbbe-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="5cbbe-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="5cbbe-126">NOTES</span></span>

## <span data-ttu-id="5cbbe-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cbbe-127">RELATED LINKS</span></span>

[<span data-ttu-id="5cbbe-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cbbe-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="5cbbe-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cbbe-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

