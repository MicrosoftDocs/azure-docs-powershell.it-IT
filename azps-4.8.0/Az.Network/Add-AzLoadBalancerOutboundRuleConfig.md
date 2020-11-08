---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ca7c581a2cc3710403dae9aff0c0afda450dbbae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189561"
---
# <span data-ttu-id="c742c-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c742c-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="c742c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c742c-102">SYNOPSIS</span></span>
<span data-ttu-id="c742c-103">Aggiunge una configurazione della regola in uscita a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c742c-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="c742c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c742c-104">SYNTAX</span></span>

### <span data-ttu-id="c742c-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c742c-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c742c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c742c-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c742c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c742c-107">DESCRIPTION</span></span>
<span data-ttu-id="c742c-108">Il cmdlet **Add-AzLoadBalancerOutboundRuleConfig** aggiunge una configurazione della regola in uscita a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="c742c-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="c742c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c742c-109">EXAMPLES</span></span>

### <span data-ttu-id="c742c-110">Esempio 1: aggiungere una configurazione di regola in uscita a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="c742c-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="c742c-111">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="c742c-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="c742c-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a **Add-AzLoadBalancerOutboundRuleConfig** , che aggiunge una configurazione della regola in uscita al bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c742c-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="c742c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c742c-113">PARAMETERS</span></span>

### <span data-ttu-id="c742c-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="c742c-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="c742c-115">Numero di porte in uscita da usare per NAT.</span><span class="sxs-lookup"><span data-stu-id="c742c-115">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c742c-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c742c-116">-BackendAddressPool</span></span>
<span data-ttu-id="c742c-117">Riferimento a un pool di DIP.</span><span class="sxs-lookup"><span data-stu-id="c742c-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c742c-118">Il traffico in uscita viene bilanciato in modo casuale tra IPs nell'IPs backend.</span><span class="sxs-lookup"><span data-stu-id="c742c-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c742c-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c742c-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="c742c-120">Riferimento a un pool di DIP.</span><span class="sxs-lookup"><span data-stu-id="c742c-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c742c-121">Il traffico in uscita viene bilanciato in modo casuale tra IPs nell'IPs backend.</span><span class="sxs-lookup"><span data-stu-id="c742c-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c742c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c742c-122">-DefaultProfile</span></span>
<span data-ttu-id="c742c-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c742c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c742c-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c742c-124">-EnableTcpReset</span></span>
<span data-ttu-id="c742c-125">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="c742c-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="c742c-126">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="c742c-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c742c-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c742c-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c742c-128">Gli indirizzi IP del frontend del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c742c-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c742c-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c742c-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c742c-130">Timeout per la connessione inattiva TCP</span><span class="sxs-lookup"><span data-stu-id="c742c-130">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c742c-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c742c-131">-LoadBalancer</span></span>
<span data-ttu-id="c742c-132">Riferimento della risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c742c-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="c742c-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="c742c-133">-Name</span></span>
<span data-ttu-id="c742c-134">Nome della regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="c742c-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="c742c-135">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="c742c-135">-Protocol</span></span>
<span data-ttu-id="c742c-136">Protocol-TCP, UDP o all</span><span class="sxs-lookup"><span data-stu-id="c742c-136">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c742c-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c742c-137">-Confirm</span></span>
<span data-ttu-id="c742c-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c742c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c742c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c742c-139">-WhatIf</span></span>
<span data-ttu-id="c742c-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c742c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c742c-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c742c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c742c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c742c-142">CommonParameters</span></span>
<span data-ttu-id="c742c-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c742c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c742c-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c742c-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c742c-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c742c-145">INPUTS</span></span>

### <span data-ttu-id="c742c-146">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c742c-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c742c-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c742c-147">System.Int32</span></span>

### <span data-ttu-id="c742c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c742c-148">System.String</span></span>

### <span data-ttu-id="c742c-149">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="c742c-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="c742c-150">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c742c-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c742c-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c742c-151">OUTPUTS</span></span>

### <span data-ttu-id="c742c-152">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c742c-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c742c-153">Note</span><span class="sxs-lookup"><span data-stu-id="c742c-153">NOTES</span></span>

## <span data-ttu-id="c742c-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c742c-154">RELATED LINKS</span></span>

[<span data-ttu-id="c742c-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c742c-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c742c-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c742c-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c742c-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c742c-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c742c-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c742c-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)