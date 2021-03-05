---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 5652615cf8072e4a448f2fe6c6d4b3fd784cc330
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996279"
---
# <span data-ttu-id="3dd7c-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dd7c-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="3dd7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd7c-103">Rimuove una configurazione della regola in uscita da una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3dd7c-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="3dd7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dd7c-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dd7c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3dd7c-105">DESCRIPTION</span></span>
<span data-ttu-id="3dd7c-106">Il cmdlet **Remove-AzLoadBalancerOutboundRuleConfig rimuove** una configurazione della regola in uscita da una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd7c-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="3dd7c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dd7c-107">EXAMPLES</span></span>

### <span data-ttu-id="3dd7c-108">Esempio 1: Eliminare una regola in uscita da una bilanciamento del carico di Azure</span><span class="sxs-lookup"><span data-stu-id="3dd7c-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="3dd7c-109">Il primo comando ottiene il bilanciamento del carico associato alla configurazione della regola in uscita che si vuole rimuovere e quindi lo archivia nella variabile $slb in uscita.</span><span class="sxs-lookup"><span data-stu-id="3dd7c-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="3dd7c-110">Il secondo comando rimuove la configurazione della regola in uscita associata dal servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3dd7c-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="3dd7c-111">Il terzo comando aggiorna il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3dd7c-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="3dd7c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dd7c-112">PARAMETERS</span></span>

### <span data-ttu-id="3dd7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd7c-113">-DefaultProfile</span></span>
<span data-ttu-id="3dd7c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd7c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dd7c-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3dd7c-115">-LoadBalancer</span></span>
<span data-ttu-id="3dd7c-116">Riferimento alla risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3dd7c-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="3dd7c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3dd7c-117">-Name</span></span>
<span data-ttu-id="3dd7c-118">Nome della regola in uscita</span><span class="sxs-lookup"><span data-stu-id="3dd7c-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="3dd7c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dd7c-119">-Confirm</span></span>
<span data-ttu-id="3dd7c-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dd7c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dd7c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dd7c-121">-WhatIf</span></span>
<span data-ttu-id="3dd7c-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dd7c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dd7c-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dd7c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dd7c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd7c-124">CommonParameters</span></span>
<span data-ttu-id="3dd7c-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dd7c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd7c-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dd7c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd7c-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="3dd7c-127">INPUTS</span></span>

### <span data-ttu-id="3dd7c-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3dd7c-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3dd7c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dd7c-129">OUTPUTS</span></span>

### <span data-ttu-id="3dd7c-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3dd7c-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3dd7c-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="3dd7c-131">NOTES</span></span>

## <span data-ttu-id="3dd7c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dd7c-132">RELATED LINKS</span></span>

[<span data-ttu-id="3dd7c-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dd7c-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="3dd7c-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dd7c-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="3dd7c-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dd7c-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="3dd7c-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dd7c-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
