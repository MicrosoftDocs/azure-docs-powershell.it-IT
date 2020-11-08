---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200506"
---
# <span data-ttu-id="6538c-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6538c-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="6538c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6538c-102">SYNOPSIS</span></span>
<span data-ttu-id="6538c-103">Aggiunge una configurazione di regola a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="6538c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6538c-104">SYNTAX</span></span>

### <span data-ttu-id="6538c-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6538c-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6538c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6538c-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6538c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6538c-107">DESCRIPTION</span></span>
<span data-ttu-id="6538c-108">Il cmdlet **Add-AzLoadBalancerRuleConfig** aggiunge una configurazione di regola a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="6538c-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="6538c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6538c-109">EXAMPLES</span></span>

### <span data-ttu-id="6538c-110">Esempio 1: aggiungere una configurazione di regola a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="6538c-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="6538c-111">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="6538c-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="6538c-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a **Add-AzLoadBalancerRuleConfig** , che aggiunge la configurazione della regola denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="6538c-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="6538c-113">Il terzo comando aggiornerà il bilanciamento del carico in Azure con la nuova configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="6538c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6538c-114">PARAMETERS</span></span>

### <span data-ttu-id="6538c-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6538c-115">-BackendAddressPool</span></span>
<span data-ttu-id="6538c-116">Specifica il pool di indirizzi di backend da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6538c-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6538c-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="6538c-118">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6538c-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="6538c-119">-BackendPort</span></span>
<span data-ttu-id="6538c-120">Specifica la porta di backend per il traffico che corrisponde a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6538c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6538c-121">-DefaultProfile</span></span>
<span data-ttu-id="6538c-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6538c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6538c-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="6538c-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="6538c-124">Configura SNAT per le VM nel pool back-end per usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="6538c-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="6538c-125">-EnableFloatingIP</span></span>
<span data-ttu-id="6538c-126">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="6538c-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6538c-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="6538c-127">-EnableTcpReset</span></span>
<span data-ttu-id="6538c-128">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="6538c-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="6538c-129">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="6538c-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="6538c-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6538c-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6538c-131">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6538c-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6538c-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6538c-133">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="6538c-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6538c-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6538c-134">-FrontendPort</span></span>
<span data-ttu-id="6538c-135">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6538c-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6538c-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6538c-137">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto nel bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="6538c-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6538c-138">-LoadBalancer</span></span>
<span data-ttu-id="6538c-139">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="6538c-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="6538c-140">Questo cmdlet aggiunge una configurazione di regola al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6538c-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="6538c-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="6538c-141">-LoadDistribution</span></span>
<span data-ttu-id="6538c-142">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="6538c-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="6538c-143">-Name</span></span>
<span data-ttu-id="6538c-144">Specifica il nome della configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6538c-145">-Probe</span><span class="sxs-lookup"><span data-stu-id="6538c-145">-Probe</span></span>
<span data-ttu-id="6538c-146">Specifica una sonda da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6538c-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="6538c-147">-ProbeId</span></span>
<span data-ttu-id="6538c-148">Specifica l'ID del Probe da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6538c-149">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="6538c-149">-Protocol</span></span>
<span data-ttu-id="6538c-150">Specifica il protocollo corrispondente a una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6538c-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="6538c-151">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="6538c-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="6538c-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6538c-152">-Confirm</span></span>
<span data-ttu-id="6538c-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6538c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6538c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6538c-154">-WhatIf</span></span>
<span data-ttu-id="6538c-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6538c-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6538c-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6538c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6538c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6538c-157">CommonParameters</span></span>
<span data-ttu-id="6538c-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6538c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6538c-159">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6538c-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6538c-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6538c-160">INPUTS</span></span>

### <span data-ttu-id="6538c-161">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6538c-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="6538c-162">System. String</span><span class="sxs-lookup"><span data-stu-id="6538c-162">System.String</span></span>

### <span data-ttu-id="6538c-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6538c-163">System.Int32</span></span>

### <span data-ttu-id="6538c-164">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6538c-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="6538c-165">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6538c-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="6538c-166">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="6538c-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="6538c-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6538c-167">OUTPUTS</span></span>

### <span data-ttu-id="6538c-168">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6538c-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6538c-169">Note</span><span class="sxs-lookup"><span data-stu-id="6538c-169">NOTES</span></span>

## <span data-ttu-id="6538c-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6538c-170">RELATED LINKS</span></span>

[<span data-ttu-id="6538c-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6538c-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6538c-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6538c-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6538c-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6538c-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6538c-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6538c-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6538c-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6538c-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


