---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: dc3019154d4041396d46f3c9f6dbdbdd3deb22a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193942"
---
# <span data-ttu-id="feb06-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="feb06-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="feb06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feb06-102">SYNOPSIS</span></span>
<span data-ttu-id="feb06-103">Recupera il set di regole di riscrittura di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="feb06-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="feb06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="feb06-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feb06-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="feb06-105">DESCRIPTION</span></span>
<span data-ttu-id="feb06-106">Recupera il set di regole di riscrittura di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="feb06-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="feb06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="feb06-107">EXAMPLES</span></span>

### <span data-ttu-id="feb06-108">Esempio 1: Ottenere un set di regole di riscrittura specifico</span><span class="sxs-lookup"><span data-stu-id="feb06-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="feb06-109">Il primo comando recupera il Gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="feb06-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="feb06-110">Il secondo comando recupera il set di regole di riscrittura denominato RuleSet01 dal Gateway di applicazione memorizzato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="feb06-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="feb06-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="feb06-111">PARAMETERS</span></span>

### <span data-ttu-id="feb06-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="feb06-112">-ApplicationGateway</span></span>
<span data-ttu-id="feb06-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="feb06-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="feb06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb06-114">-DefaultProfile</span></span>
<span data-ttu-id="feb06-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="feb06-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feb06-116">-Name</span><span class="sxs-lookup"><span data-stu-id="feb06-116">-Name</span></span>
<span data-ttu-id="feb06-117">Nome del gateway applicazione RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="feb06-117">The name of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feb06-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb06-118">CommonParameters</span></span>
<span data-ttu-id="feb06-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feb06-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb06-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="feb06-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb06-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="feb06-121">INPUTS</span></span>

### <span data-ttu-id="feb06-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="feb06-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="feb06-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="feb06-123">OUTPUTS</span></span>

### <span data-ttu-id="feb06-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="feb06-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="feb06-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="feb06-125">NOTES</span></span>

## <span data-ttu-id="feb06-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="feb06-126">RELATED LINKS</span></span>

[<span data-ttu-id="feb06-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="feb06-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="feb06-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="feb06-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="feb06-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="feb06-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="feb06-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="feb06-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="feb06-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="feb06-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="feb06-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="feb06-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="feb06-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="feb06-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
