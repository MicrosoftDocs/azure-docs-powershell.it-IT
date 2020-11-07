---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 580351ae3b46eb3f1c1d8bfd5c3562fdd208556e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678661"
---
# <span data-ttu-id="c133f-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c133f-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="c133f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c133f-102">SYNOPSIS</span></span>
<span data-ttu-id="c133f-103">Aggiunge una configurazione di regola a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="c133f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c133f-104">SYNTAX</span></span>

### <span data-ttu-id="c133f-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c133f-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c133f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c133f-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c133f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c133f-107">DESCRIPTION</span></span>
<span data-ttu-id="c133f-108">Il cmdlet **Add-AzLoadBalancerRuleConfig** aggiunge una configurazione di regola a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="c133f-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="c133f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c133f-109">EXAMPLES</span></span>

### <span data-ttu-id="c133f-110">Esempio 1: aggiungere una configurazione di regola a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="c133f-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="c133f-111">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="c133f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="c133f-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a **Add-AzLoadBalancerRuleConfig** , che aggiunge la configurazione della regola denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="c133f-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="c133f-113">Il terzo comando aggiornerà il bilanciamento del carico in Azure con la nuova configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="c133f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c133f-114">PARAMETERS</span></span>

### <span data-ttu-id="c133f-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c133f-115">-BackendAddressPool</span></span>
<span data-ttu-id="c133f-116">Specifica il pool di indirizzi di backend da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c133f-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c133f-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="c133f-118">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c133f-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c133f-119">-BackendPort</span></span>
<span data-ttu-id="c133f-120">Specifica la porta di backend per il traffico che corrisponde a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c133f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c133f-121">-DefaultProfile</span></span>
<span data-ttu-id="c133f-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c133f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c133f-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="c133f-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="c133f-124">Configura SNAT per le VM nel pool back-end per usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="c133f-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c133f-125">-EnableFloatingIP</span></span>
<span data-ttu-id="c133f-126">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="c133f-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="c133f-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c133f-127">-EnableTcpReset</span></span>
<span data-ttu-id="c133f-128">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="c133f-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c133f-129">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="c133f-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c133f-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c133f-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c133f-131">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c133f-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c133f-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c133f-133">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="c133f-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="c133f-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c133f-134">-FrontendPort</span></span>
<span data-ttu-id="c133f-135">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c133f-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c133f-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c133f-137">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto nel bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="c133f-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c133f-138">-LoadBalancer</span></span>
<span data-ttu-id="c133f-139">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="c133f-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="c133f-140">Questo cmdlet aggiunge una configurazione di regola al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c133f-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="c133f-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="c133f-141">-LoadDistribution</span></span>
<span data-ttu-id="c133f-142">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="c133f-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="c133f-143">-Name</span></span>
<span data-ttu-id="c133f-144">Specifica il nome della configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c133f-145">-Probe</span><span class="sxs-lookup"><span data-stu-id="c133f-145">-Probe</span></span>
<span data-ttu-id="c133f-146">Specifica una sonda da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c133f-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="c133f-147">-ProbeId</span></span>
<span data-ttu-id="c133f-148">Specifica l'ID del Probe da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c133f-149">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="c133f-149">-Protocol</span></span>
<span data-ttu-id="c133f-150">Specifica il protocollo che corrisponde a una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c133f-150">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="c133f-151">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="c133f-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="c133f-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c133f-152">-Confirm</span></span>
<span data-ttu-id="c133f-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c133f-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c133f-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c133f-154">-WhatIf</span></span>
<span data-ttu-id="c133f-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c133f-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c133f-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c133f-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c133f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c133f-157">CommonParameters</span></span>
<span data-ttu-id="c133f-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c133f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c133f-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c133f-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c133f-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c133f-160">INPUTS</span></span>

### <span data-ttu-id="c133f-161">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c133f-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c133f-162">System. String</span><span class="sxs-lookup"><span data-stu-id="c133f-162">System.String</span></span>

### <span data-ttu-id="c133f-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c133f-163">System.Int32</span></span>

### <span data-ttu-id="c133f-164">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c133f-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="c133f-165">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c133f-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="c133f-166">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="c133f-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="c133f-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c133f-167">OUTPUTS</span></span>

### <span data-ttu-id="c133f-168">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c133f-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c133f-169">Note</span><span class="sxs-lookup"><span data-stu-id="c133f-169">NOTES</span></span>

## <span data-ttu-id="c133f-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c133f-170">RELATED LINKS</span></span>

[<span data-ttu-id="c133f-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c133f-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c133f-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c133f-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c133f-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c133f-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c133f-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c133f-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c133f-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c133f-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)

