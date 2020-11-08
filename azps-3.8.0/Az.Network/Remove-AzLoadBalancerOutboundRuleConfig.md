---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 824675d331d37c93e6bcf3bb3d5da0fa8cbde78b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021987"
---
# <span data-ttu-id="95582-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95582-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="95582-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95582-102">SYNOPSIS</span></span>
<span data-ttu-id="95582-103">Rimuove una configurazione della regola in uscita da un programma di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="95582-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="95582-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95582-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95582-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95582-105">DESCRIPTION</span></span>
<span data-ttu-id="95582-106">Il cmdlet **Remove-AzLoadBalancerOutboundRuleConfig** rimuove una configurazione della regola in uscita da un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="95582-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="95582-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95582-107">EXAMPLES</span></span>

### <span data-ttu-id="95582-108">Esempio 1: eliminare una regola in uscita da un bilanciamento del carico di Azure</span><span class="sxs-lookup"><span data-stu-id="95582-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="95582-109">Il primo comando ottiene il bilanciamento del carico associato alla configurazione della regola in uscita che si vuole rimuovere e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="95582-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="95582-110">Il secondo comando rimuove la configurazione della regola in uscita associata dal bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="95582-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="95582-111">Il terzo comando Aggiorna il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="95582-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="95582-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95582-112">PARAMETERS</span></span>

### <span data-ttu-id="95582-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95582-113">-DefaultProfile</span></span>
<span data-ttu-id="95582-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95582-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95582-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95582-115">-LoadBalancer</span></span>
<span data-ttu-id="95582-116">Riferimento della risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="95582-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="95582-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="95582-117">-Name</span></span>
<span data-ttu-id="95582-118">Nome della regola in uscita</span><span class="sxs-lookup"><span data-stu-id="95582-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95582-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="95582-119">-Confirm</span></span>
<span data-ttu-id="95582-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95582-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95582-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95582-121">-WhatIf</span></span>
<span data-ttu-id="95582-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95582-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95582-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95582-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95582-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95582-124">CommonParameters</span></span>
<span data-ttu-id="95582-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95582-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95582-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95582-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95582-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95582-127">INPUTS</span></span>

### <span data-ttu-id="95582-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95582-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="95582-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95582-129">OUTPUTS</span></span>

### <span data-ttu-id="95582-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95582-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="95582-131">Note</span><span class="sxs-lookup"><span data-stu-id="95582-131">NOTES</span></span>

## <span data-ttu-id="95582-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95582-132">RELATED LINKS</span></span>

[<span data-ttu-id="95582-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95582-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="95582-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95582-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="95582-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95582-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="95582-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95582-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
