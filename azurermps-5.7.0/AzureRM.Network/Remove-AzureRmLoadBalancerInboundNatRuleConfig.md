---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6dcd7c51a43387139de85a3a9f0c17c0b19cfe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516687"
---
# <span data-ttu-id="f2d14-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2d14-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="f2d14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2d14-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d14-103">Rimuove una configurazione della regola NAT in ingresso da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f2d14-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2d14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2d14-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2d14-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2d14-105">DESCRIPTION</span></span>
<span data-ttu-id="f2d14-106">Il cmdlet **Remove-AzureRmLoadBalancerInboundNatRuleConfig** rimuove una configurazione della regola NAT (Network Address Translation) in ingresso da un sistema di bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d14-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="f2d14-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2d14-107">EXAMPLES</span></span>

### <span data-ttu-id="f2d14-108">1: eliminare una regola di NAT in ingresso da un bilanciamento del carico di Azure</span><span class="sxs-lookup"><span data-stu-id="f2d14-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="f2d14-109">Il primo comando carica un bilanciamento del carico già esistente denominato "mylb" e lo archivia nella variabile $load balancer.</span><span class="sxs-lookup"><span data-stu-id="f2d14-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="f2d14-110">Il secondo comando rimuove la regola NAT in ingresso associata a questo bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f2d14-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="f2d14-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2d14-111">PARAMETERS</span></span>

### <span data-ttu-id="f2d14-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d14-112">-DefaultProfile</span></span>
<span data-ttu-id="f2d14-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d14-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2d14-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2d14-114">-LoadBalancer</span></span>
<span data-ttu-id="f2d14-115">Specifica l'oggetto **LoadBalancer** che contiene la configurazione della regola NAT in ingresso rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2d14-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f2d14-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2d14-116">-Name</span></span>
<span data-ttu-id="f2d14-117">Specifica il nome della configurazione della regola NAT in ingresso rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2d14-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f2d14-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d14-118">CommonParameters</span></span>
<span data-ttu-id="f2d14-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2d14-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d14-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2d14-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d14-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2d14-121">INPUTS</span></span>

### <span data-ttu-id="f2d14-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2d14-122">PSLoadBalancer</span></span>
<span data-ttu-id="f2d14-123">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f2d14-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f2d14-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2d14-124">OUTPUTS</span></span>

### <span data-ttu-id="f2d14-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2d14-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f2d14-126">Note</span><span class="sxs-lookup"><span data-stu-id="f2d14-126">NOTES</span></span>

## <span data-ttu-id="f2d14-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2d14-127">RELATED LINKS</span></span>

[<span data-ttu-id="f2d14-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2d14-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f2d14-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2d14-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f2d14-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2d14-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f2d14-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2d14-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


