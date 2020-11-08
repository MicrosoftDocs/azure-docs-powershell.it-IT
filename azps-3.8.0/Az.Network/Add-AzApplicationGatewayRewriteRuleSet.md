---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021744"
---
# <span data-ttu-id="9a377-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a377-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="9a377-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a377-102">SYNOPSIS</span></span>
<span data-ttu-id="9a377-103">Aggiunge un set di regole di riscrittura a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a377-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="9a377-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a377-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a377-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a377-105">DESCRIPTION</span></span>
<span data-ttu-id="9a377-106">Il cmdlet **Add-AzApplicationGatewayRewriteRuleSet** aggiunge un set di regole di riscrittura a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a377-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="9a377-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a377-107">EXAMPLES</span></span>

### <span data-ttu-id="9a377-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a377-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="9a377-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9a377-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9a377-110">Il secondo comando aggiunge il set di regole di riscrittura al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a377-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="9a377-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a377-111">PARAMETERS</span></span>

### <span data-ttu-id="9a377-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9a377-112">-ApplicationGateway</span></span>
<span data-ttu-id="9a377-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9a377-113">The applicationGateway</span></span>

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

### <span data-ttu-id="9a377-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a377-114">-DefaultProfile</span></span>
<span data-ttu-id="9a377-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a377-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a377-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a377-116">-Name</span></span>
<span data-ttu-id="9a377-117">Nome del RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a377-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="9a377-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="9a377-118">-RewriteRule</span></span>
<span data-ttu-id="9a377-119">Elenco delle regole di riscrittura</span><span class="sxs-lookup"><span data-stu-id="9a377-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="9a377-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a377-120">CommonParameters</span></span>
<span data-ttu-id="9a377-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a377-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a377-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a377-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a377-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a377-123">INPUTS</span></span>

### <span data-ttu-id="9a377-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9a377-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9a377-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a377-125">OUTPUTS</span></span>

### <span data-ttu-id="9a377-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9a377-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9a377-127">Note</span><span class="sxs-lookup"><span data-stu-id="9a377-127">NOTES</span></span>

## <span data-ttu-id="9a377-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a377-128">RELATED LINKS</span></span>

[<span data-ttu-id="9a377-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a377-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9a377-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a377-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9a377-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a377-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9a377-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a377-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9a377-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9a377-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="9a377-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9a377-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="9a377-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a377-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
