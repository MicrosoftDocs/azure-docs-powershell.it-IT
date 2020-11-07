---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6a699907b70256995973bfdbde4e11b08c594669
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860977"
---
# <span data-ttu-id="7cf63-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cf63-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="7cf63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cf63-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf63-103">Aggiunge una configurazione della regola NAT in ingresso a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7cf63-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="7cf63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cf63-104">SYNTAX</span></span>

### <span data-ttu-id="7cf63-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf63-105">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7cf63-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7cf63-106">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cf63-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cf63-107">DESCRIPTION</span></span>
<span data-ttu-id="7cf63-108">Il cmdlet **Add-AzLoadBalancerInboundNatRuleConfig** aggiunge una configurazione della regola NAT (Network Address Translation) in ingresso a un sistema di bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf63-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="7cf63-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cf63-109">EXAMPLES</span></span>

### <span data-ttu-id="7cf63-110">Esempio 1: aggiungere una configurazione della regola NAT in ingresso a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="7cf63-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="7cf63-111">Il primo comando ottiene il bilanciamento del carico denominato MyloadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="7cf63-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="7cf63-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a **Add-AzLoadBalancerInboundNatRuleConfig** , che aggiunge una configurazione della regola NAT in ingresso al bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7cf63-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="7cf63-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cf63-113">PARAMETERS</span></span>

### <span data-ttu-id="7cf63-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7cf63-114">-BackendPort</span></span>
<span data-ttu-id="7cf63-115">Specifica la porta backend per il traffico corrispondente a una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="7cf63-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="7cf63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf63-116">-DefaultProfile</span></span>
<span data-ttu-id="7cf63-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf63-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cf63-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="7cf63-118">-EnableFloatingIP</span></span>
<span data-ttu-id="7cf63-119">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="7cf63-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="7cf63-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cf63-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="7cf63-121">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="7cf63-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="7cf63-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7cf63-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="7cf63-123">Specifica un ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="7cf63-123">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="7cf63-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7cf63-124">-FrontendPort</span></span>
<span data-ttu-id="7cf63-125">Specifica la porta front-end corrispondente a una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="7cf63-125">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="7cf63-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7cf63-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7cf63-127">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7cf63-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="7cf63-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7cf63-128">-LoadBalancer</span></span>
<span data-ttu-id="7cf63-129">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="7cf63-129">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="7cf63-130">Questo cmdlet aggiunge una configurazione della regola NAT in ingresso al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7cf63-130">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="7cf63-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cf63-131">-Name</span></span>
<span data-ttu-id="7cf63-132">Specifica il nome della configurazione della regola NAT in ingresso da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="7cf63-132">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="7cf63-133">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="7cf63-133">-Protocol</span></span>
<span data-ttu-id="7cf63-134">Specifica il protocollo corrispondente a una regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="7cf63-134">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="7cf63-135">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="7cf63-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="7cf63-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf63-136">CommonParameters</span></span>
<span data-ttu-id="7cf63-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf63-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf63-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf63-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf63-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cf63-139">INPUTS</span></span>

### <span data-ttu-id="7cf63-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7cf63-140">PSLoadBalancer</span></span>
<span data-ttu-id="7cf63-141">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7cf63-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7cf63-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cf63-142">OUTPUTS</span></span>

### <span data-ttu-id="7cf63-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7cf63-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7cf63-144">Note</span><span class="sxs-lookup"><span data-stu-id="7cf63-144">NOTES</span></span>

## <span data-ttu-id="7cf63-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cf63-145">RELATED LINKS</span></span>

[<span data-ttu-id="7cf63-146">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7cf63-146">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7cf63-147">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cf63-147">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7cf63-148">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cf63-148">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7cf63-149">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cf63-149">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7cf63-150">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7cf63-150">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="7cf63-151">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cf63-151">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


