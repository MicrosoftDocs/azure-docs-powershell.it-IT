---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 1cfee59f1432cee5355ae562f8cc732a640d8c2b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678665"
---
# <span data-ttu-id="64bd1-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64bd1-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="64bd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="64bd1-103">Aggiunge una configurazione della regola NAT in ingresso a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="64bd1-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="64bd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64bd1-104">SYNTAX</span></span>

### <span data-ttu-id="64bd1-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64bd1-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64bd1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="64bd1-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64bd1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64bd1-107">DESCRIPTION</span></span>
<span data-ttu-id="64bd1-108">Il cmdlet **Add-AzLoadBalancerInboundNatRuleConfig** aggiunge una configurazione della regola NAT (Network Address Translation) in ingresso a un sistema di bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="64bd1-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="64bd1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64bd1-109">EXAMPLES</span></span>

### <span data-ttu-id="64bd1-110">Esempio 1: aggiungere una configurazione della regola NAT in ingresso a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="64bd1-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="64bd1-111">Il primo comando ottiene il bilanciamento del carico denominato MyloadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="64bd1-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="64bd1-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a **Add-AzLoadBalancerInboundNatRuleConfig** , che aggiunge una configurazione della regola NAT in ingresso al bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="64bd1-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="64bd1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64bd1-113">PARAMETERS</span></span>

### <span data-ttu-id="64bd1-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="64bd1-114">-BackendPort</span></span>
<span data-ttu-id="64bd1-115">Specifica la porta backend per il traffico corrispondente a una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="64bd1-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="64bd1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64bd1-116">-DefaultProfile</span></span>
<span data-ttu-id="64bd1-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64bd1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64bd1-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="64bd1-118">-EnableFloatingIP</span></span>
<span data-ttu-id="64bd1-119">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="64bd1-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="64bd1-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="64bd1-120">-EnableTcpReset</span></span>
<span data-ttu-id="64bd1-121">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="64bd1-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="64bd1-122">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="64bd1-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="64bd1-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="64bd1-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="64bd1-124">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="64bd1-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="64bd1-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="64bd1-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="64bd1-126">Specifica un ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="64bd1-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="64bd1-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="64bd1-127">-FrontendPort</span></span>
<span data-ttu-id="64bd1-128">Specifica la porta front-end corrispondente a una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="64bd1-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="64bd1-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="64bd1-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="64bd1-130">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="64bd1-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="64bd1-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="64bd1-131">-LoadBalancer</span></span>
<span data-ttu-id="64bd1-132">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="64bd1-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="64bd1-133">Questo cmdlet aggiunge una configurazione della regola NAT in ingresso al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="64bd1-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="64bd1-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="64bd1-134">-Name</span></span>
<span data-ttu-id="64bd1-135">Specifica il nome della configurazione della regola NAT in ingresso da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="64bd1-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="64bd1-136">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="64bd1-136">-Protocol</span></span>
<span data-ttu-id="64bd1-137">Specifica il protocollo corrispondente a una regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="64bd1-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="64bd1-138">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="64bd1-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="64bd1-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64bd1-139">-Confirm</span></span>
<span data-ttu-id="64bd1-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64bd1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64bd1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64bd1-141">-WhatIf</span></span>
<span data-ttu-id="64bd1-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64bd1-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64bd1-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64bd1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64bd1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bd1-144">CommonParameters</span></span>
<span data-ttu-id="64bd1-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64bd1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bd1-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64bd1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bd1-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64bd1-147">INPUTS</span></span>

### <span data-ttu-id="64bd1-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="64bd1-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="64bd1-149">System. String</span><span class="sxs-lookup"><span data-stu-id="64bd1-149">System.String</span></span>

### <span data-ttu-id="64bd1-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="64bd1-150">System.Int32</span></span>

### <span data-ttu-id="64bd1-151">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="64bd1-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="64bd1-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64bd1-152">OUTPUTS</span></span>

### <span data-ttu-id="64bd1-153">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="64bd1-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="64bd1-154">Note</span><span class="sxs-lookup"><span data-stu-id="64bd1-154">NOTES</span></span>

## <span data-ttu-id="64bd1-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64bd1-155">RELATED LINKS</span></span>

[<span data-ttu-id="64bd1-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="64bd1-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="64bd1-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64bd1-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="64bd1-158">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64bd1-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="64bd1-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64bd1-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="64bd1-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="64bd1-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="64bd1-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64bd1-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)

