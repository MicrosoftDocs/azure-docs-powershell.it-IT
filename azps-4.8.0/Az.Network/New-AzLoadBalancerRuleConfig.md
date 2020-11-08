---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189522"
---
# <span data-ttu-id="b4d93-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4d93-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="b4d93-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4d93-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d93-103">Crea una configurazione di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b4d93-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="b4d93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4d93-104">SYNTAX</span></span>

### <span data-ttu-id="b4d93-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4d93-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d93-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d93-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4d93-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4d93-107">DESCRIPTION</span></span>
<span data-ttu-id="b4d93-108">Il cmdlet **New-AzLoadBalancerRuleConfig** crea una configurazione di regola per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d93-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="b4d93-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4d93-109">EXAMPLES</span></span>

### <span data-ttu-id="b4d93-110">Esempio 1: creazione di una configurazione di una regola per un bilanciamento del carico di Azure</span><span class="sxs-lookup"><span data-stu-id="b4d93-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
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

<span data-ttu-id="b4d93-111">I primi tre comandi configurano un IP pubblico, un front-end e una sonda per la configurazione della regola nel comando avanti.</span><span class="sxs-lookup"><span data-stu-id="b4d93-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="b4d93-112">Il comando avanti crea una nuova regola denominata MyLBrule con determinate specifiche.</span><span class="sxs-lookup"><span data-stu-id="b4d93-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="b4d93-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4d93-113">PARAMETERS</span></span>

### <span data-ttu-id="b4d93-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4d93-114">-BackendAddressPool</span></span>
<span data-ttu-id="b4d93-115">Specifica un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b4d93-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b4d93-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b4d93-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="b4d93-117">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b4d93-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b4d93-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b4d93-118">-BackendPort</span></span>
<span data-ttu-id="b4d93-119">Specifica la porta backend per il traffico che corrisponde alla configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b4d93-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b4d93-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d93-120">-DefaultProfile</span></span>
<span data-ttu-id="b4d93-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d93-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4d93-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="b4d93-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="b4d93-123">Configura SNAT per le VM nel pool back-end per usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b4d93-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="b4d93-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b4d93-124">-EnableFloatingIP</span></span>
<span data-ttu-id="b4d93-125">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="b4d93-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="b4d93-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="b4d93-126">-EnableTcpReset</span></span>
<span data-ttu-id="b4d93-127">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="b4d93-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="b4d93-128">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="b4d93-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b4d93-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d93-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b4d93-130">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b4d93-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b4d93-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b4d93-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="b4d93-132">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="b4d93-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="b4d93-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b4d93-133">-FrontendPort</span></span>
<span data-ttu-id="b4d93-134">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b4d93-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b4d93-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b4d93-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b4d93-136">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b4d93-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="b4d93-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="b4d93-137">-LoadDistribution</span></span>
<span data-ttu-id="b4d93-138">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="b4d93-138">Specifies a load distribution.</span></span>
<span data-ttu-id="b4d93-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b4d93-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4d93-140">Predefinita</span><span class="sxs-lookup"><span data-stu-id="b4d93-140">Default</span></span>
- <span data-ttu-id="b4d93-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="b4d93-141">SourceIP</span></span>
- <span data-ttu-id="b4d93-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="b4d93-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="b4d93-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4d93-143">-Name</span></span>
<span data-ttu-id="b4d93-144">Specifica il nome della regola di bilanciamento del carico creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4d93-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b4d93-145">-Probe</span><span class="sxs-lookup"><span data-stu-id="b4d93-145">-Probe</span></span>
<span data-ttu-id="b4d93-146">Specifica una sonda da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b4d93-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b4d93-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="b4d93-147">-ProbeId</span></span>
<span data-ttu-id="b4d93-148">Specifica l'ID del Probe da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b4d93-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b4d93-149">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="b4d93-149">-Protocol</span></span>
<span data-ttu-id="b4d93-150">Specifica il protocollo corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="b4d93-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="b4d93-151">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="b4d93-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="b4d93-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b4d93-152">-Confirm</span></span>
<span data-ttu-id="b4d93-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4d93-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4d93-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4d93-154">-WhatIf</span></span>
<span data-ttu-id="b4d93-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4d93-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4d93-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4d93-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4d93-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d93-157">CommonParameters</span></span>
<span data-ttu-id="b4d93-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d93-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d93-159">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d93-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d93-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4d93-160">INPUTS</span></span>

### <span data-ttu-id="b4d93-161">System. String</span><span class="sxs-lookup"><span data-stu-id="b4d93-161">System.String</span></span>

### <span data-ttu-id="b4d93-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b4d93-162">System.Int32</span></span>

### <span data-ttu-id="b4d93-163">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d93-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="b4d93-164">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4d93-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="b4d93-165">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="b4d93-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="b4d93-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4d93-166">OUTPUTS</span></span>

### <span data-ttu-id="b4d93-167">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="b4d93-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="b4d93-168">Note</span><span class="sxs-lookup"><span data-stu-id="b4d93-168">NOTES</span></span>

## <span data-ttu-id="b4d93-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4d93-169">RELATED LINKS</span></span>

[<span data-ttu-id="b4d93-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4d93-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b4d93-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4d93-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b4d93-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4d93-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b4d93-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4d93-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)

