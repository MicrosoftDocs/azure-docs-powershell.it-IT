---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 80ffb0adf7703553d22cf991ad84a1af3b8e229c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190962"
---
# <span data-ttu-id="97319-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="97319-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="97319-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97319-102">SYNOPSIS</span></span>
<span data-ttu-id="97319-103">Crea una configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="97319-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97319-104">SYNTAX</span></span>

### <span data-ttu-id="97319-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97319-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97319-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="97319-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97319-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97319-107">DESCRIPTION</span></span>
<span data-ttu-id="97319-108">Il cmdlet **New-AzNetworkInterfaceIpConfig** crea una configurazione IP di una interfaccia di rete Azure per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="97319-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97319-109">EXAMPLES</span></span>

### <span data-ttu-id="97319-110">1: creare una configurazione IP con un indirizzo IP pubblico per un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="97319-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="97319-111">I primi due comandi ottengono una rete virtuale denominata myvnet e una subnet denominata sottoreti rispettivamente che sono state create in precedenza.</span><span class="sxs-lookup"><span data-stu-id="97319-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="97319-112">Questi sono archiviati rispettivamente in $vnet e $Subnet.</span><span class="sxs-lookup"><span data-stu-id="97319-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="97319-113">Il terzo comando ottiene un indirizzo IP pubblico creato in precedenza denominato PIP1.</span><span class="sxs-lookup"><span data-stu-id="97319-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="97319-114">Il comando Forth crea una nuova configurazione IP denominata "IPConfig-1" come configurazione IP primaria con un indirizzo IP pubblico associato.</span><span class="sxs-lookup"><span data-stu-id="97319-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="97319-115">L'ultimo comando crea quindi un'interfaccia di rete denominata mynic1 con questa configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="97319-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="97319-116">2: creare una configurazione IP con un indirizzo IP privato</span><span class="sxs-lookup"><span data-stu-id="97319-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="97319-117">I primi due comandi ottengono una rete virtuale denominata myvnet e una subnet denominata sottoreti rispettivamente che sono state create in precedenza.</span><span class="sxs-lookup"><span data-stu-id="97319-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="97319-118">Questi sono archiviati rispettivamente in $vnet e $Subnet.</span><span class="sxs-lookup"><span data-stu-id="97319-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="97319-119">Il terzo comando crea una nuova configurazione IP denominata "IPConfig-2" con un indirizzo IP privato 10.0.0.5 associato.</span><span class="sxs-lookup"><span data-stu-id="97319-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="97319-120">L'ultimo comando crea quindi un'interfaccia di rete denominata mynic1 con questa configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="97319-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="97319-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97319-121">PARAMETERS</span></span>

### <span data-ttu-id="97319-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97319-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="97319-123">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97319-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="97319-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="97319-125">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97319-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="97319-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="97319-127">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97319-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="97319-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="97319-129">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97319-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97319-130">-DefaultProfile</span></span>
<span data-ttu-id="97319-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97319-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97319-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97319-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="97319-133">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97319-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="97319-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="97319-135">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97319-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="97319-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="97319-137">Specifica una raccolta di riferimenti alle regole di NAT in ingresso di bilanciamento del carico a cui appartiene l'interfaccia di rete IPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="97319-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="97319-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="97319-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="97319-139">Specifica una raccolta di riferimenti alle regole NAT (Network Address Translation) in ingresso di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97319-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="97319-140">-Name</span></span>
<span data-ttu-id="97319-141">Specifica il nome della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="97319-142">-Primaria</span><span class="sxs-lookup"><span data-stu-id="97319-142">-Primary</span></span>
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

### <span data-ttu-id="97319-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="97319-143">-PrivateIpAddress</span></span>
<span data-ttu-id="97319-144">Specifica l'indirizzo IP statico della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="97319-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="97319-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="97319-146">Specifica la versione dell'indirizzo IP di una configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="97319-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="97319-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97319-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="97319-148">IPv4</span></span>
- <span data-ttu-id="97319-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="97319-149">IPv6</span></span>

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

### <span data-ttu-id="97319-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="97319-150">-PublicIpAddress</span></span>
<span data-ttu-id="97319-151">Specifica un oggetto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="97319-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="97319-152">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="97319-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="97319-153">-PublicIpAddressId</span></span>
<span data-ttu-id="97319-154">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="97319-155">-Subnet</span><span class="sxs-lookup"><span data-stu-id="97319-155">-Subnet</span></span>
<span data-ttu-id="97319-156">Specifica un oggetto **subnet** .</span><span class="sxs-lookup"><span data-stu-id="97319-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="97319-157">Questo cmdlet crea un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="97319-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="97319-158">-SubnetId</span></span>
<span data-ttu-id="97319-159">Specifica un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="97319-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="97319-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97319-160">CommonParameters</span></span>
<span data-ttu-id="97319-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97319-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97319-162">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97319-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97319-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97319-163">INPUTS</span></span>

### <span data-ttu-id="97319-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="97319-164">System.String[]</span></span>

### <span data-ttu-id="97319-165">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="97319-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="97319-166">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="97319-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="97319-167">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="97319-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="97319-168">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="97319-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="97319-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97319-169">OUTPUTS</span></span>

### <span data-ttu-id="97319-170">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="97319-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="97319-171">Note</span><span class="sxs-lookup"><span data-stu-id="97319-171">NOTES</span></span>
* <span data-ttu-id="97319-172">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="97319-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="97319-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97319-173">RELATED LINKS</span></span>

[<span data-ttu-id="97319-174">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="97319-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="97319-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="97319-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="97319-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="97319-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="97319-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="97319-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)