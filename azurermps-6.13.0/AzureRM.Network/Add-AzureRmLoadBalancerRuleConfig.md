---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ed21aec1be522ac145fe255065b650ca4c09dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688409"
---
# <span data-ttu-id="bbc7b-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbc7b-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="bbc7b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbc7b-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc7b-103">Aggiunge una configurazione di regola a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbc7b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbc7b-104">SYNTAX</span></span>

### <span data-ttu-id="bbc7b-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bbc7b-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc7b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bbc7b-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbc7b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbc7b-107">DESCRIPTION</span></span>
<span data-ttu-id="bbc7b-108">Il cmdlet **Add-AzureRmLoadBalancerRuleConfig** aggiunge una configurazione di regola a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="bbc7b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbc7b-109">EXAMPLES</span></span>

### <span data-ttu-id="bbc7b-110">Esempio 1: aggiungere una configurazione di regola a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="bbc7b-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="bbc7b-111">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="bbc7b-112">Il secondo comando usa l'operatore pipeline per passare il bilanciamento del carico in $slb a **Add-AzureRmLoadBalancerRuleConfig** , che aggiunge la configurazione della regola denominata NewRule.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="bbc7b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbc7b-113">PARAMETERS</span></span>

### <span data-ttu-id="bbc7b-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bbc7b-114">-BackendAddressPool</span></span>
<span data-ttu-id="bbc7b-115">Specifica il pool di indirizzi di backend da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc7b-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bbc7b-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="bbc7b-117">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbc7b-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="bbc7b-118">-BackendPort</span></span>
<span data-ttu-id="bbc7b-119">Specifica la porta di backend per il traffico che corrisponde a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbc7b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc7b-120">-DefaultProfile</span></span>
<span data-ttu-id="bbc7b-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc7b-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="bbc7b-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="bbc7b-123">Configura SNAT per le VM nel pool back-end per usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="bbc7b-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="bbc7b-124">-EnableFloatingIP</span></span>
<span data-ttu-id="bbc7b-125">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="bbc7b-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="bbc7b-126">-EnableTcpReset</span></span>
<span data-ttu-id="bbc7b-127">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="bbc7b-128">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="bbc7b-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbc7b-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="bbc7b-130">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbc7b-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bbc7b-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="bbc7b-132">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="bbc7b-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="bbc7b-133">-FrontendPort</span></span>
<span data-ttu-id="bbc7b-134">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbc7b-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="bbc7b-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="bbc7b-136">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto nel bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-136">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="bbc7b-137">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbc7b-137">-LoadBalancer</span></span>
<span data-ttu-id="bbc7b-138">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="bbc7b-138">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="bbc7b-139">Questo cmdlet aggiunge una configurazione di regola al bilanciamento del carico specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-139">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="bbc7b-140">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="bbc7b-140">-LoadDistribution</span></span>
<span data-ttu-id="bbc7b-141">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-141">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="bbc7b-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbc7b-142">-Name</span></span>
<span data-ttu-id="bbc7b-143">Specifica il nome della configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-143">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbc7b-144">-Probe</span><span class="sxs-lookup"><span data-stu-id="bbc7b-144">-Probe</span></span>
<span data-ttu-id="bbc7b-145">Specifica una sonda da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc7b-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="bbc7b-146">-ProbeId</span></span>
<span data-ttu-id="bbc7b-147">Specifica l'ID del Probe da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bbc7b-148">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="bbc7b-148">-Protocol</span></span>
<span data-ttu-id="bbc7b-149">Specifica il protocollo che corrisponde a una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-149">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="bbc7b-150">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="bbc7b-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bbc7b-151">-Confirm</span></span>
<span data-ttu-id="bbc7b-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbc7b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc7b-153">-WhatIf</span></span>
<span data-ttu-id="bbc7b-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bbc7b-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbc7b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc7b-156">CommonParameters</span></span>
<span data-ttu-id="bbc7b-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbc7b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc7b-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbc7b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc7b-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbc7b-159">INPUTS</span></span>

### <span data-ttu-id="bbc7b-160">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbc7b-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="bbc7b-161">Parametri: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bbc7b-161">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="bbc7b-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbc7b-162">OUTPUTS</span></span>

### <span data-ttu-id="bbc7b-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbc7b-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bbc7b-164">Note</span><span class="sxs-lookup"><span data-stu-id="bbc7b-164">NOTES</span></span>

## <span data-ttu-id="bbc7b-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbc7b-165">RELATED LINKS</span></span>

[<span data-ttu-id="bbc7b-166">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbc7b-166">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="bbc7b-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbc7b-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="bbc7b-168">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbc7b-168">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="bbc7b-169">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbc7b-169">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="bbc7b-170">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbc7b-170">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


