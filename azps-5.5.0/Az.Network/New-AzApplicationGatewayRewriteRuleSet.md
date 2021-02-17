---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206811"
---
# <span data-ttu-id="c9d78-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9d78-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="c9d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9d78-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d78-103">Crea una regola di routing delle richieste per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c9d78-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="c9d78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9d78-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9d78-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c9d78-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d78-106">Il cmdlet **New-AzApplicationGatewayRewriteRuleSet crea** un set di regole di riscrittura per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d78-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="c9d78-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9d78-107">EXAMPLES</span></span>

### <span data-ttu-id="c9d78-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9d78-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="c9d78-109">Questo comando crea un set di regole di riscrittura denominato ruleset1 e archivia il risultato nella variabile $ruleset.</span><span class="sxs-lookup"><span data-stu-id="c9d78-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="c9d78-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9d78-110">PARAMETERS</span></span>

### <span data-ttu-id="c9d78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d78-111">-DefaultProfile</span></span>
<span data-ttu-id="c9d78-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d78-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9d78-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c9d78-113">-Name</span></span>
<span data-ttu-id="c9d78-114">Nome di RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9d78-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="c9d78-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="c9d78-115">-RewriteRule</span></span>
<span data-ttu-id="c9d78-116">Elenco delle regole di riscrittura</span><span class="sxs-lookup"><span data-stu-id="c9d78-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="c9d78-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d78-117">CommonParameters</span></span>
<span data-ttu-id="c9d78-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d78-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d78-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d78-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d78-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="c9d78-120">INPUTS</span></span>

### <span data-ttu-id="c9d78-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c9d78-121">None</span></span>

## <span data-ttu-id="c9d78-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9d78-122">OUTPUTS</span></span>

### <span data-ttu-id="c9d78-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9d78-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="c9d78-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="c9d78-124">NOTES</span></span>

## <span data-ttu-id="c9d78-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9d78-125">RELATED LINKS</span></span>

[<span data-ttu-id="c9d78-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9d78-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c9d78-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9d78-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c9d78-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9d78-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c9d78-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9d78-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c9d78-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c9d78-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="c9d78-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c9d78-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="c9d78-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9d78-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
