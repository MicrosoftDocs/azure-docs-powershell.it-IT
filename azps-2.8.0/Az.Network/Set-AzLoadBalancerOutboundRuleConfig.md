---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 482f729f0ee3fa3efc6a78a1bc2b5fbbd3fe1d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854106"
---
# <span data-ttu-id="62df7-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="62df7-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="62df7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62df7-102">SYNOPSIS</span></span>
<span data-ttu-id="62df7-103">Imposta una configurazione della regola in uscita per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="62df7-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="62df7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62df7-104">SYNTAX</span></span>

### <span data-ttu-id="62df7-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62df7-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62df7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="62df7-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62df7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62df7-107">DESCRIPTION</span></span>
<span data-ttu-id="62df7-108">Il cmdlet **set-AzLoadBalancerOutboundRuleConfig** imposta una configurazione della regola in uscita per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="62df7-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="62df7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62df7-109">EXAMPLES</span></span>

### <span data-ttu-id="62df7-110">Esempio 1: modificare la configurazione della regola in uscita in un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="62df7-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="62df7-111">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="62df7-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="62df7-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerOutboundRuleConfig, che aggiunge una configurazione di regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="62df7-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="62df7-113">Il terzo comando passa il bilanciamento del carico a **set-AzLoadBalancerOutboundRuleConfig** , che salva e aggiorna la configurazione della regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="62df7-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="62df7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62df7-114">PARAMETERS</span></span>

### <span data-ttu-id="62df7-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="62df7-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="62df7-116">Numero di porte in uscita da usare per NAT.</span><span class="sxs-lookup"><span data-stu-id="62df7-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="62df7-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="62df7-117">-BackendAddressPool</span></span>
<span data-ttu-id="62df7-118">Riferimento a un pool di DIP.</span><span class="sxs-lookup"><span data-stu-id="62df7-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="62df7-119">Il traffico in uscita viene bilanciato in modo casuale tra IPs nell'IPs backend.</span><span class="sxs-lookup"><span data-stu-id="62df7-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="62df7-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="62df7-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="62df7-121">Riferimento a un pool di DIP.</span><span class="sxs-lookup"><span data-stu-id="62df7-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="62df7-122">Il traffico in uscita viene bilanciato in modo casuale tra IPs nell'IPs backend.</span><span class="sxs-lookup"><span data-stu-id="62df7-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="62df7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62df7-123">-DefaultProfile</span></span>
<span data-ttu-id="62df7-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62df7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62df7-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="62df7-125">-EnableTcpReset</span></span>
<span data-ttu-id="62df7-126">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="62df7-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="62df7-127">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="62df7-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="62df7-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="62df7-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="62df7-129">Gli indirizzi IP del frontend del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="62df7-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="62df7-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="62df7-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="62df7-131">Timeout per la connessione inattiva TCP</span><span class="sxs-lookup"><span data-stu-id="62df7-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="62df7-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="62df7-132">-LoadBalancer</span></span>
<span data-ttu-id="62df7-133">Riferimento della risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="62df7-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="62df7-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="62df7-134">-Name</span></span>
<span data-ttu-id="62df7-135">Nome della regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="62df7-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="62df7-136">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="62df7-136">-Protocol</span></span>
<span data-ttu-id="62df7-137">Protocol-TCP, UDP o all</span><span class="sxs-lookup"><span data-stu-id="62df7-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="62df7-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62df7-138">-Confirm</span></span>
<span data-ttu-id="62df7-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62df7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62df7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62df7-140">-WhatIf</span></span>
<span data-ttu-id="62df7-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62df7-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62df7-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62df7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62df7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62df7-143">CommonParameters</span></span>
<span data-ttu-id="62df7-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62df7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62df7-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62df7-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62df7-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62df7-146">INPUTS</span></span>

### <span data-ttu-id="62df7-147">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="62df7-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="62df7-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="62df7-148">System.Int32</span></span>

### <span data-ttu-id="62df7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="62df7-149">System.String</span></span>

### <span data-ttu-id="62df7-150">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="62df7-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="62df7-151">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="62df7-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="62df7-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62df7-152">OUTPUTS</span></span>

### <span data-ttu-id="62df7-153">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="62df7-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="62df7-154">Note</span><span class="sxs-lookup"><span data-stu-id="62df7-154">NOTES</span></span>

## <span data-ttu-id="62df7-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62df7-155">RELATED LINKS</span></span>

[<span data-ttu-id="62df7-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="62df7-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="62df7-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="62df7-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="62df7-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="62df7-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="62df7-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="62df7-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
