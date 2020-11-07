---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: ee7f6f2b824041cf56b27c34dc70358c4229e527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678382"
---
# <span data-ttu-id="b3b82-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="b3b82-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="b3b82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3b82-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b82-103">Crea una condizione di corrispondenza per la regola personalizzata</span><span class="sxs-lookup"><span data-stu-id="b3b82-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="b3b82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3b82-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3b82-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3b82-105">DESCRIPTION</span></span>
<span data-ttu-id="b3b82-106">La **nuova AzApplicationGatewayFirewallCondition** crea una condizione di corrispondenza per la regola personalizzata del firewall.</span><span class="sxs-lookup"><span data-stu-id="b3b82-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="b3b82-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3b82-107">EXAMPLES</span></span>

### <span data-ttu-id="b3b82-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3b82-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzureRmApplicationGatewayFirewallConditon -MatchVariables $variable -Operator Contains -NegationConditon false -Transforms Lowercase, Trim -MatchValues abc, cde
```

<span data-ttu-id="b3b82-109">Il comando crea una nuova condizione di corrispondenza usando la variabile di corrispondenza definita nel $variable, l'operatore è Contains e la condizione di negazione è false, trasfroms includendo minuscole e trim, il valore di match è ABC e CDE.</span><span class="sxs-lookup"><span data-stu-id="b3b82-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="b3b82-110">La nuova condizione di corrispondenza viene salvata in $condition.</span><span class="sxs-lookup"><span data-stu-id="b3b82-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="b3b82-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3b82-111">PARAMETERS</span></span>

### <span data-ttu-id="b3b82-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b82-112">-DefaultProfile</span></span>
<span data-ttu-id="b3b82-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b82-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3b82-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="b3b82-114">-MatchValue</span></span>
<span data-ttu-id="b3b82-115">Valore di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="b3b82-115">Match value.</span></span>

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

### <span data-ttu-id="b3b82-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="b3b82-116">-MatchVariable</span></span>
<span data-ttu-id="b3b82-117">Elenco di variabili di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="b3b82-117">List of match variables.</span></span>

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

### <span data-ttu-id="b3b82-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="b3b82-118">-NegationCondition</span></span>
<span data-ttu-id="b3b82-119">Descrive se la condizione è negata o meno.</span><span class="sxs-lookup"><span data-stu-id="b3b82-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="b3b82-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="b3b82-120">-Operator</span></span>
<span data-ttu-id="b3b82-121">Descrive l'operatore che deve essere abbinato.</span><span class="sxs-lookup"><span data-stu-id="b3b82-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="b3b82-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="b3b82-122">-Transform</span></span>
<span data-ttu-id="b3b82-123">Elenco di trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="b3b82-123">List of transforms.</span></span>

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

### <span data-ttu-id="b3b82-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b82-124">CommonParameters</span></span>
<span data-ttu-id="b3b82-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b82-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b82-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3b82-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b82-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3b82-127">INPUTS</span></span>

### <span data-ttu-id="b3b82-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b3b82-128">None</span></span>

## <span data-ttu-id="b3b82-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3b82-129">OUTPUTS</span></span>

### <span data-ttu-id="b3b82-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="b3b82-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="b3b82-131">Note</span><span class="sxs-lookup"><span data-stu-id="b3b82-131">NOTES</span></span>

## <span data-ttu-id="b3b82-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3b82-132">RELATED LINKS</span></span>