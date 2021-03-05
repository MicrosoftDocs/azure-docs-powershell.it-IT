---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 099abbe1f8c2a536cebff59f1c21b664bb284e8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990021"
---
# <span data-ttu-id="eb16d-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb16d-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="eb16d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb16d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb16d-103">Rimuove un set di regole di riscrittura da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="eb16d-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="eb16d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb16d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb16d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eb16d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb16d-106">Il cmdlet **Remove-AzApplicationGatewayRewriteRuleSet** rimuove un set di regole di riscrittura da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="eb16d-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="eb16d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb16d-107">EXAMPLES</span></span>

### <span data-ttu-id="eb16d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eb16d-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="eb16d-109">Il primo comando ottiene un gateway applicazione e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="eb16d-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="eb16d-110">Il secondo comando rimuove il set di regole di riscrittura denominato RuleSet02 dal gateway di applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="eb16d-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="eb16d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb16d-111">PARAMETERS</span></span>

### <span data-ttu-id="eb16d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb16d-112">-ApplicationGateway</span></span>
<span data-ttu-id="eb16d-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb16d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="eb16d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb16d-114">-DefaultProfile</span></span>
<span data-ttu-id="eb16d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb16d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb16d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="eb16d-116">-Name</span></span>
<span data-ttu-id="eb16d-117">Nome del gateway applicazione RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb16d-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="eb16d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb16d-118">CommonParameters</span></span>
<span data-ttu-id="eb16d-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb16d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb16d-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb16d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb16d-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="eb16d-121">INPUTS</span></span>

### <span data-ttu-id="eb16d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb16d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eb16d-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb16d-123">OUTPUTS</span></span>

### <span data-ttu-id="eb16d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb16d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eb16d-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="eb16d-125">NOTES</span></span>

## <span data-ttu-id="eb16d-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb16d-126">RELATED LINKS</span></span>

[<span data-ttu-id="eb16d-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb16d-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb16d-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb16d-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb16d-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb16d-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb16d-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb16d-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb16d-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="eb16d-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="eb16d-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="eb16d-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="eb16d-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb16d-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
