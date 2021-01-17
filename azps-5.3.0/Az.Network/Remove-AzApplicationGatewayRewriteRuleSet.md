---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486688"
---
# <span data-ttu-id="c9c91-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9c91-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="c9c91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9c91-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c91-103">Rimuove un set di regole di riscrittura da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9c91-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="c9c91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9c91-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9c91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9c91-105">DESCRIPTION</span></span>
<span data-ttu-id="c9c91-106">Il cmdlet **Remove-AzApplicationGatewayRewriteRuleSet** rimuove un set di regole di riscrittura da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c91-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="c9c91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9c91-107">EXAMPLES</span></span>

### <span data-ttu-id="c9c91-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9c91-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="c9c91-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c9c91-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c9c91-110">Il secondo comando rimuove il set di regole di riscrittura denominato RuleSet02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c9c91-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c9c91-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9c91-111">PARAMETERS</span></span>

### <span data-ttu-id="c9c91-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9c91-112">-ApplicationGateway</span></span>
<span data-ttu-id="c9c91-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9c91-113">The applicationGateway</span></span>

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

### <span data-ttu-id="c9c91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c91-114">-DefaultProfile</span></span>
<span data-ttu-id="c9c91-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c91-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9c91-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9c91-116">-Name</span></span>
<span data-ttu-id="c9c91-117">Nome del gateway dell'applicazione RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9c91-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c9c91-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c91-118">CommonParameters</span></span>
<span data-ttu-id="c9c91-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9c91-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c91-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9c91-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c91-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9c91-121">INPUTS</span></span>

### <span data-ttu-id="c9c91-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9c91-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c9c91-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9c91-123">OUTPUTS</span></span>

### <span data-ttu-id="c9c91-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9c91-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c9c91-125">Note</span><span class="sxs-lookup"><span data-stu-id="c9c91-125">NOTES</span></span>

## <span data-ttu-id="c9c91-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9c91-126">RELATED LINKS</span></span>

[<span data-ttu-id="c9c91-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9c91-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c9c91-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9c91-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c9c91-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9c91-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c9c91-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9c91-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c9c91-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c9c91-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="c9c91-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c9c91-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="c9c91-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9c91-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
