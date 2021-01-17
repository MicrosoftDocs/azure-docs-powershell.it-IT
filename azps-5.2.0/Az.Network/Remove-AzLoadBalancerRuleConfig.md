---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ba865b5059e69ae9fb89936a45e432ddff7fb9a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351064"
---
# <span data-ttu-id="0bee1-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bee1-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="0bee1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bee1-102">SYNOPSIS</span></span>
<span data-ttu-id="0bee1-103">Rimuove una configurazione di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="0bee1-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="0bee1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bee1-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bee1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bee1-105">DESCRIPTION</span></span>
<span data-ttu-id="0bee1-106">Il cmdlet **Remove-AzLoadBalancerRuleConfig** rimuove una configurazione di regola per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="0bee1-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="0bee1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bee1-107">EXAMPLES</span></span>

### <span data-ttu-id="0bee1-108">Esempio 1: rimuovere una configurazione di una regola da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="0bee1-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="0bee1-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="0bee1-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="0bee1-110">Il secondo comando rimuove la configurazione della regola denominata MyLBruleName dal bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="0bee1-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="0bee1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bee1-111">PARAMETERS</span></span>

### <span data-ttu-id="0bee1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bee1-112">-DefaultProfile</span></span>
<span data-ttu-id="0bee1-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0bee1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bee1-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0bee1-114">-LoadBalancer</span></span>
<span data-ttu-id="0bee1-115">Specifica l'oggetto **LoadBalancer** che contiene la configurazione della regola rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bee1-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0bee1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bee1-116">-Name</span></span>
<span data-ttu-id="0bee1-117">Specifica il nome della configurazione della regola di bilanciamento del carico rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bee1-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0bee1-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0bee1-118">-Confirm</span></span>
<span data-ttu-id="0bee1-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bee1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bee1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bee1-120">-WhatIf</span></span>
<span data-ttu-id="0bee1-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0bee1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bee1-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0bee1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bee1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bee1-123">CommonParameters</span></span>
<span data-ttu-id="0bee1-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bee1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bee1-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bee1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bee1-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bee1-126">INPUTS</span></span>

### <span data-ttu-id="0bee1-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0bee1-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0bee1-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bee1-128">OUTPUTS</span></span>

### <span data-ttu-id="0bee1-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0bee1-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0bee1-130">Note</span><span class="sxs-lookup"><span data-stu-id="0bee1-130">NOTES</span></span>

## <span data-ttu-id="0bee1-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bee1-131">RELATED LINKS</span></span>

[<span data-ttu-id="0bee1-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bee1-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0bee1-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0bee1-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0bee1-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bee1-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0bee1-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bee1-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0bee1-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bee1-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


