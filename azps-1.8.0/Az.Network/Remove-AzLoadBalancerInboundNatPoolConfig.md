---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: a9a76af9eaee36913fd22c8003d6f4b9ba8c7b77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678119"
---
# <span data-ttu-id="baf0a-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="baf0a-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="baf0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="baf0a-102">SYNOPSIS</span></span>
<span data-ttu-id="baf0a-103">Rimuove una configurazione del pool NAT in ingresso da un programma di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="baf0a-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="baf0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="baf0a-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baf0a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="baf0a-105">DESCRIPTION</span></span>
<span data-ttu-id="baf0a-106">Il cmdlet **Remove-AzLoadBalancerInboundNatPoolConfig** rimuove una configurazione del pool NAT in ingresso da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="baf0a-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="baf0a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="baf0a-107">EXAMPLES</span></span>

### <span data-ttu-id="baf0a-108">1: rimuovere</span><span class="sxs-lookup"><span data-stu-id="baf0a-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="baf0a-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="baf0a-109">PARAMETERS</span></span>

### <span data-ttu-id="baf0a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf0a-110">-DefaultProfile</span></span>
<span data-ttu-id="baf0a-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="baf0a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baf0a-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="baf0a-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="baf0a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="baf0a-113">-Name</span></span>
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

### <span data-ttu-id="baf0a-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="baf0a-114">-Confirm</span></span>
<span data-ttu-id="baf0a-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baf0a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baf0a-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baf0a-116">-WhatIf</span></span>
<span data-ttu-id="baf0a-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="baf0a-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="baf0a-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="baf0a-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baf0a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf0a-119">CommonParameters</span></span>
<span data-ttu-id="baf0a-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baf0a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf0a-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baf0a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf0a-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="baf0a-122">INPUTS</span></span>

### <span data-ttu-id="baf0a-123">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="baf0a-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="baf0a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="baf0a-124">OUTPUTS</span></span>

### <span data-ttu-id="baf0a-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="baf0a-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="baf0a-126">Note</span><span class="sxs-lookup"><span data-stu-id="baf0a-126">NOTES</span></span>

## <span data-ttu-id="baf0a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="baf0a-127">RELATED LINKS</span></span>

[<span data-ttu-id="baf0a-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="baf0a-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="baf0a-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="baf0a-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="baf0a-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="baf0a-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="baf0a-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="baf0a-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
