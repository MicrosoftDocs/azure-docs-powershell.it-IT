---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 096fb182ae330750eeb23e365bc929edb17b21f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007742"
---
# <span data-ttu-id="6ec9c-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="6ec9c-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="6ec9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ec9c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec9c-103">Crea una condizione di corrispondenza per una regola personalizzata</span><span class="sxs-lookup"><span data-stu-id="6ec9c-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="6ec9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ec9c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ec9c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6ec9c-105">DESCRIPTION</span></span>
<span data-ttu-id="6ec9c-106">**New-AzApplicationGatewayFirewallCondition crea** una condizione di corrispondenza per la regola personalizzata del firewall.</span><span class="sxs-lookup"><span data-stu-id="6ec9c-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="6ec9c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ec9c-107">EXAMPLES</span></span>

### <span data-ttu-id="6ec9c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ec9c-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="6ec9c-109">Il comando crea una nuova condizione di corrispondenza usando la variabile di corrispondenza definita nel $variable, l'operatore è Contains e la condizione di negazione è false, Transfroms including lowercase and trim, the match value is abc and cde.</span><span class="sxs-lookup"><span data-stu-id="6ec9c-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="6ec9c-110">La nuova condizione di corrispondenza viene salvata in $condition.</span><span class="sxs-lookup"><span data-stu-id="6ec9c-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="6ec9c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ec9c-111">PARAMETERS</span></span>

### <span data-ttu-id="6ec9c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec9c-112">-DefaultProfile</span></span>
<span data-ttu-id="6ec9c-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec9c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ec9c-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="6ec9c-114">-MatchValue</span></span>
<span data-ttu-id="6ec9c-115">Valore corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6ec9c-115">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec9c-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="6ec9c-116">-MatchVariable</span></span>
<span data-ttu-id="6ec9c-117">Elenco di variabili corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="6ec9c-117">List of match variables.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec9c-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="6ec9c-118">-NegationCondition</span></span>
<span data-ttu-id="6ec9c-119">Descrive se questa condizione è negata o meno.</span><span class="sxs-lookup"><span data-stu-id="6ec9c-119">Describes if this is negate condition or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec9c-120">-Operatore</span><span class="sxs-lookup"><span data-stu-id="6ec9c-120">-Operator</span></span>
<span data-ttu-id="6ec9c-121">Descrive l'operatore di cui trovare una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="6ec9c-121">Describes operator to be matched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith, Regex

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec9c-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="6ec9c-122">-Transform</span></span>
<span data-ttu-id="6ec9c-123">Elenco delle trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="6ec9c-123">List of transforms.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Trim, UrlDecode, UrlEncode, RemoveNulls, HtmlEntityDecode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec9c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec9c-124">CommonParameters</span></span>
<span data-ttu-id="6ec9c-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ec9c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec9c-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ec9c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec9c-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="6ec9c-127">INPUTS</span></span>

### <span data-ttu-id="6ec9c-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6ec9c-128">None</span></span>

## <span data-ttu-id="6ec9c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ec9c-129">OUTPUTS</span></span>

### <span data-ttu-id="6ec9c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="6ec9c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="6ec9c-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="6ec9c-131">NOTES</span></span>

## <span data-ttu-id="6ec9c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ec9c-132">RELATED LINKS</span></span>
