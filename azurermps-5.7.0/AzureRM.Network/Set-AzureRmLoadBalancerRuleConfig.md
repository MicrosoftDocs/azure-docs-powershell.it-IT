---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: acc741bc038e7fe3a9612e2bc6b4e9abe6bab800
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518871"
---
# <span data-ttu-id="6d4d6-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d4d6-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="6d4d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="6d4d6-103">Imposta lo stato dell'obiettivo per una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d4d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d4d6-104">SYNTAX</span></span>

### <span data-ttu-id="6d4d6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6d4d6-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d4d6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6d4d6-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d4d6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d4d6-107">DESCRIPTION</span></span>
<span data-ttu-id="6d4d6-108">Il cmdlet **set-AzureRmLoadBalancerRuleConfig** imposta lo stato dell'obiettivo per una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="6d4d6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d4d6-109">EXAMPLES</span></span>

### <span data-ttu-id="6d4d6-110">Esempio 1: modificare una configurazione della regola di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="6d4d6-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="6d4d6-111">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="6d4d6-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzureRmLoadBalancerRuleConfig, che aggiunge una regola denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="6d4d6-113">Il terzo comando passa il bilanciamento del carico a **set-AzureRmLoadBalancerRuleConfig** , che imposta la nuova configurazione della regola.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="6d4d6-114">Tieni presente che la configurazione non Abilita un indirizzo IP mobile, che era stato abilitato dal comando precedente.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="6d4d6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d4d6-115">PARAMETERS</span></span>

### <span data-ttu-id="6d4d6-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6d4d6-116">-BackendAddressPool</span></span>
<span data-ttu-id="6d4d6-117">Specifica un oggetto **BackendAddressPool** da associare a una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="6d4d6-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6d4d6-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="6d4d6-119">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6d4d6-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="6d4d6-120">-BackendPort</span></span>
<span data-ttu-id="6d4d6-121">Specifica la porta di backend per il traffico che corrisponde alla configurazione della regola.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="6d4d6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d4d6-122">-DefaultProfile</span></span>
<span data-ttu-id="6d4d6-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d4d6-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="6d4d6-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="6d4d6-125">Configura SNAT per le VM nel pool back-end per usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="6d4d6-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="6d4d6-126">-EnableFloatingIP</span></span>
<span data-ttu-id="6d4d6-127">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6d4d6-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d4d6-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6d4d6-129">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6d4d6-130">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6d4d6-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6d4d6-131">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-131">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6d4d6-132">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6d4d6-132">-FrontendPort</span></span>
<span data-ttu-id="6d4d6-133">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6d4d6-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6d4d6-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6d4d6-135">Specifica il periodo di tempo, in minuti, per il quale lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="6d4d6-136">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d4d6-136">-LoadBalancer</span></span>
<span data-ttu-id="6d4d6-137">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-137">Specifies a load balancer.</span></span>
<span data-ttu-id="6d4d6-138">Questo cmdlet imposta la configurazione della regola dello stato dell'obiettivo per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="6d4d6-139">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="6d4d6-139">-LoadDistribution</span></span>
<span data-ttu-id="6d4d6-140">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-140">Specifies a load distribution.</span></span>
<span data-ttu-id="6d4d6-141">I valori accettabili per questo parametro sono: SourceIP e SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="6d4d6-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d4d6-142">-Name</span></span>
<span data-ttu-id="6d4d6-143">Specifica il nome di un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-143">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="6d4d6-144">-Probe</span><span class="sxs-lookup"><span data-stu-id="6d4d6-144">-Probe</span></span>
<span data-ttu-id="6d4d6-145">Specifica una sonda da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6d4d6-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="6d4d6-146">-ProbeId</span></span>
<span data-ttu-id="6d4d6-147">Specifica l'ID del Probe da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6d4d6-148">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="6d4d6-148">-Protocol</span></span>
<span data-ttu-id="6d4d6-149">Specifica il protocollo corrispondente a una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="6d4d6-150">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="6d4d6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d4d6-151">CommonParameters</span></span>
<span data-ttu-id="6d4d6-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d4d6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d4d6-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d4d6-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d4d6-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d4d6-154">INPUTS</span></span>

### <span data-ttu-id="6d4d6-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d4d6-155">PSLoadBalancer</span></span>
<span data-ttu-id="6d4d6-156">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6d4d6-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="6d4d6-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d4d6-157">OUTPUTS</span></span>

### <span data-ttu-id="6d4d6-158">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d4d6-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6d4d6-159">Note</span><span class="sxs-lookup"><span data-stu-id="6d4d6-159">NOTES</span></span>

## <span data-ttu-id="6d4d6-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d4d6-160">RELATED LINKS</span></span>

[<span data-ttu-id="6d4d6-161">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d4d6-161">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6d4d6-162">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d4d6-162">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6d4d6-163">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d4d6-163">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6d4d6-164">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d4d6-164">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6d4d6-165">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d4d6-165">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

