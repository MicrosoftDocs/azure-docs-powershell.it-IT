---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 44f8304ce1ee79c114dc4054c8dd7fff3dcd22fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006509"
---
# <span data-ttu-id="e1c18-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e1c18-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="e1c18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1c18-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c18-103">Aggiunge una configurazione della regola NAT in ingresso a una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e1c18-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="e1c18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1c18-104">SYNTAX</span></span>

### <span data-ttu-id="e1c18-105">SetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e1c18-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1c18-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1c18-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1c18-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1c18-107">DESCRIPTION</span></span>
<span data-ttu-id="e1c18-108">Il cmdlet **Add-AzLoadBalancerInboundNatRuleConfig** aggiunge una configurazione della regola NAT (Network Address Translation) in ingresso in una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c18-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="e1c18-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1c18-109">EXAMPLES</span></span>

### <span data-ttu-id="e1c18-110">Esempio 1: Aggiungere una configurazione di regola NAT in ingresso a una bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="e1c18-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="e1c18-111">Il primo comando ottiene la bilanciamento del carico denominata MyloadBalancer e quindi la archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="e1c18-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="e1c18-112">Il secondo comando usa l'operatore della pipeline per passare la bilanciamento del carico in $slb **ad Add-AzLoadBalancerInboundNatRuleConfig,** che aggiunge una configurazione della regola NAT in ingresso al bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e1c18-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>
<span data-ttu-id="e1c18-113">L'ultimo comando imposta la configurazione sul bilanciamento del carico. Se non si esegue Set-AzLoadBalancer, le modifiche non verranno applicate al bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e1c18-113">The last command sets the configuration to the loadbalancer, if you don't perform Set-AzLoadBalancer, your changes will not be applied to the loadbalancer.</span></span>

## <span data-ttu-id="e1c18-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1c18-114">PARAMETERS</span></span>

### <span data-ttu-id="e1c18-115">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="e1c18-115">-BackendPort</span></span>
<span data-ttu-id="e1c18-116">Specifica la porta back-end per il traffico corrispondente a una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="e1c18-116">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="e1c18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c18-117">-DefaultProfile</span></span>
<span data-ttu-id="e1c18-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c18-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1c18-119">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="e1c18-119">-EnableFloatingIP</span></span>
<span data-ttu-id="e1c18-120">Indica che questo cmdlet abilita un indirizzo IP mobile per la configurazione di una regola.</span><span class="sxs-lookup"><span data-stu-id="e1c18-120">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="e1c18-121">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="e1c18-121">-EnableTcpReset</span></span>
<span data-ttu-id="e1c18-122">Ricevere la reimpostazione TCP bidirezionale in un timeout di inattività del flusso TCP o un'interruzione della connessione imprevista.</span><span class="sxs-lookup"><span data-stu-id="e1c18-122">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="e1c18-123">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="e1c18-123">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="e1c18-124">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1c18-124">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e1c18-125">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="e1c18-125">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="e1c18-126">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e1c18-126">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="e1c18-127">Specifica un ID per la configurazione di un indirizzo IP front-end.</span><span class="sxs-lookup"><span data-stu-id="e1c18-127">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="e1c18-128">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="e1c18-128">-FrontendPort</span></span>
<span data-ttu-id="e1c18-129">Specifica la porta front-end a cui corrisponde una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="e1c18-129">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="e1c18-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e1c18-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e1c18-131">Specifica per l'intervallo di tempo, in minuti, che lo stato delle conversazioni viene mantenuto in una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e1c18-131">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="e1c18-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e1c18-132">-LoadBalancer</span></span>
<span data-ttu-id="e1c18-133">Specifica un **oggetto LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="e1c18-133">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="e1c18-134">Questo cmdlet aggiunge una configurazione della regola NAT in ingresso alla bilanciamento del carico specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e1c18-134">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="e1c18-135">-Name</span><span class="sxs-lookup"><span data-stu-id="e1c18-135">-Name</span></span>
<span data-ttu-id="e1c18-136">Specifica il nome della configurazione della regola NAT in ingresso da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e1c18-136">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="e1c18-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e1c18-137">-Protocol</span></span>
<span data-ttu-id="e1c18-138">Specifica il protocollo a cui corrisponde una regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="e1c18-138">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="e1c18-139">I valori accettabili per questo parametro sono: Tcp o Udp.</span><span class="sxs-lookup"><span data-stu-id="e1c18-139">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="e1c18-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1c18-140">-Confirm</span></span>
<span data-ttu-id="e1c18-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1c18-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1c18-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1c18-142">-WhatIf</span></span>
<span data-ttu-id="e1c18-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1c18-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1c18-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1c18-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1c18-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c18-145">CommonParameters</span></span>
<span data-ttu-id="e1c18-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c18-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c18-147">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1c18-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c18-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1c18-148">INPUTS</span></span>

### <span data-ttu-id="e1c18-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e1c18-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="e1c18-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e1c18-150">System.String</span></span>

### <span data-ttu-id="e1c18-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e1c18-151">System.Int32</span></span>

### <span data-ttu-id="e1c18-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1c18-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="e1c18-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1c18-153">OUTPUTS</span></span>

### <span data-ttu-id="e1c18-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e1c18-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e1c18-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1c18-155">NOTES</span></span>

## <span data-ttu-id="e1c18-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1c18-156">RELATED LINKS</span></span>

[<span data-ttu-id="e1c18-157">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e1c18-157">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e1c18-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e1c18-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e1c18-159">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e1c18-159">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e1c18-160">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e1c18-160">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e1c18-161">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e1c18-161">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="e1c18-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e1c18-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


