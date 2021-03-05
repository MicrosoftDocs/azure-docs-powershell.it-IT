---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: fc3b34e2fb9f91684aee2427d4271e6fab08843f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006446"
---
# <span data-ttu-id="f0fee-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f0fee-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="f0fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0fee-102">SYNOPSIS</span></span>
<span data-ttu-id="f0fee-103">Ottiene una configurazione della regola in uscita in una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f0fee-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="f0fee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0fee-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0fee-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0fee-105">DESCRIPTION</span></span>
<span data-ttu-id="f0fee-106">Il cmdlet **Get-AzLoadBalancerOutboundRuleConfig** ottiene una configurazione della regola in uscita o un elenco di configurazioni di regole in uscita in una soluzione di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f0fee-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="f0fee-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0fee-107">EXAMPLES</span></span>

### <span data-ttu-id="f0fee-108">Esempio 1: Ottenere una configurazione della regola in uscita in un servizio di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="f0fee-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="f0fee-109">Il primo comando ottiene la bilanciamento del carico denominata MyLoadBalancer e quindi la archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="f0fee-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="f0fee-110">Il secondo comando ottiene la configurazione della regola in uscita denominata MyRule associata a quella bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f0fee-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="f0fee-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0fee-111">PARAMETERS</span></span>

### <span data-ttu-id="f0fee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0fee-112">-DefaultProfile</span></span>
<span data-ttu-id="f0fee-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0fee-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0fee-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f0fee-114">-LoadBalancer</span></span>
<span data-ttu-id="f0fee-115">Riferimento alla risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f0fee-115">The reference of the load balancer resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0fee-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f0fee-116">-Name</span></span>
<span data-ttu-id="f0fee-117">Nome della regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="f0fee-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="f0fee-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0fee-118">CommonParameters</span></span>
<span data-ttu-id="f0fee-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0fee-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0fee-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f0fee-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0fee-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0fee-121">INPUTS</span></span>

### <span data-ttu-id="f0fee-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f0fee-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f0fee-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0fee-123">OUTPUTS</span></span>

### <span data-ttu-id="f0fee-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="f0fee-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="f0fee-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0fee-125">NOTES</span></span>

## <span data-ttu-id="f0fee-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0fee-126">RELATED LINKS</span></span>

[<span data-ttu-id="f0fee-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f0fee-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="f0fee-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f0fee-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="f0fee-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f0fee-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="f0fee-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f0fee-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
