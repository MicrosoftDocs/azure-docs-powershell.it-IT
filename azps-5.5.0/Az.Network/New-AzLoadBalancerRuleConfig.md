---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193647"
---
# <span data-ttu-id="f036e-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f036e-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="f036e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f036e-102">SYNOPSIS</span></span>
<span data-ttu-id="f036e-103">Crea una configurazione delle regole per una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f036e-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="f036e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f036e-104">SYNTAX</span></span>

### <span data-ttu-id="f036e-105">SetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f036e-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f036e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f036e-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f036e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f036e-107">DESCRIPTION</span></span>
<span data-ttu-id="f036e-108">Il cmdlet **New-AzLoadBalancerRuleConfig crea** una configurazione di regola per una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="f036e-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f036e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f036e-109">EXAMPLES</span></span>

### <span data-ttu-id="f036e-110">Esempio 1: Creazione di una configurazione di regole per un servizio di bilanciamento del carico di Azure</span><span class="sxs-lookup"><span data-stu-id="f036e-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
```powershell
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" `
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd `
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port `
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration `
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp `
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP `
    -LoadDistribution SourceIP
```

<span data-ttu-id="f036e-111">I primi tre comandi configurano un indirizzo IP pubblico, un front-end e un altro per la configurazione delle regole nel forth comando.</span><span class="sxs-lookup"><span data-stu-id="f036e-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="f036e-112">Il forth comando crea una nuova regola denominata MyLBrule con specifiche specifiche.</span><span class="sxs-lookup"><span data-stu-id="f036e-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="f036e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f036e-113">PARAMETERS</span></span>

### <span data-ttu-id="f036e-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f036e-114">-BackendAddressPool</span></span>
<span data-ttu-id="f036e-115">Specifica un oggetto **BackendAddressPool** da associare a una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f036e-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f036e-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f036e-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="f036e-117">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f036e-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f036e-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="f036e-118">-BackendPort</span></span>
<span data-ttu-id="f036e-119">Specifica la porta back-end per il traffico corrispondente a questa configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f036e-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f036e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f036e-120">-DefaultProfile</span></span>
<span data-ttu-id="f036e-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f036e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f036e-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="f036e-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="f036e-123">Configura SNAT per le macchine virtuali nel pool back-end in modo da usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f036e-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="f036e-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="f036e-124">-EnableFloatingIP</span></span>
<span data-ttu-id="f036e-125">Indica che questo cmdlet abilita un indirizzo IP mobile per la configurazione di una regola.</span><span class="sxs-lookup"><span data-stu-id="f036e-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="f036e-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="f036e-126">-EnableTcpReset</span></span>
<span data-ttu-id="f036e-127">Ricevere la reimpostazione TCP bidirezionale in un timeout di inattività del flusso TCP o un'interruzione della connessione imprevista.</span><span class="sxs-lookup"><span data-stu-id="f036e-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="f036e-128">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="f036e-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="f036e-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f036e-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f036e-130">Specifica un elenco di indirizzi IP front-end da associare a una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f036e-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f036e-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f036e-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="f036e-132">Specifica l'ID per una configurazione dell'indirizzo IP front-end.</span><span class="sxs-lookup"><span data-stu-id="f036e-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="f036e-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f036e-133">-FrontendPort</span></span>
<span data-ttu-id="f036e-134">Specifica la porta front-end a cui corrisponde una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f036e-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f036e-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f036e-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f036e-136">Specifica per l'intervallo di tempo, in minuti, che lo stato delle conversazioni viene mantenuto in una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f036e-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="f036e-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="f036e-137">-LoadDistribution</span></span>
<span data-ttu-id="f036e-138">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="f036e-138">Specifies a load distribution.</span></span>
<span data-ttu-id="f036e-139">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="f036e-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f036e-140">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="f036e-140">Default</span></span>
- <span data-ttu-id="f036e-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="f036e-141">SourceIP</span></span>
- <span data-ttu-id="f036e-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="f036e-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="f036e-143">-Name</span><span class="sxs-lookup"><span data-stu-id="f036e-143">-Name</span></span>
<span data-ttu-id="f036e-144">Specifica il nome della regola di bilanciamento del carico creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f036e-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f036e-145">-Snodato</span><span class="sxs-lookup"><span data-stu-id="f036e-145">-Probe</span></span>
<span data-ttu-id="f036e-146">Specifica un modello da associare a una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f036e-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f036e-147">-LambdaId</span><span class="sxs-lookup"><span data-stu-id="f036e-147">-ProbeId</span></span>
<span data-ttu-id="f036e-148">Specifica l'ID dell'elemento da associare a una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f036e-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f036e-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f036e-149">-Protocol</span></span>
<span data-ttu-id="f036e-150">Specifica il protocollo a cui corrisponde una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f036e-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="f036e-151">I valori accettabili per questo parametro sono: Tcp o Udp.</span><span class="sxs-lookup"><span data-stu-id="f036e-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="f036e-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f036e-152">-Confirm</span></span>
<span data-ttu-id="f036e-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f036e-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f036e-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f036e-154">-WhatIf</span></span>
<span data-ttu-id="f036e-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f036e-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f036e-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f036e-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f036e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f036e-157">CommonParameters</span></span>
<span data-ttu-id="f036e-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f036e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f036e-159">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f036e-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f036e-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="f036e-160">INPUTS</span></span>

### <span data-ttu-id="f036e-161">System.String</span><span class="sxs-lookup"><span data-stu-id="f036e-161">System.String</span></span>

### <span data-ttu-id="f036e-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f036e-162">System.Int32</span></span>

### <span data-ttu-id="f036e-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f036e-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="f036e-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f036e-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="f036e-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="f036e-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="f036e-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f036e-166">OUTPUTS</span></span>

### <span data-ttu-id="f036e-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="f036e-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="f036e-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="f036e-168">NOTES</span></span>

## <span data-ttu-id="f036e-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f036e-169">RELATED LINKS</span></span>

[<span data-ttu-id="f036e-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f036e-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f036e-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f036e-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f036e-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f036e-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f036e-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f036e-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


