---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199538"
---
# <span data-ttu-id="f0e98-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f0e98-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="f0e98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0e98-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e98-103">Rimuove una configurazione del pool NAT in ingresso da un programma di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f0e98-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="f0e98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0e98-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0e98-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0e98-105">DESCRIPTION</span></span>
<span data-ttu-id="f0e98-106">Il cmdlet **Remove-AzLoadBalancerInboundNatPoolConfig** rimuove una configurazione del pool NAT in ingresso da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f0e98-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="f0e98-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0e98-107">EXAMPLES</span></span>

### <span data-ttu-id="f0e98-108">1: rimuovere</span><span class="sxs-lookup"><span data-stu-id="f0e98-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="f0e98-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0e98-109">PARAMETERS</span></span>

### <span data-ttu-id="f0e98-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e98-110">-DefaultProfile</span></span>
<span data-ttu-id="f0e98-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0e98-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0e98-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f0e98-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="f0e98-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0e98-113">-Name</span></span>
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

### <span data-ttu-id="f0e98-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0e98-114">-Confirm</span></span>
<span data-ttu-id="f0e98-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0e98-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0e98-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0e98-116">-WhatIf</span></span>
<span data-ttu-id="f0e98-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0e98-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0e98-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0e98-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0e98-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e98-119">CommonParameters</span></span>
<span data-ttu-id="f0e98-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0e98-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e98-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0e98-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e98-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0e98-122">INPUTS</span></span>

### <span data-ttu-id="f0e98-123">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f0e98-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f0e98-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0e98-124">OUTPUTS</span></span>

### <span data-ttu-id="f0e98-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f0e98-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f0e98-126">Note</span><span class="sxs-lookup"><span data-stu-id="f0e98-126">NOTES</span></span>

## <span data-ttu-id="f0e98-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0e98-127">RELATED LINKS</span></span>

[<span data-ttu-id="f0e98-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f0e98-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="f0e98-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f0e98-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="f0e98-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f0e98-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="f0e98-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f0e98-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)