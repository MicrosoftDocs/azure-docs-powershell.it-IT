---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9fef4a3cfe57b75ad992d4f4068bb0d51bbdcd90
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192851"
---
# <span data-ttu-id="b6b90-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6b90-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="b6b90-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6b90-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b90-103">Aggiunge una configurazione IP di interfaccia di rete a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="b6b90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6b90-104">SYNTAX</span></span>

### <span data-ttu-id="b6b90-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6b90-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6b90-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b90-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6b90-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6b90-107">DESCRIPTION</span></span>
<span data-ttu-id="b6b90-108">Il cmdlet **Add-AzNetworkInterfaceIpConfig** aggiunge una configurazione IP di interfaccia di rete a un'interfaccia di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b90-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="b6b90-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6b90-109">EXAMPLES</span></span>

### <span data-ttu-id="b6b90-110">Esempio 1: aggiungere una nuova configurazione IP con un gruppo di sicurezza dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b6b90-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="b6b90-111">In questo esempio creiamo una nuova interfaccia di rete MyNetworkInterface che appartiene a una subnet nella nuova rete virtuale MyVNET.</span><span class="sxs-lookup"><span data-stu-id="b6b90-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="b6b90-112">Creiamo anche un gruppo di sicurezza delle applicazioni vuoto MyASG da associare alle configurazioni IP nell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="b6b90-113">Una volta creati entrambi gli oggetti, collegheremo la configurazione IP predefinita all'oggetto MyASG.</span><span class="sxs-lookup"><span data-stu-id="b6b90-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="b6b90-114">Infine, creiamo una nuova configurazione IP nell'interfaccia di rete collegata anche all'oggetto gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b6b90-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="b6b90-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6b90-115">PARAMETERS</span></span>

### <span data-ttu-id="b6b90-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b6b90-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="b6b90-117">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b6b90-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="b6b90-119">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b6b90-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="b6b90-121">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b6b90-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="b6b90-123">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b90-124">-DefaultProfile</span></span>
<span data-ttu-id="b6b90-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b90-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6b90-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b6b90-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="b6b90-127">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b6b90-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="b6b90-129">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="b6b90-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="b6b90-131">Specifica una raccolta di riferimenti alle regole NAT (Network Address Translation) in ingresso di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="b6b90-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="b6b90-133">Specifica una raccolta di riferimenti alle regole di NAT in ingresso di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6b90-134">-Name</span></span>
<span data-ttu-id="b6b90-135">Specifica il nome della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="b6b90-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b6b90-136">-NetworkInterface</span></span>
<span data-ttu-id="b6b90-137">Specifica un oggetto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="b6b90-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="b6b90-138">Questo cmdlet aggiunge una configurazione IP dell'interfaccia di rete all'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b6b90-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-139">-Primaria</span><span class="sxs-lookup"><span data-stu-id="b6b90-139">-Primary</span></span>
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

### <span data-ttu-id="b6b90-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b6b90-140">-PrivateIpAddress</span></span>
<span data-ttu-id="b6b90-141">Specifica l'indirizzo IP statico della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-141">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b6b90-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="b6b90-143">Specifica la versione dell'indirizzo IP di una configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="b6b90-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b6b90-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6b90-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="b6b90-145">IPv4</span></span>
- <span data-ttu-id="b6b90-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="b6b90-146">IPv6</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b6b90-147">-PublicIpAddress</span></span>
<span data-ttu-id="b6b90-148">Specifica un oggetto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="b6b90-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="b6b90-149">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b6b90-150">-PublicIpAddressId</span></span>
<span data-ttu-id="b6b90-151">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-152">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b6b90-152">-Subnet</span></span>
<span data-ttu-id="b6b90-153">Specifica un oggetto **subnet** .</span><span class="sxs-lookup"><span data-stu-id="b6b90-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="b6b90-154">Questo cmdlet crea un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b6b90-155">-SubnetId</span></span>
<span data-ttu-id="b6b90-156">Questo cmdlet crea un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b6b90-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b90-157">CommonParameters</span></span>
<span data-ttu-id="b6b90-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b90-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b90-159">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6b90-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b90-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6b90-160">INPUTS</span></span>

### <span data-ttu-id="b6b90-161">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b6b90-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="b6b90-162">System. String []</span><span class="sxs-lookup"><span data-stu-id="b6b90-162">System.String[]</span></span>

### <span data-ttu-id="b6b90-163">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="b6b90-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="b6b90-164">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="b6b90-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="b6b90-165">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="b6b90-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="b6b90-166">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="b6b90-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="b6b90-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6b90-167">OUTPUTS</span></span>

### <span data-ttu-id="b6b90-168">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b6b90-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b6b90-169">Note</span><span class="sxs-lookup"><span data-stu-id="b6b90-169">NOTES</span></span>
* <span data-ttu-id="b6b90-170">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="b6b90-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b6b90-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6b90-171">RELATED LINKS</span></span>

[<span data-ttu-id="b6b90-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6b90-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b6b90-173">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6b90-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b6b90-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6b90-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b6b90-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6b90-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)