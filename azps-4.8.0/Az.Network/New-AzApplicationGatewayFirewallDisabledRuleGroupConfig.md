---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190987"
---
# <span data-ttu-id="5b10a-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="5b10a-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="5b10a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b10a-102">SYNOPSIS</span></span>
<span data-ttu-id="5b10a-103">Crea una nuova configurazione del gruppo di regole disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5b10a-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="5b10a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b10a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b10a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b10a-105">DESCRIPTION</span></span>
<span data-ttu-id="5b10a-106">Il cmdlet **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** crea una nuova configurazione del gruppo di regole disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5b10a-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="5b10a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b10a-107">EXAMPLES</span></span>

### <span data-ttu-id="5b10a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5b10a-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="5b10a-109">Il comando crea una nuova configurazione del gruppo di regole disabilitata per il gruppo di regole denominato "REQUEST-942-APPLICATION-ATTACK-SQLI" con la regola 942130 e la regola 942140 disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5b10a-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="5b10a-110">La nuova configurazione del gruppo di regole disabilitata viene salvata in $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="5b10a-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="5b10a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b10a-111">PARAMETERS</span></span>

### <span data-ttu-id="5b10a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b10a-112">-DefaultProfile</span></span>
<span data-ttu-id="5b10a-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b10a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b10a-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="5b10a-114">-RuleGroupName</span></span>
<span data-ttu-id="5b10a-115">Nome del gruppo di regole che verrà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="5b10a-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="5b10a-116">-Regole</span><span class="sxs-lookup"><span data-stu-id="5b10a-116">-Rules</span></span>
<span data-ttu-id="5b10a-117">Elenco di regole che verranno disabilitate.</span><span class="sxs-lookup"><span data-stu-id="5b10a-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="5b10a-118">Se null, tutte le regole del gruppo di regole verranno disabilitate.</span><span class="sxs-lookup"><span data-stu-id="5b10a-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="5b10a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b10a-119">CommonParameters</span></span>
<span data-ttu-id="5b10a-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b10a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b10a-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b10a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b10a-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b10a-122">INPUTS</span></span>

### <span data-ttu-id="5b10a-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5b10a-123">None</span></span>

## <span data-ttu-id="5b10a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b10a-124">OUTPUTS</span></span>

### <span data-ttu-id="5b10a-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="5b10a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="5b10a-126">Note</span><span class="sxs-lookup"><span data-stu-id="5b10a-126">NOTES</span></span>

## <span data-ttu-id="5b10a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b10a-127">RELATED LINKS</span></span>

[<span data-ttu-id="5b10a-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b10a-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="5b10a-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b10a-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)
