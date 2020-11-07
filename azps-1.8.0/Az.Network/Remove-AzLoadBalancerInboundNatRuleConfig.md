---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 2d47a3481772d846a65e3b0bc0d1eb1c62fa5cd5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678117"
---
# <span data-ttu-id="9db2c-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9db2c-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="9db2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9db2c-102">SYNOPSIS</span></span>
<span data-ttu-id="9db2c-103">Rimuove una configurazione della regola NAT in ingresso da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="9db2c-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="9db2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9db2c-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9db2c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9db2c-105">DESCRIPTION</span></span>
<span data-ttu-id="9db2c-106">Il cmdlet **Remove-AzLoadBalancerInboundNatRuleConfig** rimuove una configurazione della regola NAT (Network Address Translation) in ingresso da un sistema di bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="9db2c-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="9db2c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9db2c-107">EXAMPLES</span></span>

### <span data-ttu-id="9db2c-108">1: eliminare una regola di NAT in ingresso da un bilanciamento del carico di Azure</span><span class="sxs-lookup"><span data-stu-id="9db2c-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="9db2c-109">Il primo comando carica un bilanciamento del carico già esistente denominato "mylb" e lo archivia nella variabile $load balancer.</span><span class="sxs-lookup"><span data-stu-id="9db2c-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="9db2c-110">Il secondo comando rimuove la regola NAT in ingresso associata a questo bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="9db2c-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="9db2c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9db2c-111">PARAMETERS</span></span>

### <span data-ttu-id="9db2c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db2c-112">-DefaultProfile</span></span>
<span data-ttu-id="9db2c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9db2c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9db2c-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9db2c-114">-LoadBalancer</span></span>
<span data-ttu-id="9db2c-115">Specifica l'oggetto **LoadBalancer** che contiene la configurazione della regola NAT in ingresso rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9db2c-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9db2c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9db2c-116">-Name</span></span>
<span data-ttu-id="9db2c-117">Specifica il nome della configurazione della regola NAT in ingresso rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9db2c-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9db2c-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9db2c-118">-Confirm</span></span>
<span data-ttu-id="9db2c-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9db2c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9db2c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9db2c-120">-WhatIf</span></span>
<span data-ttu-id="9db2c-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9db2c-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9db2c-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9db2c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9db2c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db2c-123">CommonParameters</span></span>
<span data-ttu-id="9db2c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9db2c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db2c-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9db2c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db2c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9db2c-126">INPUTS</span></span>

### <span data-ttu-id="9db2c-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9db2c-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9db2c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9db2c-128">OUTPUTS</span></span>

### <span data-ttu-id="9db2c-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9db2c-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9db2c-130">Note</span><span class="sxs-lookup"><span data-stu-id="9db2c-130">NOTES</span></span>

## <span data-ttu-id="9db2c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9db2c-131">RELATED LINKS</span></span>

[<span data-ttu-id="9db2c-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9db2c-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9db2c-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9db2c-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9db2c-134">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9db2c-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9db2c-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9db2c-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)

