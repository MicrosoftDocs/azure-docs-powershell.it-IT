---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: b25c25b642f8c912f62f75788e69e96c3ebdc73c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179791"
---
# <span data-ttu-id="3f81c-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="3f81c-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="3f81c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f81c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f81c-103">Crea una nuova regola personalizzata per il criterio firewall del gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3f81c-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="3f81c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f81c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f81c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3f81c-105">DESCRIPTION</span></span>
<span data-ttu-id="3f81c-106">**New-AzApplicationGatewayFirewallCustomRule** crea una regola personalizzata per i criteri del firewall.</span><span class="sxs-lookup"><span data-stu-id="3f81c-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="3f81c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f81c-107">EXAMPLES</span></span>

### <span data-ttu-id="3f81c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3f81c-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="3f81c-109">Il comando crea una nuova regola personalizzata con il nome della regola di esempio, la priorità 1 e il tipo di regola sarà MatchRule con la condizione definita nella variabile della condizione. L'azione sarà consentita.</span><span class="sxs-lookup"><span data-stu-id="3f81c-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="3f81c-110">La nuova regola personalizzata di corrispondenza viene salvata in $customRule.</span><span class="sxs-lookup"><span data-stu-id="3f81c-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="3f81c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f81c-111">PARAMETERS</span></span>

### <span data-ttu-id="3f81c-112">-Action</span><span class="sxs-lookup"><span data-stu-id="3f81c-112">-Action</span></span>
<span data-ttu-id="3f81c-113">Tipo di azioni.</span><span class="sxs-lookup"><span data-stu-id="3f81c-113">Type of Actions.</span></span>

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

### <span data-ttu-id="3f81c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f81c-114">-DefaultProfile</span></span>
<span data-ttu-id="3f81c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f81c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f81c-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="3f81c-116">-MatchCondition</span></span>
<span data-ttu-id="3f81c-117">Elenco di condizioni di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="3f81c-117">List of match conditions.</span></span>

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

### <span data-ttu-id="3f81c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3f81c-118">-Name</span></span>
<span data-ttu-id="3f81c-119">Nome della regola.</span><span class="sxs-lookup"><span data-stu-id="3f81c-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="3f81c-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="3f81c-120">-Priority</span></span>
<span data-ttu-id="3f81c-121">Descrive la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="3f81c-121">Describes priority of the rule.</span></span>
<span data-ttu-id="3f81c-122">Le regole con un valore inferiore verranno valutate prima delle regole con un valore più alto.</span><span class="sxs-lookup"><span data-stu-id="3f81c-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

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

### <span data-ttu-id="3f81c-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="3f81c-123">-RuleType</span></span>
<span data-ttu-id="3f81c-124">Descrive il tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="3f81c-124">Describes type of rule.</span></span>

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

### <span data-ttu-id="3f81c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f81c-125">CommonParameters</span></span>
<span data-ttu-id="3f81c-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f81c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f81c-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f81c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f81c-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="3f81c-128">INPUTS</span></span>

### <span data-ttu-id="3f81c-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3f81c-129">None</span></span>

## <span data-ttu-id="3f81c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f81c-130">OUTPUTS</span></span>

### <span data-ttu-id="3f81c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="3f81c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="3f81c-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="3f81c-132">NOTES</span></span>

## <span data-ttu-id="3f81c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f81c-133">RELATED LINKS</span></span>
