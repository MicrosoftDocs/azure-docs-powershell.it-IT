---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 049b99ee0d019ae7f845e5e7578d9982e41a7a4b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865189"
---
# <span data-ttu-id="27b1f-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27b1f-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="27b1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="27b1f-103">Aggiorna un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="27b1f-103">Updates a load balancer.</span></span>

## <span data-ttu-id="27b1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27b1f-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27b1f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27b1f-105">DESCRIPTION</span></span>
<span data-ttu-id="27b1f-106">Il cmdlet **set-AzLoadBalancer** aggiorna un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="27b1f-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="27b1f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27b1f-107">EXAMPLES</span></span>

### <span data-ttu-id="27b1f-108">Esempio 1: modificare un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="27b1f-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="27b1f-109">Il primo comando ottiene il bilanciamento del carico denominato NRPLB e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="27b1f-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="27b1f-110">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerInboundNatRuleConfig, che aggiunge una regola di NAT in ingresso denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="27b1f-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="27b1f-111">Il terzo comando passa il bilanciamento del carico a **set-AzLoadBalancer** , che aggiorna la configurazione del bilanciamento del carico e la Salva.</span><span class="sxs-lookup"><span data-stu-id="27b1f-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="27b1f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27b1f-112">PARAMETERS</span></span>

### <span data-ttu-id="27b1f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27b1f-113">-AsJob</span></span>
<span data-ttu-id="27b1f-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="27b1f-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b1f-115">-DefaultProfile</span></span>
<span data-ttu-id="27b1f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27b1f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27b1f-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27b1f-117">-LoadBalancer</span></span>
<span data-ttu-id="27b1f-118">Specifica un oggetto di bilanciamento del carico che rappresenta lo stato in cui deve essere impostato il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="27b1f-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27b1f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27b1f-119">-Confirm</span></span>
<span data-ttu-id="27b1f-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27b1f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27b1f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b1f-121">-WhatIf</span></span>
<span data-ttu-id="27b1f-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27b1f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27b1f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27b1f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27b1f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b1f-124">CommonParameters</span></span>
<span data-ttu-id="27b1f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27b1f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b1f-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27b1f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b1f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27b1f-127">INPUTS</span></span>

### <span data-ttu-id="27b1f-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27b1f-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="27b1f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27b1f-129">OUTPUTS</span></span>

### <span data-ttu-id="27b1f-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27b1f-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="27b1f-131">Note</span><span class="sxs-lookup"><span data-stu-id="27b1f-131">NOTES</span></span>

## <span data-ttu-id="27b1f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27b1f-132">RELATED LINKS</span></span>

[<span data-ttu-id="27b1f-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27b1f-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="27b1f-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27b1f-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="27b1f-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27b1f-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


