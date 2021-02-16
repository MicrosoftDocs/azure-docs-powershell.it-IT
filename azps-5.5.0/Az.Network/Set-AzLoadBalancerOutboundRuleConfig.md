---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 82e61d3c4a387630dec2c829d651f8d9746a3419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179327"
---
# <span data-ttu-id="316be-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="316be-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="316be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="316be-102">SYNOPSIS</span></span>
<span data-ttu-id="316be-103">Imposta una configurazione della regola in uscita per una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="316be-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="316be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="316be-104">SYNTAX</span></span>

### <span data-ttu-id="316be-105">SetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="316be-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="316be-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="316be-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="316be-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="316be-107">DESCRIPTION</span></span>
<span data-ttu-id="316be-108">Il cmdlet **Set-AzLoadBalancerOutboundRuleConfig imposta** una configurazione della regola in uscita per una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="316be-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="316be-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="316be-109">EXAMPLES</span></span>

### <span data-ttu-id="316be-110">Esempio 1: Modificare la configurazione della regola in uscita in un servizio di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="316be-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="316be-111">Il primo comando recupera la bilanciamento del carico denominata MyLoadBalancer e quindi la archivia nella $slb variabile.</span><span class="sxs-lookup"><span data-stu-id="316be-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="316be-112">Il secondo comando usa l'operatore della pipeline per passare la bilanciamento del carico in $slb ad Add-AzLoadBalancerOutboundRuleConfig, che aggiunge una configurazione della regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="316be-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="316be-113">Il terzo comando passa la bilanciamento del carico **a Set-AzLoadBalancerOutboundRuleConfig,** che salva e aggiorna la configurazione della regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="316be-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig**, which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="316be-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="316be-114">PARAMETERS</span></span>

### <span data-ttu-id="316be-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="316be-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="316be-116">Il numero di porte in uscita da usare per NAT.</span><span class="sxs-lookup"><span data-stu-id="316be-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="316be-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="316be-117">-BackendAddressPool</span></span>
<span data-ttu-id="316be-118">Riferimento a un pool di dip.</span><span class="sxs-lookup"><span data-stu-id="316be-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="316be-119">Il traffico in uscita è bilanciato in modo casuale tra gli IP negli IP back-end.</span><span class="sxs-lookup"><span data-stu-id="316be-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="316be-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="316be-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="316be-121">Riferimento a un pool di dip.</span><span class="sxs-lookup"><span data-stu-id="316be-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="316be-122">Il traffico in uscita è bilanciato in modo casuale tra gli IP negli IP back-end.</span><span class="sxs-lookup"><span data-stu-id="316be-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="316be-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316be-123">-DefaultProfile</span></span>
<span data-ttu-id="316be-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="316be-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="316be-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="316be-125">-EnableTcpReset</span></span>
<span data-ttu-id="316be-126">Ricevere la reimpostazione TCP bidirezionale in un timeout di inattività del flusso TCP o un'interruzione della connessione imprevista.</span><span class="sxs-lookup"><span data-stu-id="316be-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="316be-127">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="316be-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="316be-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="316be-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="316be-129">Indirizzi IP frontend della bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="316be-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="316be-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="316be-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="316be-131">Timeout della connessione TCP inattiva</span><span class="sxs-lookup"><span data-stu-id="316be-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="316be-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="316be-132">-LoadBalancer</span></span>
<span data-ttu-id="316be-133">Riferimento alla risorsa di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="316be-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="316be-134">-Name</span><span class="sxs-lookup"><span data-stu-id="316be-134">-Name</span></span>
<span data-ttu-id="316be-135">Nome della regola in uscita.</span><span class="sxs-lookup"><span data-stu-id="316be-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="316be-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="316be-136">-Protocol</span></span>
<span data-ttu-id="316be-137">Protocol - TCP, UDP o All</span><span class="sxs-lookup"><span data-stu-id="316be-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="316be-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="316be-138">-Confirm</span></span>
<span data-ttu-id="316be-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="316be-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="316be-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="316be-140">-WhatIf</span></span>
<span data-ttu-id="316be-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="316be-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="316be-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="316be-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="316be-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316be-143">CommonParameters</span></span>
<span data-ttu-id="316be-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="316be-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316be-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="316be-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316be-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="316be-146">INPUTS</span></span>

### <span data-ttu-id="316be-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="316be-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="316be-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="316be-148">System.Int32</span></span>

### <span data-ttu-id="316be-149">System.String</span><span class="sxs-lookup"><span data-stu-id="316be-149">System.String</span></span>

### <span data-ttu-id="316be-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="316be-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="316be-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="316be-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="316be-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="316be-152">OUTPUTS</span></span>

### <span data-ttu-id="316be-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="316be-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="316be-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="316be-154">NOTES</span></span>

## <span data-ttu-id="316be-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="316be-155">RELATED LINKS</span></span>

[<span data-ttu-id="316be-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="316be-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="316be-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="316be-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="316be-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="316be-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="316be-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="316be-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
