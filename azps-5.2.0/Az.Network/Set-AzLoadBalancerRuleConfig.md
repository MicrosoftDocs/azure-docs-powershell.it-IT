---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d86af5e56b44526cdc717d91927193cfcb3fd444
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354055"
---
# <span data-ttu-id="51dc7-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51dc7-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="51dc7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="51dc7-103">Aggiorna una configurazione di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="51dc7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51dc7-104">SYNTAX</span></span>

### <span data-ttu-id="51dc7-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51dc7-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51dc7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="51dc7-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51dc7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51dc7-107">DESCRIPTION</span></span>
<span data-ttu-id="51dc7-108">Il cmdlet **set-AzLoadBalancerRuleConfig** aggiorna una configurazione di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="51dc7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51dc7-109">EXAMPLES</span></span>

### <span data-ttu-id="51dc7-110">Esempio 1: modificare una configurazione della regola di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="51dc7-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="51dc7-111">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="51dc7-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="51dc7-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerRuleConfig, che aggiunge una regola denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="51dc7-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="51dc7-113">Il terzo comando passa il bilanciamento del carico a **set-AzLoadBalancerRuleConfig**, che imposta la nuova configurazione della regola.</span><span class="sxs-lookup"><span data-stu-id="51dc7-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig**, which sets the new rule configuration.</span></span>
<span data-ttu-id="51dc7-114">Tieni presente che la configurazione non Abilita un indirizzo IP mobile, che era stato abilitato dal comando precedente.</span><span class="sxs-lookup"><span data-stu-id="51dc7-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="51dc7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51dc7-115">PARAMETERS</span></span>

### <span data-ttu-id="51dc7-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="51dc7-116">-BackendAddressPool</span></span>
<span data-ttu-id="51dc7-117">Specifica un oggetto **BackendAddressPool** da associare a una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51dc7-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="51dc7-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="51dc7-119">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51dc7-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="51dc7-120">-BackendPort</span></span>
<span data-ttu-id="51dc7-121">Specifica la porta di backend per il traffico che corrisponde alla configurazione della regola.</span><span class="sxs-lookup"><span data-stu-id="51dc7-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="51dc7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51dc7-122">-DefaultProfile</span></span>
<span data-ttu-id="51dc7-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51dc7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51dc7-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="51dc7-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="51dc7-125">Configura SNAT per le VM nel pool back-end per usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="51dc7-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="51dc7-126">-EnableFloatingIP</span></span>
<span data-ttu-id="51dc7-127">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="51dc7-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="51dc7-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="51dc7-128">-EnableTcpReset</span></span>
<span data-ttu-id="51dc7-129">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="51dc7-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="51dc7-130">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="51dc7-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="51dc7-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="51dc7-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="51dc7-132">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51dc7-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="51dc7-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="51dc7-134">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="51dc7-134">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51dc7-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="51dc7-135">-FrontendPort</span></span>
<span data-ttu-id="51dc7-136">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="51dc7-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="51dc7-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="51dc7-138">Specifica il periodo di tempo, in minuti, per il quale lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="51dc7-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51dc7-139">-LoadBalancer</span></span>
<span data-ttu-id="51dc7-140">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-140">Specifies a load balancer.</span></span>
<span data-ttu-id="51dc7-141">Questo cmdlet aggiorna una configurazione di regola per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="51dc7-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="51dc7-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="51dc7-142">-LoadDistribution</span></span>
<span data-ttu-id="51dc7-143">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-143">Specifies a load distribution.</span></span>
<span data-ttu-id="51dc7-144">I valori accettabili per questo parametro sono: SourceIP e SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="51dc7-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51dc7-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="51dc7-145">-Name</span></span>
<span data-ttu-id="51dc7-146">Specifica il nome di un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="51dc7-147">-Probe</span><span class="sxs-lookup"><span data-stu-id="51dc7-147">-Probe</span></span>
<span data-ttu-id="51dc7-148">Specifica una sonda da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51dc7-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="51dc7-149">-ProbeId</span></span>
<span data-ttu-id="51dc7-150">Specifica l'ID del Probe da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51dc7-151">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="51dc7-151">-Protocol</span></span>
<span data-ttu-id="51dc7-152">Specifica il protocollo corrispondente a una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="51dc7-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="51dc7-153">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="51dc7-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51dc7-154">-Confermare</span><span class="sxs-lookup"><span data-stu-id="51dc7-154">-Confirm</span></span>
<span data-ttu-id="51dc7-155">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51dc7-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51dc7-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51dc7-156">-WhatIf</span></span>
<span data-ttu-id="51dc7-157">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51dc7-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51dc7-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51dc7-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51dc7-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51dc7-159">CommonParameters</span></span>
<span data-ttu-id="51dc7-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51dc7-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51dc7-161">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51dc7-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51dc7-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51dc7-162">INPUTS</span></span>

### <span data-ttu-id="51dc7-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51dc7-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="51dc7-164">System. String</span><span class="sxs-lookup"><span data-stu-id="51dc7-164">System.String</span></span>

### <span data-ttu-id="51dc7-165">System. Int32</span><span class="sxs-lookup"><span data-stu-id="51dc7-165">System.Int32</span></span>

### <span data-ttu-id="51dc7-166">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="51dc7-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="51dc7-167">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="51dc7-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="51dc7-168">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="51dc7-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="51dc7-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51dc7-169">OUTPUTS</span></span>

### <span data-ttu-id="51dc7-170">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51dc7-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="51dc7-171">Note</span><span class="sxs-lookup"><span data-stu-id="51dc7-171">NOTES</span></span>

## <span data-ttu-id="51dc7-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51dc7-172">RELATED LINKS</span></span>

[<span data-ttu-id="51dc7-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51dc7-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="51dc7-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51dc7-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="51dc7-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51dc7-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="51dc7-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51dc7-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="51dc7-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51dc7-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


