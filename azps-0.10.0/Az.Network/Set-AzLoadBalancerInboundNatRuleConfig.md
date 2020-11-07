---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: c8de559b6a2b6da9212cb6d9e2607392cf787bf4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862786"
---
# <span data-ttu-id="32272-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32272-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="32272-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32272-102">SYNOPSIS</span></span>
<span data-ttu-id="32272-103">Imposta una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="32272-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="32272-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32272-104">SYNTAX</span></span>

### <span data-ttu-id="32272-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="32272-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32272-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="32272-106">SetByResource</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32272-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32272-107">DESCRIPTION</span></span>
<span data-ttu-id="32272-108">Il cmdlet **set-AzLoadBalancerInboundNatRuleConfig** imposta una configurazione della regola NAT (Network Address Translation) in ingresso per un sistema di bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="32272-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="32272-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32272-109">EXAMPLES</span></span>

### <span data-ttu-id="32272-110">Esempio 1: modificare la configurazione della regola NAT in ingresso in un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="32272-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="32272-111">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="32272-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="32272-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a Add-AzLoadBalancerInboundNatRuleConfig, che aggiunge una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="32272-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="32272-113">Il terzo comando passa il bilanciamento del carico a **set-AzLoadBalancerInboundNatRuleConfig** , che salva e aggiorna la configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="32272-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="32272-114">Tieni presente che la configurazione della regola è stata impostata senza abilitare l'IP mobile, che era stato abilitato dal comando precedente.</span><span class="sxs-lookup"><span data-stu-id="32272-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="32272-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32272-115">PARAMETERS</span></span>

### <span data-ttu-id="32272-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="32272-116">-BackendPort</span></span>
<span data-ttu-id="32272-117">Specifica la porta di backend per il traffico che corrisponde alla configurazione della regola.</span><span class="sxs-lookup"><span data-stu-id="32272-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="32272-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32272-118">-DefaultProfile</span></span>
<span data-ttu-id="32272-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32272-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32272-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="32272-120">-EnableFloatingIP</span></span>
<span data-ttu-id="32272-121">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="32272-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="32272-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="32272-122">-FrontendIpConfiguration</span></span>
<span data-ttu-id="32272-123">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="32272-123">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="32272-124">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="32272-124">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="32272-125">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="32272-125">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="32272-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="32272-126">-FrontendPort</span></span>
<span data-ttu-id="32272-127">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="32272-127">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="32272-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="32272-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="32272-129">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="32272-129">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="32272-130">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="32272-130">-LoadBalancer</span></span>
<span data-ttu-id="32272-131">Specifica un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="32272-131">Specifies a load balancer.</span></span>
<span data-ttu-id="32272-132">Questo cmdlet imposta una configurazione della regola NAT in ingresso per il bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="32272-132">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="32272-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="32272-133">-Name</span></span>
<span data-ttu-id="32272-134">Specifica il nome di una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="32272-134">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="32272-135">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="32272-135">-Protocol</span></span>
<span data-ttu-id="32272-136">Specifica il protocollo corrispondente alla configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="32272-136">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="32272-137">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="32272-137">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32272-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32272-138">CommonParameters</span></span>
<span data-ttu-id="32272-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32272-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32272-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32272-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32272-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32272-141">INPUTS</span></span>

### <span data-ttu-id="32272-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="32272-142">PSLoadBalancer</span></span>
<span data-ttu-id="32272-143">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="32272-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="32272-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32272-144">OUTPUTS</span></span>

### <span data-ttu-id="32272-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="32272-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="32272-146">Note</span><span class="sxs-lookup"><span data-stu-id="32272-146">NOTES</span></span>

## <span data-ttu-id="32272-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32272-147">RELATED LINKS</span></span>

[<span data-ttu-id="32272-148">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32272-148">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="32272-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="32272-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="32272-150">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32272-150">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="32272-151">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32272-151">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="32272-152">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32272-152">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


