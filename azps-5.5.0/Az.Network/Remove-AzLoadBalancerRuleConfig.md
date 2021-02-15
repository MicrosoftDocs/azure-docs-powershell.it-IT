---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ba865b5059e69ae9fb89936a45e432ddff7fb9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186950"
---
# <span data-ttu-id="30156-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30156-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="30156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30156-102">SYNOPSIS</span></span>
<span data-ttu-id="30156-103">Rimuove una configurazione di regola per una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="30156-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="30156-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30156-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30156-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="30156-105">DESCRIPTION</span></span>
<span data-ttu-id="30156-106">Il cmdlet **Remove-AzLoadBalancerRuleConfig rimuove** una configurazione di regola per una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="30156-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="30156-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30156-107">EXAMPLES</span></span>

### <span data-ttu-id="30156-108">Esempio 1: Rimuovere una configurazione di regole da un servizio di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="30156-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="30156-109">Il primo comando recupera la bilanciamento del carico denominata MyLoadBalancer e quindi la archivia nella $loadbalancer variabile.</span><span class="sxs-lookup"><span data-stu-id="30156-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="30156-110">Il secondo comando rimuove la configurazione della regola denominata MyLBruleName dal servizio di bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="30156-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="30156-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30156-111">PARAMETERS</span></span>

### <span data-ttu-id="30156-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30156-112">-DefaultProfile</span></span>
<span data-ttu-id="30156-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30156-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30156-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30156-114">-LoadBalancer</span></span>
<span data-ttu-id="30156-115">Specifica **l'oggetto LoadBalancer** che contiene la configurazione della regola rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30156-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="30156-116">-Name</span><span class="sxs-lookup"><span data-stu-id="30156-116">-Name</span></span>
<span data-ttu-id="30156-117">Specifica il nome della configurazione della regola di bilanciamento del carico rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30156-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="30156-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30156-118">-Confirm</span></span>
<span data-ttu-id="30156-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30156-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30156-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30156-120">-WhatIf</span></span>
<span data-ttu-id="30156-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30156-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30156-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30156-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30156-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30156-123">CommonParameters</span></span>
<span data-ttu-id="30156-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30156-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30156-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30156-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30156-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="30156-126">INPUTS</span></span>

### <span data-ttu-id="30156-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30156-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="30156-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30156-128">OUTPUTS</span></span>

### <span data-ttu-id="30156-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30156-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="30156-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="30156-130">NOTES</span></span>

## <span data-ttu-id="30156-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30156-131">RELATED LINKS</span></span>

[<span data-ttu-id="30156-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30156-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="30156-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30156-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="30156-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30156-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="30156-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30156-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="30156-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30156-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


