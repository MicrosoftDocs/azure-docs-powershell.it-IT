---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: f566c2b9ac771071a9eb72673edb7e5218656c9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862773"
---
# <span data-ttu-id="beeff-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="beeff-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="beeff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="beeff-102">SYNOPSIS</span></span>
<span data-ttu-id="beeff-103">Imposta lo stato dell'obiettivo per una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-103">Sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="beeff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="beeff-104">SYNTAX</span></span>

### <span data-ttu-id="beeff-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="beeff-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="beeff-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="beeff-106">SetByResource</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beeff-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="beeff-107">DESCRIPTION</span></span>
<span data-ttu-id="beeff-108">Il cmdlet **set-AzLoadBalancerRuleConfig** imposta lo stato dell'obiettivo per una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-108">The **Set-AzLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="beeff-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="beeff-109">EXAMPLES</span></span>

### <span data-ttu-id="beeff-110">Esempio 1: modificare una configurazione della regola di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="beeff-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="beeff-111">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="beeff-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="beeff-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerRuleConfig, che aggiunge una regola denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="beeff-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="beeff-113">Il terzo comando passa il bilanciamento del carico a **set-AzLoadBalancerRuleConfig** , che imposta la nuova configurazione della regola.</span><span class="sxs-lookup"><span data-stu-id="beeff-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="beeff-114">Tieni presente che la configurazione non Abilita un indirizzo IP mobile, che era stato abilitato dal comando precedente.</span><span class="sxs-lookup"><span data-stu-id="beeff-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="beeff-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="beeff-115">PARAMETERS</span></span>

### <span data-ttu-id="beeff-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="beeff-116">-BackendAddressPool</span></span>
<span data-ttu-id="beeff-117">Specifica un oggetto **BackendAddressPool** da associare a una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="beeff-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="beeff-119">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="beeff-120">-BackendPort</span></span>
<span data-ttu-id="beeff-121">Specifica la porta di backend per il traffico che corrisponde alla configurazione della regola.</span><span class="sxs-lookup"><span data-stu-id="beeff-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beeff-122">-DefaultProfile</span></span>
<span data-ttu-id="beeff-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="beeff-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="beeff-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="beeff-125">Configura SNAT per le VM nel pool back-end per usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="beeff-126">-EnableFloatingIP</span></span>
<span data-ttu-id="beeff-127">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="beeff-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="beeff-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="beeff-129">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-130">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="beeff-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="beeff-131">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="beeff-131">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-132">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="beeff-132">-FrontendPort</span></span>
<span data-ttu-id="beeff-133">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="beeff-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="beeff-135">Specifica il periodo di tempo, in minuti, per il quale lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-136">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="beeff-136">-LoadBalancer</span></span>
<span data-ttu-id="beeff-137">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-137">Specifies a load balancer.</span></span>
<span data-ttu-id="beeff-138">Questo cmdlet imposta la configurazione della regola dello stato dell'obiettivo per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="beeff-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-139">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="beeff-139">-LoadDistribution</span></span>
<span data-ttu-id="beeff-140">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-140">Specifies a load distribution.</span></span>
<span data-ttu-id="beeff-141">I valori accettabili per questo parametro sono: SourceIP e SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="beeff-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="beeff-142">-Name</span></span>
<span data-ttu-id="beeff-143">Specifica il nome di un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-143">Specifies the name of a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-144">-Probe</span><span class="sxs-lookup"><span data-stu-id="beeff-144">-Probe</span></span>
<span data-ttu-id="beeff-145">Specifica una sonda da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="beeff-146">-ProbeId</span></span>
<span data-ttu-id="beeff-147">Specifica l'ID del Probe da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-148">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="beeff-148">-Protocol</span></span>
<span data-ttu-id="beeff-149">Specifica il protocollo corrispondente a una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="beeff-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="beeff-150">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="beeff-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beeff-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beeff-151">CommonParameters</span></span>
<span data-ttu-id="beeff-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beeff-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beeff-153">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beeff-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beeff-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="beeff-154">INPUTS</span></span>

### <span data-ttu-id="beeff-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="beeff-155">PSLoadBalancer</span></span>
<span data-ttu-id="beeff-156">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="beeff-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="beeff-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="beeff-157">OUTPUTS</span></span>

### <span data-ttu-id="beeff-158">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="beeff-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="beeff-159">Note</span><span class="sxs-lookup"><span data-stu-id="beeff-159">NOTES</span></span>

## <span data-ttu-id="beeff-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="beeff-160">RELATED LINKS</span></span>

[<span data-ttu-id="beeff-161">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="beeff-161">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="beeff-162">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="beeff-162">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="beeff-163">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="beeff-163">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="beeff-164">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="beeff-164">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="beeff-165">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="beeff-165">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


