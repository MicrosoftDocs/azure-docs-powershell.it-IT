---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 46c08913b36958bb9cd0bd75393b87ed887a0f1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688407"
---
# <span data-ttu-id="06118-101">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="06118-101">Add-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="06118-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06118-102">SYNOPSIS</span></span>
<span data-ttu-id="06118-103">Aggiunge una configurazione IP di interfaccia di rete a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-103">Adds a network interface IP configuration to a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06118-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06118-104">SYNTAX</span></span>

### <span data-ttu-id="06118-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06118-105">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06118-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="06118-106">SetByResourceId</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06118-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06118-107">DESCRIPTION</span></span>
<span data-ttu-id="06118-108">Il cmdlet **Add-AzureRmNetworkInterfaceIpConfig** aggiunge una configurazione IP di interfaccia di rete a un'interfaccia di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="06118-108">The **Add-AzureRmNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="06118-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06118-109">EXAMPLES</span></span>

### <span data-ttu-id="06118-110">Esempio 1: aggiungere una nuova configurazione IP con un gruppo di sicurezza dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="06118-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzureRmvirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzureRmNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US"  -Subnet $vnet.Subnets[0]

$asg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzureRmNetworkInterface

$nic | Add-AzureRmNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg  | Set-AzureRmNetworkInterface
```

<span data-ttu-id="06118-111">In questo esempio creiamo una nuova interfaccia di rete MyNetworkInterface che appartiene a una subnet nella nuova rete virtuale MyVNET.</span><span class="sxs-lookup"><span data-stu-id="06118-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="06118-112">Creiamo anche un gruppo di sicurezza delle applicazioni vuoto MyASG da associare alle configurazioni IP nell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="06118-113">Una volta creati entrambi gli oggetti, collegheremo la configurazione IP predefinita all'oggetto MyASG.</span><span class="sxs-lookup"><span data-stu-id="06118-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="06118-114">Infine, creiamo una nuova configurazione IP nell'interfaccia di rete collegata anche all'oggetto gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="06118-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="06118-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06118-115">PARAMETERS</span></span>

### <span data-ttu-id="06118-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="06118-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="06118-117">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06118-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="06118-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="06118-119">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06118-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="06118-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="06118-121">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06118-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="06118-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="06118-123">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06118-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06118-124">-DefaultProfile</span></span>
<span data-ttu-id="06118-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06118-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06118-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="06118-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="06118-127">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06118-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="06118-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="06118-129">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06118-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="06118-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="06118-131">Specifica una raccolta di riferimenti alle regole NAT (Network Address Translation) in ingresso di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06118-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="06118-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="06118-133">Specifica una raccolta di riferimenti alle regole di NAT in ingresso di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06118-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="06118-134">-Name</span></span>
<span data-ttu-id="06118-135">Specifica il nome della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="06118-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="06118-136">-NetworkInterface</span></span>
<span data-ttu-id="06118-137">Specifica un oggetto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="06118-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="06118-138">Questo cmdlet aggiunge una configurazione IP dell'interfaccia di rete all'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="06118-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="06118-139">-Primaria</span><span class="sxs-lookup"><span data-stu-id="06118-139">-Primary</span></span>
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

### <span data-ttu-id="06118-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="06118-140">-PrivateIpAddress</span></span>
<span data-ttu-id="06118-141">Specifica l'indirizzo IP statico della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="06118-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="06118-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="06118-143">Specifica la versione dell'indirizzo IP di una configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="06118-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="06118-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06118-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="06118-145">IPv4</span></span>
- <span data-ttu-id="06118-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="06118-146">IPv6</span></span>

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

### <span data-ttu-id="06118-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="06118-147">-PublicIpAddress</span></span>
<span data-ttu-id="06118-148">Specifica un oggetto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="06118-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="06118-149">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="06118-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="06118-150">-PublicIpAddressId</span></span>
<span data-ttu-id="06118-151">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="06118-152">-Subnet</span><span class="sxs-lookup"><span data-stu-id="06118-152">-Subnet</span></span>
<span data-ttu-id="06118-153">Specifica un oggetto **subnet** .</span><span class="sxs-lookup"><span data-stu-id="06118-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="06118-154">Questo cmdlet crea un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="06118-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="06118-155">-SubnetId</span></span>
<span data-ttu-id="06118-156">Questo cmdlet crea un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="06118-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="06118-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06118-157">CommonParameters</span></span>
<span data-ttu-id="06118-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06118-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06118-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06118-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06118-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06118-160">INPUTS</span></span>

### <span data-ttu-id="06118-161">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="06118-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="06118-162">Parametri: NetworkInterface (ByValue)</span><span class="sxs-lookup"><span data-stu-id="06118-162">Parameters: NetworkInterface (ByValue)</span></span>

### <span data-ttu-id="06118-163">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="06118-163">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="06118-164">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="06118-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="06118-165">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSInboundNatRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="06118-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="06118-166">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="06118-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="06118-167">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="06118-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="06118-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06118-168">OUTPUTS</span></span>

### <span data-ttu-id="06118-169">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="06118-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="06118-170">Note</span><span class="sxs-lookup"><span data-stu-id="06118-170">NOTES</span></span>
* <span data-ttu-id="06118-171">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="06118-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="06118-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06118-172">RELATED LINKS</span></span>

[<span data-ttu-id="06118-173">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="06118-173">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="06118-174">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="06118-174">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="06118-175">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="06118-175">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="06118-176">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="06118-176">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


