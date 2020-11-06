---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d76803df11ff3f89e20ca7d849577ca51331416c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517452"
---
# <span data-ttu-id="9d878-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d878-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="9d878-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d878-102">SYNOPSIS</span></span>
<span data-ttu-id="9d878-103">Rimuove una configurazione della regola NAT in ingresso da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="9d878-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d878-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d878-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d878-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d878-105">DESCRIPTION</span></span>
<span data-ttu-id="9d878-106">Il cmdlet **Remove-AzureRmLoadBalancerInboundNatRuleConfig** rimuove una configurazione della regola NAT (Network Address Translation) in ingresso da un sistema di bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="9d878-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="9d878-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d878-107">EXAMPLES</span></span>

### <span data-ttu-id="9d878-108">1: eliminare una regola di NAT in ingresso da un bilanciamento del carico di Azure</span><span class="sxs-lookup"><span data-stu-id="9d878-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="9d878-109">Il primo comando carica un bilanciamento del carico già esistente denominato "mylb" e lo archivia nella variabile $load balancer.</span><span class="sxs-lookup"><span data-stu-id="9d878-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="9d878-110">Il secondo comando rimuove la regola NAT in ingresso associata a questo bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="9d878-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="9d878-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d878-111">PARAMETERS</span></span>

### <span data-ttu-id="9d878-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d878-112">-DefaultProfile</span></span>
<span data-ttu-id="9d878-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d878-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d878-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9d878-114">-LoadBalancer</span></span>
<span data-ttu-id="9d878-115">Specifica l'oggetto **LoadBalancer** che contiene la configurazione della regola NAT in ingresso rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d878-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9d878-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d878-116">-Name</span></span>
<span data-ttu-id="9d878-117">Specifica il nome della configurazione della regola NAT in ingresso rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d878-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9d878-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d878-118">-Confirm</span></span>
<span data-ttu-id="9d878-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d878-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d878-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d878-120">-WhatIf</span></span>
<span data-ttu-id="9d878-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d878-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d878-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d878-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d878-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d878-123">CommonParameters</span></span>
<span data-ttu-id="9d878-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d878-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d878-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d878-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d878-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d878-126">INPUTS</span></span>

### <span data-ttu-id="9d878-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9d878-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="9d878-128">Parametri: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9d878-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="9d878-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d878-129">OUTPUTS</span></span>

### <span data-ttu-id="9d878-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9d878-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9d878-131">Note</span><span class="sxs-lookup"><span data-stu-id="9d878-131">NOTES</span></span>

## <span data-ttu-id="9d878-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d878-132">RELATED LINKS</span></span>

[<span data-ttu-id="9d878-133">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d878-133">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9d878-134">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d878-134">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9d878-135">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d878-135">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9d878-136">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d878-136">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


