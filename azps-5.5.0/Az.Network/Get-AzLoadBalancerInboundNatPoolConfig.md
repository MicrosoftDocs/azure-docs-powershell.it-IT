---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203079"
---
# <span data-ttu-id="150b0-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="150b0-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="150b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="150b0-102">SYNOPSIS</span></span>
<span data-ttu-id="150b0-103">Ottiene una o più configurazioni di pool NAT in ingresso da una soluzione di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="150b0-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="150b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="150b0-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="150b0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="150b0-105">DESCRIPTION</span></span>
<span data-ttu-id="150b0-106">Il cmdlet **Get-AzLoadBalancerInboundNatPoolConfig** ottiene una o più configurazioni di pool NAT in ingresso da una soluzione di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="150b0-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="150b0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="150b0-107">EXAMPLES</span></span>

### <span data-ttu-id="150b0-108">1: Ottieni</span><span class="sxs-lookup"><span data-stu-id="150b0-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="150b0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="150b0-109">PARAMETERS</span></span>

### <span data-ttu-id="150b0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150b0-110">-DefaultProfile</span></span>
<span data-ttu-id="150b0-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="150b0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="150b0-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="150b0-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="150b0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="150b0-113">-Name</span></span>
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

### <span data-ttu-id="150b0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150b0-114">CommonParameters</span></span>
<span data-ttu-id="150b0-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="150b0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150b0-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="150b0-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150b0-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="150b0-117">INPUTS</span></span>

### <span data-ttu-id="150b0-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="150b0-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="150b0-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="150b0-119">OUTPUTS</span></span>

### <span data-ttu-id="150b0-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="150b0-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="150b0-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="150b0-121">NOTES</span></span>

## <span data-ttu-id="150b0-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="150b0-122">RELATED LINKS</span></span>

[<span data-ttu-id="150b0-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="150b0-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="150b0-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="150b0-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="150b0-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="150b0-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="150b0-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="150b0-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
