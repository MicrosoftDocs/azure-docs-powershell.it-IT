---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: b25c25b642f8c912f62f75788e69e96c3ebdc73c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203413"
---
# <span data-ttu-id="7af86-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="7af86-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="7af86-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7af86-102">SYNOPSIS</span></span>
<span data-ttu-id="7af86-103">Crea una nuova regola personalizzata per i criteri firewall di Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7af86-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="7af86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7af86-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7af86-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7af86-105">DESCRIPTION</span></span>
<span data-ttu-id="7af86-106">La **nuova AzApplicationGatewayFirewallCustomRule** crea una regola personalizzata per i criteri di firewall.</span><span class="sxs-lookup"><span data-stu-id="7af86-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="7af86-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7af86-107">EXAMPLES</span></span>

### <span data-ttu-id="7af86-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7af86-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="7af86-109">Il comando crea una nuova regola personalizzata con il nome dell'esempio-regola, priorità 1 e il tipo di regola sarà MatchRule con la condizione definita nella variabile di condizione, l'azione consentirà.</span><span class="sxs-lookup"><span data-stu-id="7af86-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="7af86-110">La nuova regola personalizzata della corrispondenza viene salvata in $customRule.</span><span class="sxs-lookup"><span data-stu-id="7af86-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="7af86-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7af86-111">PARAMETERS</span></span>

### <span data-ttu-id="7af86-112">-Azione</span><span class="sxs-lookup"><span data-stu-id="7af86-112">-Action</span></span>
<span data-ttu-id="7af86-113">Tipo di azioni.</span><span class="sxs-lookup"><span data-stu-id="7af86-113">Type of Actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af86-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af86-114">-DefaultProfile</span></span>
<span data-ttu-id="7af86-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7af86-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7af86-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="7af86-116">-MatchCondition</span></span>
<span data-ttu-id="7af86-117">Elenco delle condizioni di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="7af86-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af86-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7af86-118">-Name</span></span>
<span data-ttu-id="7af86-119">Nome della regola.</span><span class="sxs-lookup"><span data-stu-id="7af86-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="7af86-120">-Priorità</span><span class="sxs-lookup"><span data-stu-id="7af86-120">-Priority</span></span>
<span data-ttu-id="7af86-121">Descrive la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="7af86-121">Describes priority of the rule.</span></span>
<span data-ttu-id="7af86-122">Le regole con un valore inferiore verranno valutate prima di regole con un valore superiore.</span><span class="sxs-lookup"><span data-stu-id="7af86-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af86-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="7af86-123">-RuleType</span></span>
<span data-ttu-id="7af86-124">Descrive il tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="7af86-124">Describes type of rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af86-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af86-125">CommonParameters</span></span>
<span data-ttu-id="7af86-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7af86-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af86-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7af86-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af86-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7af86-128">INPUTS</span></span>

### <span data-ttu-id="7af86-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7af86-129">None</span></span>

## <span data-ttu-id="7af86-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7af86-130">OUTPUTS</span></span>

### <span data-ttu-id="7af86-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="7af86-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="7af86-132">Note</span><span class="sxs-lookup"><span data-stu-id="7af86-132">NOTES</span></span>

## <span data-ttu-id="7af86-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7af86-133">RELATED LINKS</span></span>
