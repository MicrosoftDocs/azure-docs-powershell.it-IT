---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 378d9521e309629bdb9e6ee58cfc1cd06fd9ef7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510888"
---
# <span data-ttu-id="5cbe3-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5cbe3-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="5cbe3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5cbe3-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbe3-103">Ottiene una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="5cbe3-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cbe3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cbe3-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cbe3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cbe3-105">DESCRIPTION</span></span>
<span data-ttu-id="5cbe3-106">Il cmdlet **Get-AzureRmLoadBalancerInboundNatRuleConfig** ottiene una o più regole NAT (Network Address Translation) in ingresso in un sistema di bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbe3-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="5cbe3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cbe3-107">EXAMPLES</span></span>

### <span data-ttu-id="5cbe3-108">Esempio 1: ottenere una configurazione della regola NAT in ingresso</span><span class="sxs-lookup"><span data-stu-id="5cbe3-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="5cbe3-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="5cbe3-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="5cbe3-110">Il secondo comando ottiene la regola NAT associata denominata MyInboundNatRule1 dal bilanciamento del carico in $slb.</span><span class="sxs-lookup"><span data-stu-id="5cbe3-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="5cbe3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5cbe3-111">PARAMETERS</span></span>

### <span data-ttu-id="5cbe3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbe3-112">-DefaultProfile</span></span>
<span data-ttu-id="5cbe3-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbe3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbe3-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5cbe3-114">-LoadBalancer</span></span>
<span data-ttu-id="5cbe3-115">Specifica il bilanciamento del carico associato alla configurazione della regola NAT in ingresso da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5cbe3-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="5cbe3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cbe3-116">-Name</span></span>
<span data-ttu-id="5cbe3-117">Specifica il nome della configurazione della regola NAT in ingresso da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5cbe3-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="5cbe3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbe3-118">CommonParameters</span></span>
<span data-ttu-id="5cbe3-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbe3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbe3-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cbe3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbe3-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5cbe3-121">INPUTS</span></span>

### <span data-ttu-id="5cbe3-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5cbe3-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="5cbe3-123">Parametri: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5cbe3-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="5cbe3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cbe3-124">OUTPUTS</span></span>

### <span data-ttu-id="5cbe3-125">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="5cbe3-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="5cbe3-126">Note</span><span class="sxs-lookup"><span data-stu-id="5cbe3-126">NOTES</span></span>

## <span data-ttu-id="5cbe3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cbe3-127">RELATED LINKS</span></span>

[<span data-ttu-id="5cbe3-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5cbe3-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="5cbe3-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5cbe3-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="5cbe3-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5cbe3-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="5cbe3-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5cbe3-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


