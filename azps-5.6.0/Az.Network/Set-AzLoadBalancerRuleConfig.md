---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 28f71cfe18b344c1e0fbccb632e87a19cf6e8075
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003406"
---
# <span data-ttu-id="995d7-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="995d7-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="995d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="995d7-102">SYNOPSIS</span></span>
<span data-ttu-id="995d7-103">Aggiorna una configurazione di regola per una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="995d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="995d7-104">SYNTAX</span></span>

### <span data-ttu-id="995d7-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="995d7-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="995d7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="995d7-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="995d7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="995d7-107">DESCRIPTION</span></span>
<span data-ttu-id="995d7-108">Il cmdlet **Set-AzLoadBalancerRuleConfig** aggiorna una configurazione di regola per un servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="995d7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="995d7-109">EXAMPLES</span></span>

### <span data-ttu-id="995d7-110">Esempio 1: Modificare la configurazione di una regola di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="995d7-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="995d7-111">Il primo comando recupera la bilanciamento del carico denominata MyLoadBalancer e quindi la archivia nella $slb variabile.</span><span class="sxs-lookup"><span data-stu-id="995d7-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="995d7-112">Il secondo comando usa l'operatore della pipeline per passare la bilanciamento del carico in $slb ad Add-AzLoadBalancerRuleConfig, che aggiunge una regola denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="995d7-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="995d7-113">Il terzo comando passa la bilanciamento del carico **a Set-AzLoadBalancerRuleConfig,** che imposta la configurazione della nuova regola.</span><span class="sxs-lookup"><span data-stu-id="995d7-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig**, which sets the new rule configuration.</span></span>
<span data-ttu-id="995d7-114">Si noti che la configurazione non abilita un indirizzo IP mobile, che era stato abilitato dal comando precedente.</span><span class="sxs-lookup"><span data-stu-id="995d7-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="995d7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="995d7-115">PARAMETERS</span></span>

### <span data-ttu-id="995d7-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="995d7-116">-BackendAddressPool</span></span>
<span data-ttu-id="995d7-117">Specifica un oggetto **BackendAddressPool** da associare a una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="995d7-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="995d7-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="995d7-119">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="995d7-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="995d7-120">-BackendPort</span></span>
<span data-ttu-id="995d7-121">Specifica la porta back-end per il traffico corrispondente a questa configurazione della regola.</span><span class="sxs-lookup"><span data-stu-id="995d7-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="995d7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="995d7-122">-DefaultProfile</span></span>
<span data-ttu-id="995d7-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="995d7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="995d7-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="995d7-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="995d7-125">Configura SNAT per le macchine virtuali nel pool back-end in modo da usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="995d7-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="995d7-126">-EnableFloatingIP</span></span>
<span data-ttu-id="995d7-127">Indica che questo cmdlet abilita un indirizzo IP mobile per la configurazione di una regola.</span><span class="sxs-lookup"><span data-stu-id="995d7-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="995d7-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="995d7-128">-EnableTcpReset</span></span>
<span data-ttu-id="995d7-129">Ricevere la reimpostazione TCP bidirezionale in un timeout di inattività del flusso TCP o un'interruzione della connessione imprevista.</span><span class="sxs-lookup"><span data-stu-id="995d7-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="995d7-130">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="995d7-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="995d7-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="995d7-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="995d7-132">Specifica un elenco di indirizzi IP front-end da associare a una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="995d7-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="995d7-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="995d7-134">Specifica l'ID per una configurazione dell'indirizzo IP front-end.</span><span class="sxs-lookup"><span data-stu-id="995d7-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="995d7-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="995d7-135">-FrontendPort</span></span>
<span data-ttu-id="995d7-136">Specifica la porta front-end a cui corrisponde una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="995d7-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="995d7-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="995d7-138">Specifica l'intervallo di tempo, in minuti, per cui lo stato delle conversazioni viene gestito in una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="995d7-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="995d7-139">-LoadBalancer</span></span>
<span data-ttu-id="995d7-140">Specifica una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-140">Specifies a load balancer.</span></span>
<span data-ttu-id="995d7-141">Questo cmdlet aggiorna una configurazione della regola per la bilanciamento del carico specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="995d7-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="995d7-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="995d7-142">-LoadDistribution</span></span>
<span data-ttu-id="995d7-143">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-143">Specifies a load distribution.</span></span>
<span data-ttu-id="995d7-144">I valori accettabili per questo parametro sono: SourceIP e SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="995d7-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="995d7-145">-Name</span><span class="sxs-lookup"><span data-stu-id="995d7-145">-Name</span></span>
<span data-ttu-id="995d7-146">Specifica il nome di una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="995d7-147">-Snodato</span><span class="sxs-lookup"><span data-stu-id="995d7-147">-Probe</span></span>
<span data-ttu-id="995d7-148">Specifica un modello da associare a una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="995d7-149">-LambdaId</span><span class="sxs-lookup"><span data-stu-id="995d7-149">-ProbeId</span></span>
<span data-ttu-id="995d7-150">Specifica l'ID dell'elemento da associare a una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="995d7-151">-Protocol</span><span class="sxs-lookup"><span data-stu-id="995d7-151">-Protocol</span></span>
<span data-ttu-id="995d7-152">Specifica il protocollo a cui corrisponde una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="995d7-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="995d7-153">I valori accettabili per questo parametro sono: Tcp o Udp.</span><span class="sxs-lookup"><span data-stu-id="995d7-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="995d7-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="995d7-154">-Confirm</span></span>
<span data-ttu-id="995d7-155">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="995d7-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="995d7-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="995d7-156">-WhatIf</span></span>
<span data-ttu-id="995d7-157">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="995d7-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="995d7-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="995d7-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="995d7-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="995d7-159">CommonParameters</span></span>
<span data-ttu-id="995d7-160">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="995d7-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="995d7-161">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="995d7-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="995d7-162">INPUT</span><span class="sxs-lookup"><span data-stu-id="995d7-162">INPUTS</span></span>

### <span data-ttu-id="995d7-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="995d7-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="995d7-164">System.String</span><span class="sxs-lookup"><span data-stu-id="995d7-164">System.String</span></span>

### <span data-ttu-id="995d7-165">System.Int32</span><span class="sxs-lookup"><span data-stu-id="995d7-165">System.Int32</span></span>

### <span data-ttu-id="995d7-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="995d7-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="995d7-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="995d7-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="995d7-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="995d7-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="995d7-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="995d7-169">OUTPUTS</span></span>

### <span data-ttu-id="995d7-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="995d7-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="995d7-171">NOTE</span><span class="sxs-lookup"><span data-stu-id="995d7-171">NOTES</span></span>

## <span data-ttu-id="995d7-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="995d7-172">RELATED LINKS</span></span>

[<span data-ttu-id="995d7-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="995d7-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="995d7-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="995d7-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="995d7-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="995d7-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="995d7-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="995d7-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="995d7-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="995d7-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


