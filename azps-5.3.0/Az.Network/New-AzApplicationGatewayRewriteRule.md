---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379371"
---
# <span data-ttu-id="b57c4-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b57c4-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="b57c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b57c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b57c4-103">Crea una regola di riscrittura per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b57c4-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="b57c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b57c4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b57c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b57c4-105">DESCRIPTION</span></span>
<span data-ttu-id="b57c4-106">**Il cmdlet New-AzApplicationGatewayRewriteRule** crea una regola di riscrittura per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="b57c4-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="b57c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b57c4-107">EXAMPLES</span></span>

### <span data-ttu-id="b57c4-108">Esempio 1: creare una regola di riscrittura per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="b57c4-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="b57c4-109">Questo comando crea una regola di riscrittura denominata Rule1 e archivia il risultato nella variabile denominata $rule.</span><span class="sxs-lookup"><span data-stu-id="b57c4-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="b57c4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b57c4-110">PARAMETERS</span></span>

### <span data-ttu-id="b57c4-111">-Actiont</span><span class="sxs-lookup"><span data-stu-id="b57c4-111">-ActionSet</span></span>
<span data-ttu-id="b57c4-112">Actiont della regola di riscrittura</span><span class="sxs-lookup"><span data-stu-id="b57c4-112">ActionSet of the rewrite rule</span></span>

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

### <span data-ttu-id="b57c4-113">-Condition</span><span class="sxs-lookup"><span data-stu-id="b57c4-113">-Condition</span></span>
<span data-ttu-id="b57c4-114">Condizione per l'esecuzione della regola di riscrittura</span><span class="sxs-lookup"><span data-stu-id="b57c4-114">Condition for the rewrite rule to execute</span></span>

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

### <span data-ttu-id="b57c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b57c4-115">-DefaultProfile</span></span>
<span data-ttu-id="b57c4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b57c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b57c4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b57c4-117">-Name</span></span>
<span data-ttu-id="b57c4-118">Nome del RewriteRule</span><span class="sxs-lookup"><span data-stu-id="b57c4-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="b57c4-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="b57c4-119">-RuleSequence</span></span>
<span data-ttu-id="b57c4-120">Ordinamento delle regole di questa regola di riscrittura nel set di regole di riscrittura</span><span class="sxs-lookup"><span data-stu-id="b57c4-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="b57c4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b57c4-121">CommonParameters</span></span>
<span data-ttu-id="b57c4-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b57c4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b57c4-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b57c4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b57c4-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b57c4-124">INPUTS</span></span>

### <span data-ttu-id="b57c4-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b57c4-125">None</span></span>

## <span data-ttu-id="b57c4-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b57c4-126">OUTPUTS</span></span>

### <span data-ttu-id="b57c4-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b57c4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="b57c4-128">Note</span><span class="sxs-lookup"><span data-stu-id="b57c4-128">NOTES</span></span>

## <span data-ttu-id="b57c4-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b57c4-129">RELATED LINKS</span></span>

[<span data-ttu-id="b57c4-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b57c4-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b57c4-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b57c4-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b57c4-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b57c4-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b57c4-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b57c4-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b57c4-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b57c4-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b57c4-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b57c4-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="b57c4-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b57c4-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
