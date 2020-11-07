---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6b866dc04975c2cde17509182e21936a2d6c9363
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860770"
---
# <span data-ttu-id="1d076-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d076-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="1d076-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d076-102">SYNOPSIS</span></span>
<span data-ttu-id="1d076-103">Ottiene una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1d076-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="1d076-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d076-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d076-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d076-105">DESCRIPTION</span></span>
<span data-ttu-id="1d076-106">Il cmdlet **Get-AzLoadBalancerInboundNatRuleConfig** ottiene una o più regole NAT (Network Address Translation) in ingresso in un sistema di bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d076-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="1d076-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d076-107">EXAMPLES</span></span>

### <span data-ttu-id="1d076-108">Esempio 1: ottenere una configurazione della regola NAT in ingresso</span><span class="sxs-lookup"><span data-stu-id="1d076-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="1d076-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="1d076-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="1d076-110">Il secondo comando ottiene la regola NAT associata denominata MyInboundNatRule1 dal bilanciamento del carico in $slb.</span><span class="sxs-lookup"><span data-stu-id="1d076-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="1d076-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d076-111">PARAMETERS</span></span>

### <span data-ttu-id="1d076-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d076-112">-DefaultProfile</span></span>
<span data-ttu-id="1d076-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d076-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d076-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1d076-114">-LoadBalancer</span></span>
<span data-ttu-id="1d076-115">Specifica il bilanciamento del carico associato alla configurazione della regola NAT in ingresso da ottenere.</span><span class="sxs-lookup"><span data-stu-id="1d076-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d076-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d076-116">-Name</span></span>
<span data-ttu-id="1d076-117">Specifica il nome della configurazione della regola NAT in ingresso da ottenere.</span><span class="sxs-lookup"><span data-stu-id="1d076-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d076-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d076-118">CommonParameters</span></span>
<span data-ttu-id="1d076-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d076-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d076-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d076-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d076-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d076-121">INPUTS</span></span>

### <span data-ttu-id="1d076-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1d076-122">PSLoadBalancer</span></span>
<span data-ttu-id="1d076-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1d076-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="1d076-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d076-124">OUTPUTS</span></span>

### <span data-ttu-id="1d076-125">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="1d076-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="1d076-126">Note</span><span class="sxs-lookup"><span data-stu-id="1d076-126">NOTES</span></span>

## <span data-ttu-id="1d076-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d076-127">RELATED LINKS</span></span>

[<span data-ttu-id="1d076-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1d076-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1d076-129">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d076-129">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1d076-130">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d076-130">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1d076-131">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d076-131">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


