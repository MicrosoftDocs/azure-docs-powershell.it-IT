---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 9304471b12f33d677f493a3ee6803a1219d9f977
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193862"
---
# <span data-ttu-id="a1419-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1419-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="a1419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1419-102">SYNOPSIS</span></span>
<span data-ttu-id="a1419-103">Ottiene una configurazione della regola NAT in ingresso per un servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="a1419-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a1419-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1419-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1419-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a1419-105">DESCRIPTION</span></span>
<span data-ttu-id="a1419-106">Il cmdlet **Get-AzLoadBalancerInboundNatRuleConfig** ottiene una o più regole NAT (Network Address Translation) in ingresso in una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="a1419-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="a1419-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1419-107">EXAMPLES</span></span>

### <span data-ttu-id="a1419-108">Esempio 1: Ottenere una configurazione della regola NAT in ingresso</span><span class="sxs-lookup"><span data-stu-id="a1419-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="a1419-109">Il primo comando recupera la bilanciamento del carico denominata MyLoadBalancer e la archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="a1419-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="a1419-110">Il secondo comando recupera la regola NAT associata denominata MyInboundNatRule1 dal servizio di bilanciamento del carico in $slb.</span><span class="sxs-lookup"><span data-stu-id="a1419-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="a1419-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1419-111">PARAMETERS</span></span>

### <span data-ttu-id="a1419-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1419-112">-DefaultProfile</span></span>
<span data-ttu-id="a1419-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1419-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1419-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1419-114">-LoadBalancer</span></span>
<span data-ttu-id="a1419-115">Specifica la bilanciamento del carico associata alla configurazione della regola NAT in ingresso da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a1419-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="a1419-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a1419-116">-Name</span></span>
<span data-ttu-id="a1419-117">Specifica il nome della configurazione della regola NAT in ingresso da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a1419-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="a1419-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1419-118">CommonParameters</span></span>
<span data-ttu-id="a1419-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1419-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1419-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a1419-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1419-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="a1419-121">INPUTS</span></span>

### <span data-ttu-id="a1419-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1419-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a1419-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1419-123">OUTPUTS</span></span>

### <span data-ttu-id="a1419-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a1419-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="a1419-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="a1419-125">NOTES</span></span>

## <span data-ttu-id="a1419-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1419-126">RELATED LINKS</span></span>

[<span data-ttu-id="a1419-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1419-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a1419-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1419-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a1419-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1419-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a1419-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1419-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


