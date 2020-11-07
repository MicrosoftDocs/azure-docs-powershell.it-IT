---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: 0708540cbb0ccac2f445fc0692c3c91f9358213c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866670"
---
# <span data-ttu-id="e2085-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2085-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="e2085-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2085-102">SYNOPSIS</span></span>
<span data-ttu-id="e2085-103">Aggiunge una configurazione di regola a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2085-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2085-104">SYNTAX</span></span>

### <span data-ttu-id="e2085-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2085-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2085-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e2085-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2085-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2085-107">DESCRIPTION</span></span>
<span data-ttu-id="e2085-108">Il cmdlet **Add-AzureRmLoadBalancerRuleConfig** aggiunge una configurazione di regola a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="e2085-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="e2085-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2085-109">EXAMPLES</span></span>

### <span data-ttu-id="e2085-110">Esempio 1: aggiungere una configurazione di regola a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="e2085-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="e2085-111">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="e2085-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="e2085-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a **Add-AzureRmLoadBalancerRuleConfig** , che aggiunge la configurazione della regola denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="e2085-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="e2085-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2085-113">PARAMETERS</span></span>

### <span data-ttu-id="e2085-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2085-114">-BackendAddressPool</span></span>
<span data-ttu-id="e2085-115">Specifica il pool di indirizzi di backend da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e2085-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e2085-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="e2085-117">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e2085-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="e2085-118">-BackendPort</span></span>
<span data-ttu-id="e2085-119">Specifica la porta di backend per il traffico che corrisponde a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e2085-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2085-120">-DefaultProfile</span></span>
<span data-ttu-id="e2085-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2085-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2085-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="e2085-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="e2085-123">Configura SNAT per le VM nel pool back-end per usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="e2085-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="e2085-124">-EnableFloatingIP</span></span>
<span data-ttu-id="e2085-125">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="e2085-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="e2085-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2085-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e2085-127">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e2085-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e2085-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="e2085-129">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="e2085-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="e2085-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="e2085-130">-FrontendPort</span></span>
<span data-ttu-id="e2085-131">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e2085-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e2085-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e2085-133">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto nel bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="e2085-134">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2085-134">-LoadBalancer</span></span>
<span data-ttu-id="e2085-135">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="e2085-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="e2085-136">Questo cmdlet aggiunge una configurazione di regola al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e2085-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="e2085-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="e2085-137">-LoadDistribution</span></span>
<span data-ttu-id="e2085-138">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-138">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="e2085-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2085-139">-Name</span></span>
<span data-ttu-id="e2085-140">Specifica il nome della configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-140">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e2085-141">-Probe</span><span class="sxs-lookup"><span data-stu-id="e2085-141">-Probe</span></span>
<span data-ttu-id="e2085-142">Specifica una sonda da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e2085-143">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="e2085-143">-ProbeId</span></span>
<span data-ttu-id="e2085-144">Specifica l'ID del Probe da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e2085-145">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="e2085-145">-Protocol</span></span>
<span data-ttu-id="e2085-146">Specifica il protocollo che corrisponde a una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e2085-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="e2085-147">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="e2085-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="e2085-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2085-148">CommonParameters</span></span>
<span data-ttu-id="e2085-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2085-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2085-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2085-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2085-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2085-151">INPUTS</span></span>

### <span data-ttu-id="e2085-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2085-152">PSLoadBalancer</span></span>
<span data-ttu-id="e2085-153">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e2085-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e2085-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2085-154">OUTPUTS</span></span>

### <span data-ttu-id="e2085-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2085-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e2085-156">Note</span><span class="sxs-lookup"><span data-stu-id="e2085-156">NOTES</span></span>

## <span data-ttu-id="e2085-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2085-157">RELATED LINKS</span></span>

[<span data-ttu-id="e2085-158">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2085-158">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="e2085-159">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2085-159">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e2085-160">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2085-160">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e2085-161">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2085-161">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e2085-162">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2085-162">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


