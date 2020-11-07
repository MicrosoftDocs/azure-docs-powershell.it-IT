---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 8e055df66c0623fbddbed8379cb25f165efb7081
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686497"
---
# <span data-ttu-id="0431d-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0431d-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="0431d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0431d-102">SYNOPSIS</span></span>
<span data-ttu-id="0431d-103">Aggiunge una configurazione della regola NAT in ingresso a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="0431d-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0431d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0431d-104">SYNTAX</span></span>

### <span data-ttu-id="0431d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0431d-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0431d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0431d-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0431d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0431d-107">DESCRIPTION</span></span>
<span data-ttu-id="0431d-108">Il cmdlet **Add-AzureRmLoadBalancerInboundNatRuleConfig** aggiunge una configurazione della regola NAT (Network Address Translation) in ingresso a un sistema di bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="0431d-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="0431d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0431d-109">EXAMPLES</span></span>

### <span data-ttu-id="0431d-110">Esempio 1: aggiungere una configurazione della regola NAT in ingresso a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="0431d-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="0431d-111">Il primo comando ottiene il bilanciamento del carico denominato MyloadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="0431d-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="0431d-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a **Add-AzureRmLoadBalancerInboundNatRuleConfig** , che aggiunge una configurazione della regola NAT in ingresso al bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="0431d-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="0431d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0431d-113">PARAMETERS</span></span>

### <span data-ttu-id="0431d-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="0431d-114">-BackendPort</span></span>
<span data-ttu-id="0431d-115">Specifica la porta backend per il traffico corrispondente a una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="0431d-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="0431d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0431d-116">-DefaultProfile</span></span>
<span data-ttu-id="0431d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0431d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0431d-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="0431d-118">-EnableFloatingIP</span></span>
<span data-ttu-id="0431d-119">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="0431d-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="0431d-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0431d-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="0431d-121">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="0431d-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="0431d-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0431d-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="0431d-123">Specifica un ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="0431d-123">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="0431d-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="0431d-124">-FrontendPort</span></span>
<span data-ttu-id="0431d-125">Specifica la porta front-end corrispondente a una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="0431d-125">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="0431d-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0431d-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0431d-127">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="0431d-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="0431d-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0431d-128">-LoadBalancer</span></span>
<span data-ttu-id="0431d-129">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="0431d-129">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="0431d-130">Questo cmdlet aggiunge una configurazione della regola NAT in ingresso al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0431d-130">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="0431d-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="0431d-131">-Name</span></span>
<span data-ttu-id="0431d-132">Specifica il nome della configurazione della regola NAT in ingresso da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="0431d-132">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="0431d-133">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="0431d-133">-Protocol</span></span>
<span data-ttu-id="0431d-134">Specifica il protocollo corrispondente a una regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="0431d-134">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="0431d-135">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="0431d-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="0431d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0431d-136">CommonParameters</span></span>
<span data-ttu-id="0431d-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0431d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0431d-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0431d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0431d-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0431d-139">INPUTS</span></span>

### <span data-ttu-id="0431d-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0431d-140">PSLoadBalancer</span></span>
<span data-ttu-id="0431d-141">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0431d-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0431d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0431d-142">OUTPUTS</span></span>

### <span data-ttu-id="0431d-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0431d-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0431d-144">Note</span><span class="sxs-lookup"><span data-stu-id="0431d-144">NOTES</span></span>

## <span data-ttu-id="0431d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0431d-145">RELATED LINKS</span></span>

[<span data-ttu-id="0431d-146">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0431d-146">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="0431d-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0431d-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0431d-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0431d-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0431d-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0431d-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0431d-150">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0431d-150">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="0431d-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0431d-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


