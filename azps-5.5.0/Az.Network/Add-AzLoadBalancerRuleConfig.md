---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187262"
---
# <span data-ttu-id="98b37-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98b37-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="98b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98b37-102">SYNOPSIS</span></span>
<span data-ttu-id="98b37-103">Aggiunge una configurazione di regola a una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="98b37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98b37-104">SYNTAX</span></span>

### <span data-ttu-id="98b37-105">SetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98b37-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98b37-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="98b37-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98b37-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="98b37-107">DESCRIPTION</span></span>
<span data-ttu-id="98b37-108">Il cmdlet **Add-AzLoadBalancerRuleConfig aggiunge** una configurazione della regola a una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="98b37-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="98b37-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98b37-109">EXAMPLES</span></span>

### <span data-ttu-id="98b37-110">Esempio 1: Aggiungere una configurazione di regole a un servizio di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="98b37-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="98b37-111">Il primo comando ottiene la bilanciamento del carico denominata MyLoadBalancer e quindi la archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="98b37-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="98b37-112">Il secondo comando usa l'operatore della pipeline per passare la bilanciamento del carico in $slb **ad Add-AzLoadBalancerRuleConfig,** che aggiunge la configurazione della regola denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="98b37-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig**, which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="98b37-113">Il terzo comando aggiornerà la bilanciamento del carico in Azure con la nuova configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="98b37-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98b37-114">PARAMETERS</span></span>

### <span data-ttu-id="98b37-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="98b37-115">-BackendAddressPool</span></span>
<span data-ttu-id="98b37-116">Specifica il pool di indirizzi back-end da associare a una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="98b37-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="98b37-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="98b37-118">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="98b37-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="98b37-119">-BackendPort</span></span>
<span data-ttu-id="98b37-120">Specifica la porta back-end per il traffico a cui corrisponde una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="98b37-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b37-121">-DefaultProfile</span></span>
<span data-ttu-id="98b37-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98b37-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98b37-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="98b37-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="98b37-124">Configura SNAT per le macchine virtuali nel pool back-end in modo da usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="98b37-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="98b37-125">-EnableFloatingIP</span></span>
<span data-ttu-id="98b37-126">Indica che questo cmdlet abilita un indirizzo IP mobile per la configurazione di una regola.</span><span class="sxs-lookup"><span data-stu-id="98b37-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="98b37-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="98b37-127">-EnableTcpReset</span></span>
<span data-ttu-id="98b37-128">Ricevere la reimpostazione TCP bidirezionale in un timeout di inattività del flusso TCP o un'interruzione della connessione imprevista.</span><span class="sxs-lookup"><span data-stu-id="98b37-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="98b37-129">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="98b37-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="98b37-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="98b37-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="98b37-131">Specifica un elenco di indirizzi IP front-end da associare a una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="98b37-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="98b37-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="98b37-133">Specifica l'ID per una configurazione dell'indirizzo IP front-end.</span><span class="sxs-lookup"><span data-stu-id="98b37-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="98b37-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="98b37-134">-FrontendPort</span></span>
<span data-ttu-id="98b37-135">Specifica la porta front-end a cui corrisponde una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="98b37-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="98b37-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="98b37-137">Specifica per l'intervallo di tempo, in minuti, che lo stato delle conversazioni viene mantenuto nel bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="98b37-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98b37-138">-LoadBalancer</span></span>
<span data-ttu-id="98b37-139">Specifica un **oggetto LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="98b37-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="98b37-140">Questo cmdlet aggiunge una configurazione della regola al servizio di bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="98b37-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="98b37-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="98b37-141">-LoadDistribution</span></span>
<span data-ttu-id="98b37-142">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="98b37-143">-Name</span><span class="sxs-lookup"><span data-stu-id="98b37-143">-Name</span></span>
<span data-ttu-id="98b37-144">Specifica il nome della configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="98b37-145">-Snodato</span><span class="sxs-lookup"><span data-stu-id="98b37-145">-Probe</span></span>
<span data-ttu-id="98b37-146">Specifica un modello da associare a una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="98b37-147">-LambdaId</span><span class="sxs-lookup"><span data-stu-id="98b37-147">-ProbeId</span></span>
<span data-ttu-id="98b37-148">Specifica l'ID dell'elemento da associare a una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="98b37-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="98b37-149">-Protocol</span></span>
<span data-ttu-id="98b37-150">Specifica il protocollo a cui corrisponde una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="98b37-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="98b37-151">I valori accettabili per questo parametro sono: Tcp o Udp.</span><span class="sxs-lookup"><span data-stu-id="98b37-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="98b37-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98b37-152">-Confirm</span></span>
<span data-ttu-id="98b37-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98b37-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98b37-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98b37-154">-WhatIf</span></span>
<span data-ttu-id="98b37-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98b37-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98b37-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98b37-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98b37-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b37-157">CommonParameters</span></span>
<span data-ttu-id="98b37-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98b37-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b37-159">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98b37-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b37-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="98b37-160">INPUTS</span></span>

### <span data-ttu-id="98b37-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98b37-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="98b37-162">System.String</span><span class="sxs-lookup"><span data-stu-id="98b37-162">System.String</span></span>

### <span data-ttu-id="98b37-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="98b37-163">System.Int32</span></span>

### <span data-ttu-id="98b37-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="98b37-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="98b37-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="98b37-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="98b37-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="98b37-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="98b37-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98b37-167">OUTPUTS</span></span>

### <span data-ttu-id="98b37-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98b37-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="98b37-169">NOTE</span><span class="sxs-lookup"><span data-stu-id="98b37-169">NOTES</span></span>

## <span data-ttu-id="98b37-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98b37-170">RELATED LINKS</span></span>

[<span data-ttu-id="98b37-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98b37-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="98b37-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98b37-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="98b37-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98b37-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="98b37-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98b37-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="98b37-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98b37-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


