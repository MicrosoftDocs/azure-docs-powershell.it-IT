---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199681"
---
# <span data-ttu-id="10653-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10653-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="10653-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10653-102">SYNOPSIS</span></span>
<span data-ttu-id="10653-103">Ottiene la configurazione della regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="10653-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="10653-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10653-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10653-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10653-105">DESCRIPTION</span></span>
<span data-ttu-id="10653-106">Il cmdlet **Get-AzLoadBalancerRuleConfig** ottiene una o più configurazioni di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="10653-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="10653-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10653-107">EXAMPLES</span></span>

### <span data-ttu-id="10653-108">Esempio 1: ottenere la configurazione della regola di un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="10653-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="10653-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="10653-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="10653-110">Il secondo comando ottiene la configurazione di regola associata denominata MyLBrulename dal bilanciamento del carico in $slb.</span><span class="sxs-lookup"><span data-stu-id="10653-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="10653-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10653-111">PARAMETERS</span></span>

### <span data-ttu-id="10653-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10653-112">-DefaultProfile</span></span>
<span data-ttu-id="10653-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10653-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10653-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="10653-114">-LoadBalancer</span></span>
<span data-ttu-id="10653-115">Specifica il bilanciamento del carico associato alla configurazione della regola da ottenere.</span><span class="sxs-lookup"><span data-stu-id="10653-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="10653-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="10653-116">-Name</span></span>
<span data-ttu-id="10653-117">Specifica il nome della configurazione della regola da ottenere.</span><span class="sxs-lookup"><span data-stu-id="10653-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="10653-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10653-118">CommonParameters</span></span>
<span data-ttu-id="10653-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10653-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10653-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10653-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10653-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10653-121">INPUTS</span></span>

### <span data-ttu-id="10653-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="10653-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="10653-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10653-123">OUTPUTS</span></span>

### <span data-ttu-id="10653-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="10653-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="10653-125">Note</span><span class="sxs-lookup"><span data-stu-id="10653-125">NOTES</span></span>

## <span data-ttu-id="10653-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10653-126">RELATED LINKS</span></span>

[<span data-ttu-id="10653-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10653-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="10653-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="10653-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="10653-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10653-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="10653-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10653-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


