---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 4b2b8f2694377845af92db5809230a423f83d594
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853930"
---
# <span data-ttu-id="356fc-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="356fc-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="356fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="356fc-102">SYNOPSIS</span></span>
<span data-ttu-id="356fc-103">Aggiunge un set di regole di riscrittura a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="356fc-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="356fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="356fc-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="356fc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="356fc-105">DESCRIPTION</span></span>
<span data-ttu-id="356fc-106">Il cmdlet **Add-AzApplicationGatewayRewriteRuleSet** aggiunge un set di regole di riscrittura a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="356fc-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="356fc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="356fc-107">EXAMPLES</span></span>

### <span data-ttu-id="356fc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="356fc-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="356fc-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="356fc-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="356fc-110">Il secondo comando aggiunge il set di regole di riscrittura al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="356fc-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="356fc-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="356fc-111">PARAMETERS</span></span>

### <span data-ttu-id="356fc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="356fc-112">-ApplicationGateway</span></span>
<span data-ttu-id="356fc-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="356fc-113">The applicationGateway</span></span>

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

### <span data-ttu-id="356fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356fc-114">-DefaultProfile</span></span>
<span data-ttu-id="356fc-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="356fc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="356fc-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="356fc-116">-Name</span></span>
<span data-ttu-id="356fc-117">Nome del RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="356fc-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="356fc-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="356fc-118">-RewriteRule</span></span>
<span data-ttu-id="356fc-119">Elenco delle regole di riscrittura</span><span class="sxs-lookup"><span data-stu-id="356fc-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="356fc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356fc-120">CommonParameters</span></span>
<span data-ttu-id="356fc-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="356fc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356fc-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="356fc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356fc-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="356fc-123">INPUTS</span></span>

### <span data-ttu-id="356fc-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="356fc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="356fc-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="356fc-125">OUTPUTS</span></span>

### <span data-ttu-id="356fc-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="356fc-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="356fc-127">Note</span><span class="sxs-lookup"><span data-stu-id="356fc-127">NOTES</span></span>

## <span data-ttu-id="356fc-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="356fc-128">RELATED LINKS</span></span>

[<span data-ttu-id="356fc-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="356fc-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="356fc-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="356fc-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="356fc-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="356fc-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="356fc-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="356fc-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="356fc-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="356fc-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="356fc-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="356fc-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="356fc-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="356fc-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
