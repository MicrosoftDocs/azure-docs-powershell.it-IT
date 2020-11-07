---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 35338b5fa179e916bfb52f2529a12d5be1665e89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853302"
---
# <span data-ttu-id="d3ce6-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3ce6-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="d3ce6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ce6-103">Ottiene il set di regole di riscrittura di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d3ce6-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="d3ce6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3ce6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3ce6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3ce6-105">DESCRIPTION</span></span>
<span data-ttu-id="d3ce6-106">Ottiene il set di regole di riscrittura di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d3ce6-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="d3ce6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3ce6-107">EXAMPLES</span></span>

### <span data-ttu-id="d3ce6-108">Esempio 1: ottenere un set di regole di riscrittura specifico</span><span class="sxs-lookup"><span data-stu-id="d3ce6-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="d3ce6-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="d3ce6-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="d3ce6-110">Il secondo comando ottiene il set di regole di riscrittura denominato RuleSet01 dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="d3ce6-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="d3ce6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3ce6-111">PARAMETERS</span></span>

### <span data-ttu-id="d3ce6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3ce6-112">-ApplicationGateway</span></span>
<span data-ttu-id="d3ce6-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3ce6-113">The applicationGateway</span></span>

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

### <span data-ttu-id="d3ce6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ce6-114">-DefaultProfile</span></span>
<span data-ttu-id="d3ce6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3ce6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3ce6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3ce6-116">-Name</span></span>
<span data-ttu-id="d3ce6-117">Nome del gateway dell'applicazione RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3ce6-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="d3ce6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ce6-118">CommonParameters</span></span>
<span data-ttu-id="d3ce6-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3ce6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ce6-120">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3ce6-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ce6-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3ce6-121">INPUTS</span></span>

### <span data-ttu-id="d3ce6-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3ce6-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d3ce6-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3ce6-123">OUTPUTS</span></span>

### <span data-ttu-id="d3ce6-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3ce6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="d3ce6-125">Note</span><span class="sxs-lookup"><span data-stu-id="d3ce6-125">NOTES</span></span>

## <span data-ttu-id="d3ce6-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3ce6-126">RELATED LINKS</span></span>

[<span data-ttu-id="d3ce6-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3ce6-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3ce6-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3ce6-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3ce6-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3ce6-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3ce6-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3ce6-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3ce6-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d3ce6-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d3ce6-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d3ce6-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="d3ce6-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3ce6-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
