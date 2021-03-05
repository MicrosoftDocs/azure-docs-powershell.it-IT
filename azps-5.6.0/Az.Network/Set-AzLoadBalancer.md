---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: b608a8fe62f7316116409d4174ea01603b928ae2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963934"
---
# <span data-ttu-id="9a876-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a876-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="9a876-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a876-102">SYNOPSIS</span></span>
<span data-ttu-id="9a876-103">Aggiorna una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="9a876-103">Updates a load balancer.</span></span>

## <span data-ttu-id="9a876-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a876-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a876-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9a876-105">DESCRIPTION</span></span>
<span data-ttu-id="9a876-106">Il cmdlet **Set-AzLoadBalancer** aggiorna una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="9a876-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="9a876-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a876-107">EXAMPLES</span></span>

### <span data-ttu-id="9a876-108">Esempio 1: Modificare una bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="9a876-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="9a876-109">Il primo comando ottiene la soluzione di bilanciamento del carico denominata NRPLB e quindi la archivia nella $slb variabile.</span><span class="sxs-lookup"><span data-stu-id="9a876-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="9a876-110">Il secondo comando usa l'operatore della pipeline per passare la bilanciamento del carico in $slb ad Add-AzLoadBalancerInboundNatRuleConfig, che aggiunge una regola NAT in ingresso denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="9a876-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="9a876-111">Il terzo comando passa la bilanciamento del carico **a Set-AzLoadBalancer,** che aggiorna la configurazione di bilanciamento del carico e la salva.</span><span class="sxs-lookup"><span data-stu-id="9a876-111">The third command passes the load balancer to **Set-AzLoadBalancer**, which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="9a876-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a876-112">PARAMETERS</span></span>

### <span data-ttu-id="9a876-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a876-113">-AsJob</span></span>
<span data-ttu-id="9a876-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9a876-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a876-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a876-115">-DefaultProfile</span></span>
<span data-ttu-id="9a876-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a876-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a876-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a876-117">-LoadBalancer</span></span>
<span data-ttu-id="9a876-118">Specifica un oggetto di bilanciamento del carico che rappresenta lo stato su cui deve essere impostata la bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="9a876-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="9a876-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a876-119">-Confirm</span></span>
<span data-ttu-id="9a876-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a876-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a876-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a876-121">-WhatIf</span></span>
<span data-ttu-id="9a876-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a876-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a876-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a876-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a876-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a876-124">CommonParameters</span></span>
<span data-ttu-id="9a876-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a876-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a876-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a876-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a876-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="9a876-127">INPUTS</span></span>

### <span data-ttu-id="9a876-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a876-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9a876-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a876-129">OUTPUTS</span></span>

### <span data-ttu-id="9a876-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a876-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9a876-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="9a876-131">NOTES</span></span>

## <span data-ttu-id="9a876-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a876-132">RELATED LINKS</span></span>

[<span data-ttu-id="9a876-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a876-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="9a876-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a876-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="9a876-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a876-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


