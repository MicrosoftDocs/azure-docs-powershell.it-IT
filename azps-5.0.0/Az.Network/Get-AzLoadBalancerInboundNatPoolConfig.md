---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199688"
---
# <span data-ttu-id="646a4-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="646a4-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="646a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="646a4-102">SYNOPSIS</span></span>
<span data-ttu-id="646a4-103">Ottiene una o più configurazioni di pool NAT in ingresso da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="646a4-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="646a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="646a4-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="646a4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="646a4-105">DESCRIPTION</span></span>
<span data-ttu-id="646a4-106">Il cmdlet **Get-AzLoadBalancerInboundNatPoolConfig** ottiene una o più configurazioni di pool NAT in ingresso da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="646a4-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="646a4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="646a4-107">EXAMPLES</span></span>

### <span data-ttu-id="646a4-108">1: ottenere</span><span class="sxs-lookup"><span data-stu-id="646a4-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="646a4-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="646a4-109">PARAMETERS</span></span>

### <span data-ttu-id="646a4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="646a4-110">-DefaultProfile</span></span>
<span data-ttu-id="646a4-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="646a4-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="646a4-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="646a4-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="646a4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="646a4-113">-Name</span></span>
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

### <span data-ttu-id="646a4-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646a4-114">CommonParameters</span></span>
<span data-ttu-id="646a4-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="646a4-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646a4-116">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="646a4-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646a4-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="646a4-117">INPUTS</span></span>

### <span data-ttu-id="646a4-118">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="646a4-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="646a4-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="646a4-119">OUTPUTS</span></span>

### <span data-ttu-id="646a4-120">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="646a4-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="646a4-121">Note</span><span class="sxs-lookup"><span data-stu-id="646a4-121">NOTES</span></span>

## <span data-ttu-id="646a4-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="646a4-122">RELATED LINKS</span></span>

[<span data-ttu-id="646a4-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="646a4-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="646a4-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="646a4-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="646a4-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="646a4-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="646a4-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="646a4-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
