---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 45d7fdf6a276e98ce0aca2c2a0db6989e062e42c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032306"
---
# <span data-ttu-id="b3114-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3114-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b3114-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3114-102">SYNOPSIS</span></span>
<span data-ttu-id="b3114-103">Modifica un set di regole di riscrittura per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b3114-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="b3114-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3114-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3114-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3114-105">DESCRIPTION</span></span>
<span data-ttu-id="b3114-106">Il cmdlet **set-AzApplicationGatewayRewriteRuleSet** modifica una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="b3114-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="b3114-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3114-107">EXAMPLES</span></span>

### <span data-ttu-id="b3114-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3114-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="b3114-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b3114-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b3114-110">Il secondo comando modifica il set di regole di riscrittura per il gateway dell'applicazione per usare le regole di riscrittura specificate nella variabile $rule.</span><span class="sxs-lookup"><span data-stu-id="b3114-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="b3114-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3114-111">PARAMETERS</span></span>

### <span data-ttu-id="b3114-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b3114-112">-ApplicationGateway</span></span>
<span data-ttu-id="b3114-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b3114-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b3114-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3114-114">-DefaultProfile</span></span>
<span data-ttu-id="b3114-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3114-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3114-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3114-116">-Name</span></span>
<span data-ttu-id="b3114-117">Nome del RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3114-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="b3114-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="b3114-118">-RewriteRule</span></span>
<span data-ttu-id="b3114-119">Elenco delle regole di riscrittura</span><span class="sxs-lookup"><span data-stu-id="b3114-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="b3114-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3114-120">CommonParameters</span></span>
<span data-ttu-id="b3114-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3114-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3114-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3114-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3114-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3114-123">INPUTS</span></span>

### <span data-ttu-id="b3114-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b3114-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b3114-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3114-125">OUTPUTS</span></span>

### <span data-ttu-id="b3114-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b3114-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b3114-127">Note</span><span class="sxs-lookup"><span data-stu-id="b3114-127">NOTES</span></span>

## <span data-ttu-id="b3114-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3114-128">RELATED LINKS</span></span>

[<span data-ttu-id="b3114-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3114-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b3114-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3114-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b3114-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3114-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b3114-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3114-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b3114-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b3114-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b3114-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b3114-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="b3114-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3114-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
