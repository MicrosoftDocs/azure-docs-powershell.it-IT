---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: d59bb27608e1ccf614048dcd27eb6643695ba523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006493"
---
# <span data-ttu-id="05955-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05955-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="05955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05955-102">SYNOPSIS</span></span>
<span data-ttu-id="05955-103">Aggiunge una configurazione di regola in uscita a una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="05955-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="05955-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05955-104">SYNTAX</span></span>

### <span data-ttu-id="05955-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="05955-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05955-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="05955-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05955-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05955-107">DESCRIPTION</span></span>
<span data-ttu-id="05955-108">Il cmdlet **Add-AzLoadBalancerOutboundRuleConfig aggiunge** una configurazione della regola in uscita a una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="05955-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="05955-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05955-109">EXAMPLES</span></span>

### <span data-ttu-id="05955-110">Esempio 1: Aggiungere una configurazione di regola in uscita a un servizio di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="05955-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="05955-111">Il primo comando ottiene la bilanciamento del carico denominata MyLoadBalancer e quindi la archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="05955-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="05955-112">Il secondo comando usa l'operatore della pipeline per passare la bilanciamento del carico in $slb **ad Add-AzLoadBalancerOutboundRuleConfig,** che aggiunge una configurazione della regola in uscita al servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="05955-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig**, which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="05955-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05955-113">PARAMETERS</span></span>

### <span data-ttu-id="05955-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="05955-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="05955-115">Il numero di porte in uscita da usare per NAT.</span><span class="sxs-lookup"><span data-stu-id="05955-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="05955-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="05955-116">-BackendAddressPool</span></span>
<span data-ttu-id="05955-117">Riferimento a un pool di dip.</span><span class="sxs-lookup"><span data-stu-id="05955-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="05955-118">Il traffico in uscita è bilanciato in modo casuale tra gli IP negli IP back-end.</span><span class="sxs-lookup"><span data-stu-id="05955-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05955-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="05955-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="05955-120">Riferimento a un pool di dip.</span><span class="sxs-lookup"><span data-stu-id="05955-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="05955-121">Il traffico in uscita è bilanciato in modo casuale tra gli IP negli IP back-end.</span><span class="sxs-lookup"><span data-stu-id="05955-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05955-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05955-122">-DefaultProfile</span></span>
<span data-ttu-id="05955-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05955-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05955-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="05955-124">-EnableTcpReset</span></span>
<span data-ttu-id="05955-125">Ricevere la reimpostazione TCP bidirezionale in un timeout di inattività del flusso TCP o un'interruzione della connessione imprevista.</span><span class="sxs-lookup"><span data-stu-id="05955-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="05955-126">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="05955-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="05955-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="05955-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="05955-128">Indirizzi IP frontend del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="05955-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05955-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="05955-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="05955-130">Timeout della connessione TCP inattiva</span><span class="sxs-lookup"><span data-stu-id="05955-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="05955-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="05955-131">-LoadBalancer</span></span>
<span data-ttu-id="05955-132">Riferimento alla risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="05955-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="05955-133">-Name</span><span class="sxs-lookup"><span data-stu-id="05955-133">-Name</span></span>
<span data-ttu-id="05955-134">Nome della regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="05955-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="05955-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="05955-135">-Protocol</span></span>
<span data-ttu-id="05955-136">Protocollo: TCP, UDP o All</span><span class="sxs-lookup"><span data-stu-id="05955-136">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05955-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05955-137">-Confirm</span></span>
<span data-ttu-id="05955-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05955-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05955-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05955-139">-WhatIf</span></span>
<span data-ttu-id="05955-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05955-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05955-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05955-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05955-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05955-142">CommonParameters</span></span>
<span data-ttu-id="05955-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05955-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05955-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05955-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05955-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="05955-145">INPUTS</span></span>

### <span data-ttu-id="05955-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="05955-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="05955-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="05955-147">System.Int32</span></span>

### <span data-ttu-id="05955-148">System.String</span><span class="sxs-lookup"><span data-stu-id="05955-148">System.String</span></span>

### <span data-ttu-id="05955-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="05955-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="05955-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="05955-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="05955-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05955-151">OUTPUTS</span></span>

### <span data-ttu-id="05955-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="05955-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="05955-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="05955-153">NOTES</span></span>

## <span data-ttu-id="05955-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05955-154">RELATED LINKS</span></span>

[<span data-ttu-id="05955-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05955-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="05955-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05955-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="05955-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05955-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="05955-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05955-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
