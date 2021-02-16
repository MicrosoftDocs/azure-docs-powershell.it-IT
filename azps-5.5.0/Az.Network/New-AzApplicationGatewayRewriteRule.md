---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202878"
---
# <span data-ttu-id="5dce5-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5dce5-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="5dce5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dce5-102">SYNOPSIS</span></span>
<span data-ttu-id="5dce5-103">Crea una regola di riscrittura per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5dce5-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="5dce5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5dce5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dce5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5dce5-105">DESCRIPTION</span></span>
<span data-ttu-id="5dce5-106">Il cmdlet **New-AzApplicationGatewayRewriteRule** crea una regola di riscrittura per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5dce5-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="5dce5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5dce5-107">EXAMPLES</span></span>

### <span data-ttu-id="5dce5-108">Esempio 1: Creare una regola di riscrittura per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="5dce5-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="5dce5-109">Questo comando crea una regola di riscrittura denominata regola1 e archivia il risultato nella variabile $rule.</span><span class="sxs-lookup"><span data-stu-id="5dce5-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="5dce5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5dce5-110">PARAMETERS</span></span>

### <span data-ttu-id="5dce5-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="5dce5-111">-ActionSet</span></span>
<span data-ttu-id="5dce5-112">ActionSet della regola di riscrittura</span><span class="sxs-lookup"><span data-stu-id="5dce5-112">ActionSet of the rewrite rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dce5-113">-Condizione</span><span class="sxs-lookup"><span data-stu-id="5dce5-113">-Condition</span></span>
<span data-ttu-id="5dce5-114">Condizione per l'esecuzione della regola di riscrittura</span><span class="sxs-lookup"><span data-stu-id="5dce5-114">Condition for the rewrite rule to execute</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dce5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dce5-115">-DefaultProfile</span></span>
<span data-ttu-id="5dce5-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5dce5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dce5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5dce5-117">-Name</span></span>
<span data-ttu-id="5dce5-118">Nome dell'oggetto RewriteRule</span><span class="sxs-lookup"><span data-stu-id="5dce5-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="5dce5-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="5dce5-119">-RuleSequence</span></span>
<span data-ttu-id="5dce5-120">L'ordinamento delle regole di questa regola di riscrittura nel set di regole di riscrittura</span><span class="sxs-lookup"><span data-stu-id="5dce5-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dce5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dce5-121">CommonParameters</span></span>
<span data-ttu-id="5dce5-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dce5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dce5-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dce5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dce5-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="5dce5-124">INPUTS</span></span>

### <span data-ttu-id="5dce5-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5dce5-125">None</span></span>

## <span data-ttu-id="5dce5-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5dce5-126">OUTPUTS</span></span>

### <span data-ttu-id="5dce5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5dce5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="5dce5-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="5dce5-128">NOTES</span></span>

## <span data-ttu-id="5dce5-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5dce5-129">RELATED LINKS</span></span>

[<span data-ttu-id="5dce5-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5dce5-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5dce5-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5dce5-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5dce5-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5dce5-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5dce5-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5dce5-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5dce5-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5dce5-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5dce5-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5dce5-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="5dce5-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5dce5-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
