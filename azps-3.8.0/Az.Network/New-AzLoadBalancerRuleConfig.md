---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d93bf82421851a79399061861ed9f2ca29d9a5c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864301"
---
# <span data-ttu-id="3a329-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a329-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="3a329-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a329-102">SYNOPSIS</span></span>
<span data-ttu-id="3a329-103">Crea una configurazione di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3a329-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="3a329-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a329-104">SYNTAX</span></span>

### <span data-ttu-id="3a329-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3a329-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a329-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3a329-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a329-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a329-107">DESCRIPTION</span></span>
<span data-ttu-id="3a329-108">Il cmdlet **New-AzLoadBalancerRuleConfig** crea una configurazione di regola per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="3a329-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="3a329-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a329-109">EXAMPLES</span></span>

### <span data-ttu-id="3a329-110">1: creazione di una configurazione di regola per un bilanciamento del carico di Azure</span><span class="sxs-lookup"><span data-stu-id="3a329-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="3a329-111">I primi tre comandi configurano un IP pubblico, un front-end e una sonda per la configurazione della regola nel comando avanti.</span><span class="sxs-lookup"><span data-stu-id="3a329-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="3a329-112">Il comando avanti crea una nuova regola denominata MyLBrule con determinate specifiche.</span><span class="sxs-lookup"><span data-stu-id="3a329-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="3a329-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a329-113">PARAMETERS</span></span>

### <span data-ttu-id="3a329-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3a329-114">-BackendAddressPool</span></span>
<span data-ttu-id="3a329-115">Specifica un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3a329-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3a329-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3a329-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="3a329-117">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3a329-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3a329-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="3a329-118">-BackendPort</span></span>
<span data-ttu-id="3a329-119">Specifica la porta backend per il traffico che corrisponde alla configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3a329-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3a329-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a329-120">-DefaultProfile</span></span>
<span data-ttu-id="3a329-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a329-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a329-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="3a329-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="3a329-123">Configura SNAT per le VM nel pool back-end per usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3a329-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="3a329-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="3a329-124">-EnableFloatingIP</span></span>
<span data-ttu-id="3a329-125">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="3a329-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="3a329-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="3a329-126">-EnableTcpReset</span></span>
<span data-ttu-id="3a329-127">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="3a329-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="3a329-128">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="3a329-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="3a329-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a329-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="3a329-130">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3a329-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3a329-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3a329-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="3a329-132">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3a329-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="3a329-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="3a329-133">-FrontendPort</span></span>
<span data-ttu-id="3a329-134">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3a329-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3a329-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="3a329-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3a329-136">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3a329-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="3a329-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="3a329-137">-LoadDistribution</span></span>
<span data-ttu-id="3a329-138">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="3a329-138">Specifies a load distribution.</span></span>
<span data-ttu-id="3a329-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a329-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3a329-140">Predefinita</span><span class="sxs-lookup"><span data-stu-id="3a329-140">Default</span></span>
- <span data-ttu-id="3a329-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="3a329-141">SourceIP</span></span>
- <span data-ttu-id="3a329-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="3a329-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="3a329-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a329-143">-Name</span></span>
<span data-ttu-id="3a329-144">Specifica il nome della regola di bilanciamento del carico creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a329-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3a329-145">-Probe</span><span class="sxs-lookup"><span data-stu-id="3a329-145">-Probe</span></span>
<span data-ttu-id="3a329-146">Specifica una sonda da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3a329-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3a329-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="3a329-147">-ProbeId</span></span>
<span data-ttu-id="3a329-148">Specifica l'ID del Probe da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3a329-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3a329-149">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="3a329-149">-Protocol</span></span>
<span data-ttu-id="3a329-150">Specifica il protocollo corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3a329-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="3a329-151">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="3a329-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="3a329-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3a329-152">-Confirm</span></span>
<span data-ttu-id="3a329-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a329-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a329-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a329-154">-WhatIf</span></span>
<span data-ttu-id="3a329-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a329-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a329-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a329-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a329-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a329-157">CommonParameters</span></span>
<span data-ttu-id="3a329-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a329-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a329-159">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a329-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a329-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a329-160">INPUTS</span></span>

### <span data-ttu-id="3a329-161">System. String</span><span class="sxs-lookup"><span data-stu-id="3a329-161">System.String</span></span>

### <span data-ttu-id="3a329-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3a329-162">System.Int32</span></span>

### <span data-ttu-id="3a329-163">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a329-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="3a329-164">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3a329-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="3a329-165">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="3a329-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="3a329-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a329-166">OUTPUTS</span></span>

### <span data-ttu-id="3a329-167">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="3a329-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="3a329-168">Note</span><span class="sxs-lookup"><span data-stu-id="3a329-168">NOTES</span></span>

## <span data-ttu-id="3a329-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a329-169">RELATED LINKS</span></span>

[<span data-ttu-id="3a329-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a329-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3a329-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a329-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3a329-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a329-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3a329-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a329-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


