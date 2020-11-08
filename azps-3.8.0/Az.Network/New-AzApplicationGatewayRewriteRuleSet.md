---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022732"
---
# <span data-ttu-id="35f7e-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35f7e-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="35f7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="35f7e-103">Crea una regola di routing delle richieste per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35f7e-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="35f7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35f7e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35f7e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="35f7e-106">**Il cmdlet New-AzApplicationGatewayRewriteRuleSet** crea un set di regole di riscrittura per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="35f7e-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="35f7e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35f7e-107">EXAMPLES</span></span>

### <span data-ttu-id="35f7e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35f7e-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="35f7e-109">Questo comando crea un set di regole di riscrittura denominato RuleSet1 e archivia il risultato nella variabile denominata $ruleset.</span><span class="sxs-lookup"><span data-stu-id="35f7e-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="35f7e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35f7e-110">PARAMETERS</span></span>

### <span data-ttu-id="35f7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f7e-111">-DefaultProfile</span></span>
<span data-ttu-id="35f7e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35f7e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35f7e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="35f7e-113">-Name</span></span>
<span data-ttu-id="35f7e-114">Nome del RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35f7e-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="35f7e-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="35f7e-115">-RewriteRule</span></span>
<span data-ttu-id="35f7e-116">Elenco delle regole di riscrittura</span><span class="sxs-lookup"><span data-stu-id="35f7e-116">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f7e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f7e-117">CommonParameters</span></span>
<span data-ttu-id="35f7e-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35f7e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f7e-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35f7e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f7e-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35f7e-120">INPUTS</span></span>

### <span data-ttu-id="35f7e-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="35f7e-121">None</span></span>

## <span data-ttu-id="35f7e-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35f7e-122">OUTPUTS</span></span>

### <span data-ttu-id="35f7e-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35f7e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="35f7e-124">Note</span><span class="sxs-lookup"><span data-stu-id="35f7e-124">NOTES</span></span>

## <span data-ttu-id="35f7e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35f7e-125">RELATED LINKS</span></span>

[<span data-ttu-id="35f7e-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35f7e-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="35f7e-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35f7e-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="35f7e-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35f7e-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="35f7e-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35f7e-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="35f7e-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="35f7e-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="35f7e-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="35f7e-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="35f7e-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="35f7e-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
