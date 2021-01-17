---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475867"
---
# <span data-ttu-id="5876d-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5876d-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="5876d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5876d-102">SYNOPSIS</span></span>
<span data-ttu-id="5876d-103">Rimuove una configurazione del pool NAT in ingresso da un programma di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="5876d-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="5876d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5876d-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5876d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5876d-105">DESCRIPTION</span></span>
<span data-ttu-id="5876d-106">Il cmdlet **Remove-AzLoadBalancerInboundNatPoolConfig** rimuove una configurazione del pool NAT in ingresso da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="5876d-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="5876d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5876d-107">EXAMPLES</span></span>

### <span data-ttu-id="5876d-108">1: rimuovere</span><span class="sxs-lookup"><span data-stu-id="5876d-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="5876d-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5876d-109">PARAMETERS</span></span>

### <span data-ttu-id="5876d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5876d-110">-DefaultProfile</span></span>
<span data-ttu-id="5876d-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5876d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5876d-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5876d-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="5876d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5876d-113">-Name</span></span>
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

### <span data-ttu-id="5876d-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5876d-114">-Confirm</span></span>
<span data-ttu-id="5876d-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5876d-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5876d-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5876d-116">-WhatIf</span></span>
<span data-ttu-id="5876d-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5876d-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5876d-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5876d-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5876d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5876d-119">CommonParameters</span></span>
<span data-ttu-id="5876d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5876d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5876d-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5876d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5876d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5876d-122">INPUTS</span></span>

### <span data-ttu-id="5876d-123">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5876d-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5876d-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5876d-124">OUTPUTS</span></span>

### <span data-ttu-id="5876d-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5876d-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5876d-126">Note</span><span class="sxs-lookup"><span data-stu-id="5876d-126">NOTES</span></span>

## <span data-ttu-id="5876d-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5876d-127">RELATED LINKS</span></span>

[<span data-ttu-id="5876d-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5876d-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="5876d-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5876d-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="5876d-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5876d-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="5876d-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5876d-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
