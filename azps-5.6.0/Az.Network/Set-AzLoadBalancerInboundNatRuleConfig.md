---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: a0d5adbc1e3fb2b38ded91431ab0cf349c541ebd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963886"
---
# <span data-ttu-id="6490a-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6490a-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="6490a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6490a-102">SYNOPSIS</span></span>
<span data-ttu-id="6490a-103">Imposta una configurazione della regola NAT in ingresso per una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6490a-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="6490a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6490a-104">SYNTAX</span></span>

### <span data-ttu-id="6490a-105">SetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6490a-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6490a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6490a-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6490a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6490a-107">DESCRIPTION</span></span>
<span data-ttu-id="6490a-108">Il cmdlet **Set-AzLoadBalancerInboundNatRuleConfig** imposta una configurazione della regola NAT (Network Address Translation) in ingresso per una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="6490a-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="6490a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6490a-109">EXAMPLES</span></span>

### <span data-ttu-id="6490a-110">Esempio 1: Modificare la configurazione della regola NAT in ingresso in un servizio di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="6490a-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="6490a-111">Il primo comando recupera la bilanciamento del carico denominata MyLoadBalancer e quindi la archivia nella $slb variabile.</span><span class="sxs-lookup"><span data-stu-id="6490a-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="6490a-112">Il secondo comando usa l'operatore della pipeline per passare la bilanciamento del carico in $slb ad Add-AzLoadBalancerInboundNatRuleConfig, che aggiunge una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="6490a-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="6490a-113">Il terzo comando passa la bilanciamento del carico a **Set-AzLoadBalancerInboundNatRuleConfig,** che salva e aggiorna la configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="6490a-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig**, which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="6490a-114">Si noti che la configurazione della regola è stata impostata senza abilitare l'IP mobile, che era stato abilitato dal comando precedente.</span><span class="sxs-lookup"><span data-stu-id="6490a-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="6490a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6490a-115">PARAMETERS</span></span>

### <span data-ttu-id="6490a-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="6490a-116">-BackendPort</span></span>
<span data-ttu-id="6490a-117">Specifica la porta back-end per il traffico corrispondente a questa configurazione della regola.</span><span class="sxs-lookup"><span data-stu-id="6490a-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="6490a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6490a-118">-DefaultProfile</span></span>
<span data-ttu-id="6490a-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6490a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6490a-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="6490a-120">-EnableFloatingIP</span></span>
<span data-ttu-id="6490a-121">Indica che questo cmdlet abilita un indirizzo IP mobile per la configurazione di una regola.</span><span class="sxs-lookup"><span data-stu-id="6490a-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6490a-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="6490a-122">-EnableTcpReset</span></span>
<span data-ttu-id="6490a-123">Ricevere la reimpostazione TCP bidirezionale in un timeout di inattività del flusso TCP o un'interruzione della connessione imprevista.</span><span class="sxs-lookup"><span data-stu-id="6490a-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="6490a-124">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="6490a-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="6490a-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6490a-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6490a-126">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="6490a-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="6490a-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6490a-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6490a-128">Specifica l'ID per una configurazione dell'indirizzo IP front-end.</span><span class="sxs-lookup"><span data-stu-id="6490a-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6490a-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6490a-129">-FrontendPort</span></span>
<span data-ttu-id="6490a-130">Specifica la porta front-end a cui corrisponde una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6490a-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6490a-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6490a-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6490a-132">Specifica per l'intervallo di tempo, in minuti, che lo stato delle conversazioni viene mantenuto in una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6490a-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="6490a-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6490a-133">-LoadBalancer</span></span>
<span data-ttu-id="6490a-134">Specifica una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6490a-134">Specifies a load balancer.</span></span>
<span data-ttu-id="6490a-135">Questo cmdlet imposta una configurazione della regola NAT in ingresso per la bilanciamento del carico specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6490a-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="6490a-136">-Name</span><span class="sxs-lookup"><span data-stu-id="6490a-136">-Name</span></span>
<span data-ttu-id="6490a-137">Specifica il nome di una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="6490a-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="6490a-138">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6490a-138">-Protocol</span></span>
<span data-ttu-id="6490a-139">Specifica il protocollo a cui corrisponde una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="6490a-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="6490a-140">I valori accettabili per questo parametro sono: Tcp o Udp.</span><span class="sxs-lookup"><span data-stu-id="6490a-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="6490a-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6490a-141">-Confirm</span></span>
<span data-ttu-id="6490a-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6490a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6490a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6490a-143">-WhatIf</span></span>
<span data-ttu-id="6490a-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6490a-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6490a-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6490a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6490a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6490a-146">CommonParameters</span></span>
<span data-ttu-id="6490a-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6490a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6490a-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6490a-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6490a-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="6490a-149">INPUTS</span></span>

### <span data-ttu-id="6490a-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6490a-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="6490a-151">System.String</span><span class="sxs-lookup"><span data-stu-id="6490a-151">System.String</span></span>

### <span data-ttu-id="6490a-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6490a-152">System.Int32</span></span>

### <span data-ttu-id="6490a-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6490a-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="6490a-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6490a-154">OUTPUTS</span></span>

### <span data-ttu-id="6490a-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6490a-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6490a-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="6490a-156">NOTES</span></span>

## <span data-ttu-id="6490a-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6490a-157">RELATED LINKS</span></span>

[<span data-ttu-id="6490a-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6490a-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6490a-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6490a-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6490a-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6490a-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6490a-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6490a-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6490a-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6490a-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


