---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 871982993492ba8eb06d818759e31d3c3500c1d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515052"
---
# <span data-ttu-id="af22c-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af22c-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="af22c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af22c-102">SYNOPSIS</span></span>
<span data-ttu-id="af22c-103">Crea una configurazione di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="af22c-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af22c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af22c-104">SYNTAX</span></span>

### <span data-ttu-id="af22c-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af22c-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af22c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="af22c-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af22c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af22c-107">DESCRIPTION</span></span>
<span data-ttu-id="af22c-108">Il cmdlet **New-AzureRmLoadBalancerRuleConfig** crea una configurazione di regola per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="af22c-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="af22c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af22c-109">EXAMPLES</span></span>

### <span data-ttu-id="af22c-110">1: creazione di una configurazione di regola per un bilanciamento del carico di Azure</span><span class="sxs-lookup"><span data-stu-id="af22c-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="af22c-111">I primi tre comandi configurano un IP pubblico, un front-end e una sonda per la configurazione della regola nel comando avanti.</span><span class="sxs-lookup"><span data-stu-id="af22c-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="af22c-112">Il comando avanti crea una nuova regola denominata MyLBrule con determinate specifiche.</span><span class="sxs-lookup"><span data-stu-id="af22c-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="af22c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af22c-113">PARAMETERS</span></span>

### <span data-ttu-id="af22c-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af22c-114">-BackendAddressPool</span></span>
<span data-ttu-id="af22c-115">Specifica un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="af22c-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="af22c-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="af22c-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="af22c-117">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="af22c-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="af22c-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="af22c-118">-BackendPort</span></span>
<span data-ttu-id="af22c-119">Specifica la porta backend per il traffico che corrisponde alla configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="af22c-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="af22c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af22c-120">-DefaultProfile</span></span>
<span data-ttu-id="af22c-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af22c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af22c-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="af22c-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="af22c-123">Configura SNAT per le VM nel pool back-end per usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="af22c-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="af22c-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="af22c-124">-EnableFloatingIP</span></span>
<span data-ttu-id="af22c-125">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="af22c-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="af22c-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="af22c-126">-EnableTcpReset</span></span>
<span data-ttu-id="af22c-127">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="af22c-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="af22c-128">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="af22c-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="af22c-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="af22c-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="af22c-130">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="af22c-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="af22c-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="af22c-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="af22c-132">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="af22c-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="af22c-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="af22c-133">-FrontendPort</span></span>
<span data-ttu-id="af22c-134">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="af22c-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="af22c-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="af22c-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="af22c-136">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="af22c-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="af22c-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="af22c-137">-LoadDistribution</span></span>
<span data-ttu-id="af22c-138">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="af22c-138">Specifies a load distribution.</span></span>
<span data-ttu-id="af22c-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="af22c-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="af22c-140">Predefinita</span><span class="sxs-lookup"><span data-stu-id="af22c-140">Default</span></span>
- <span data-ttu-id="af22c-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="af22c-141">SourceIP</span></span>
- <span data-ttu-id="af22c-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="af22c-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="af22c-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="af22c-143">-Name</span></span>
<span data-ttu-id="af22c-144">Specifica il nome della regola di bilanciamento del carico creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af22c-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="af22c-145">-Probe</span><span class="sxs-lookup"><span data-stu-id="af22c-145">-Probe</span></span>
<span data-ttu-id="af22c-146">Specifica una sonda da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="af22c-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="af22c-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="af22c-147">-ProbeId</span></span>
<span data-ttu-id="af22c-148">Specifica l'ID del Probe da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="af22c-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="af22c-149">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="af22c-149">-Protocol</span></span>
<span data-ttu-id="af22c-150">Specifica il protocollo corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="af22c-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="af22c-151">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="af22c-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="af22c-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af22c-152">-Confirm</span></span>
<span data-ttu-id="af22c-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af22c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af22c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af22c-154">-WhatIf</span></span>
<span data-ttu-id="af22c-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af22c-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af22c-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af22c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af22c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af22c-157">CommonParameters</span></span>
<span data-ttu-id="af22c-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af22c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af22c-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af22c-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af22c-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af22c-160">INPUTS</span></span>

### <span data-ttu-id="af22c-161">Nessuno</span><span class="sxs-lookup"><span data-stu-id="af22c-161">None</span></span>

## <span data-ttu-id="af22c-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af22c-162">OUTPUTS</span></span>

### <span data-ttu-id="af22c-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="af22c-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="af22c-164">Note</span><span class="sxs-lookup"><span data-stu-id="af22c-164">NOTES</span></span>

## <span data-ttu-id="af22c-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af22c-165">RELATED LINKS</span></span>

[<span data-ttu-id="af22c-166">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af22c-166">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="af22c-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af22c-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="af22c-168">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af22c-168">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="af22c-169">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af22c-169">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


