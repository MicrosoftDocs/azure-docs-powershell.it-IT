---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184286"
---
# <span data-ttu-id="b10ae-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b10ae-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="b10ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b10ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b10ae-103">Rimuove una configurazione del pool NAT in ingresso da una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b10ae-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="b10ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b10ae-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b10ae-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b10ae-105">DESCRIPTION</span></span>
<span data-ttu-id="b10ae-106">Il cmdlet **Remove-AzLoadBalancerInboundNatPoolConfig** rimuove una configurazione del pool NAT in ingresso da una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b10ae-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="b10ae-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b10ae-107">EXAMPLES</span></span>

### <span data-ttu-id="b10ae-108">1: Rimuovere</span><span class="sxs-lookup"><span data-stu-id="b10ae-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="b10ae-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b10ae-109">PARAMETERS</span></span>

### <span data-ttu-id="b10ae-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b10ae-110">-DefaultProfile</span></span>
<span data-ttu-id="b10ae-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b10ae-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b10ae-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b10ae-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="b10ae-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b10ae-113">-Name</span></span>
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

### <span data-ttu-id="b10ae-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b10ae-114">-Confirm</span></span>
<span data-ttu-id="b10ae-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b10ae-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b10ae-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b10ae-116">-WhatIf</span></span>
<span data-ttu-id="b10ae-117">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b10ae-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b10ae-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b10ae-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b10ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b10ae-119">CommonParameters</span></span>
<span data-ttu-id="b10ae-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b10ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b10ae-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b10ae-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b10ae-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="b10ae-122">INPUTS</span></span>

### <span data-ttu-id="b10ae-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b10ae-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b10ae-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b10ae-124">OUTPUTS</span></span>

### <span data-ttu-id="b10ae-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b10ae-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b10ae-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="b10ae-126">NOTES</span></span>

## <span data-ttu-id="b10ae-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b10ae-127">RELATED LINKS</span></span>

[<span data-ttu-id="b10ae-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b10ae-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b10ae-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b10ae-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b10ae-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b10ae-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b10ae-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b10ae-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
