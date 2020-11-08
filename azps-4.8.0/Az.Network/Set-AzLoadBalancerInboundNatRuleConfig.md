---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 68b3043b67580dcc781badb7c1891444e97e281f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192279"
---
# <span data-ttu-id="ff720-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff720-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="ff720-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff720-102">SYNOPSIS</span></span>
<span data-ttu-id="ff720-103">Imposta una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="ff720-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="ff720-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff720-104">SYNTAX</span></span>

### <span data-ttu-id="ff720-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff720-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff720-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ff720-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff720-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff720-107">DESCRIPTION</span></span>
<span data-ttu-id="ff720-108">Il cmdlet **set-AzLoadBalancerInboundNatRuleConfig** imposta una configurazione della regola NAT (Network Address Translation) in ingresso per un sistema di bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff720-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ff720-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff720-109">EXAMPLES</span></span>

### <span data-ttu-id="ff720-110">Esempio 1: modificare la configurazione della regola NAT in ingresso in un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="ff720-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="ff720-111">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="ff720-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="ff720-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerInboundNatRuleConfig, che aggiunge una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="ff720-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="ff720-113">Il terzo comando passa il bilanciamento del carico a **set-AzLoadBalancerInboundNatRuleConfig** , che salva e aggiorna la configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="ff720-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="ff720-114">Tieni presente che la configurazione della regola è stata impostata senza abilitare l'IP mobile, che era stato abilitato dal comando precedente.</span><span class="sxs-lookup"><span data-stu-id="ff720-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="ff720-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff720-115">PARAMETERS</span></span>

### <span data-ttu-id="ff720-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ff720-116">-BackendPort</span></span>
<span data-ttu-id="ff720-117">Specifica la porta di backend per il traffico che corrisponde alla configurazione della regola.</span><span class="sxs-lookup"><span data-stu-id="ff720-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="ff720-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff720-118">-DefaultProfile</span></span>
<span data-ttu-id="ff720-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff720-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff720-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="ff720-120">-EnableFloatingIP</span></span>
<span data-ttu-id="ff720-121">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="ff720-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="ff720-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ff720-122">-EnableTcpReset</span></span>
<span data-ttu-id="ff720-123">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="ff720-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="ff720-124">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="ff720-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ff720-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff720-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ff720-126">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="ff720-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="ff720-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ff720-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="ff720-128">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="ff720-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="ff720-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ff720-129">-FrontendPort</span></span>
<span data-ttu-id="ff720-130">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="ff720-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ff720-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ff720-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ff720-132">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="ff720-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="ff720-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ff720-133">-LoadBalancer</span></span>
<span data-ttu-id="ff720-134">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="ff720-134">Specifies a load balancer.</span></span>
<span data-ttu-id="ff720-135">Questo cmdlet imposta una configurazione della regola NAT in ingresso per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ff720-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff720-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff720-136">-Name</span></span>
<span data-ttu-id="ff720-137">Specifica il nome di una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="ff720-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="ff720-138">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="ff720-138">-Protocol</span></span>
<span data-ttu-id="ff720-139">Specifica il protocollo corrispondente alla configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="ff720-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="ff720-140">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="ff720-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="ff720-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ff720-141">-Confirm</span></span>
<span data-ttu-id="ff720-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff720-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff720-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff720-143">-WhatIf</span></span>
<span data-ttu-id="ff720-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff720-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff720-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff720-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff720-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff720-146">CommonParameters</span></span>
<span data-ttu-id="ff720-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff720-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff720-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff720-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff720-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff720-149">INPUTS</span></span>

### <span data-ttu-id="ff720-150">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ff720-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="ff720-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ff720-151">System.String</span></span>

### <span data-ttu-id="ff720-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ff720-152">System.Int32</span></span>

### <span data-ttu-id="ff720-153">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff720-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ff720-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff720-154">OUTPUTS</span></span>

### <span data-ttu-id="ff720-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ff720-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ff720-156">Note</span><span class="sxs-lookup"><span data-stu-id="ff720-156">NOTES</span></span>

## <span data-ttu-id="ff720-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff720-157">RELATED LINKS</span></span>

[<span data-ttu-id="ff720-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff720-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ff720-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ff720-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ff720-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff720-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ff720-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff720-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ff720-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff720-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

