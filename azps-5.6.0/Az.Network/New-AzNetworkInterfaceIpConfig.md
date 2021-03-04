---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 72d2439e66245e8469e440cb5e501cd9e9379fa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953934"
---
# <span data-ttu-id="20f21-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="20f21-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="20f21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f21-102">SYNOPSIS</span></span>
<span data-ttu-id="20f21-103">Crea una configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="20f21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20f21-104">SYNTAX</span></span>

### <span data-ttu-id="20f21-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="20f21-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20f21-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="20f21-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20f21-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="20f21-107">DESCRIPTION</span></span>
<span data-ttu-id="20f21-108">Il cmdlet **New-AzNetworkInterfaceIpConfig crea** una configurazione IP dell'interfaccia di rete di Azure per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="20f21-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20f21-109">EXAMPLES</span></span>

### <span data-ttu-id="20f21-110">1: Creare una configurazione IP con un indirizzo IP pubblico per un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="20f21-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="20f21-111">I primi due comandi ottengono rispettivamente una rete virtuale denominata myvnet e una subnet denominata mysubnet, create in precedenza.</span><span class="sxs-lookup"><span data-stu-id="20f21-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="20f21-112">Vengono archiviate in $vnet e $Subnet, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="20f21-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="20f21-113">Il terzo comando ottiene un indirizzo IP pubblico creato in precedenza denominato PIP1.</span><span class="sxs-lookup"><span data-stu-id="20f21-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="20f21-114">Il secondo comando crea una nuova configurazione IP denominata "IPConfig-1" come configurazione IP principale con un indirizzo IP pubblico associato.</span><span class="sxs-lookup"><span data-stu-id="20f21-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="20f21-115">L'ultimo comando crea quindi un'interfaccia di rete denominata mynic1 usando questa configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="20f21-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="20f21-116">2: Creare una configurazione IP con un indirizzo IP privato</span><span class="sxs-lookup"><span data-stu-id="20f21-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="20f21-117">I primi due comandi ottengono rispettivamente una rete virtuale denominata myvnet e una subnet denominata mysubnet, create in precedenza.</span><span class="sxs-lookup"><span data-stu-id="20f21-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="20f21-118">Vengono archiviate in $vnet e $Subnet, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="20f21-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="20f21-119">Il terzo comando crea una nuova configurazione IP denominata "IPConfig-2" con un indirizzo IP privato 10.0.0.5 associato.</span><span class="sxs-lookup"><span data-stu-id="20f21-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="20f21-120">L'ultimo comando crea quindi un'interfaccia di rete denominata mynic1 usando questa configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="20f21-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="20f21-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20f21-121">PARAMETERS</span></span>

### <span data-ttu-id="20f21-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="20f21-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="20f21-123">Specifica una raccolta di riferimenti al pool di indirizzi back-end del gateway applicazione a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="20f21-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="20f21-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="20f21-125">Specifica una raccolta di riferimenti al pool di indirizzi back-end del gateway applicazione a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="20f21-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20f21-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="20f21-127">Specifica una raccolta di riferimenti a gruppi di sicurezza applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="20f21-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="20f21-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="20f21-129">Specifica una raccolta di riferimenti a gruppi di sicurezza applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="20f21-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f21-130">-DefaultProfile</span></span>
<span data-ttu-id="20f21-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20f21-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20f21-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="20f21-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="20f21-133">Specifica una raccolta di riferimenti al pool di indirizzi back-end di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="20f21-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="20f21-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="20f21-135">Specifica una raccolta di riferimenti al pool di indirizzi back-end di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="20f21-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="20f21-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="20f21-137">Specifica una raccolta di riferimenti a regole Nat in ingresso di bilanciamento del carico a cui appartiene questa IPConfiguration dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="20f21-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="20f21-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="20f21-139">Specifica una raccolta di riferimenti a regole NAT (Network Address Translation) in ingresso a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="20f21-140">-Name</span><span class="sxs-lookup"><span data-stu-id="20f21-140">-Name</span></span>
<span data-ttu-id="20f21-141">Specifica il nome della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="20f21-142">-Principale</span><span class="sxs-lookup"><span data-stu-id="20f21-142">-Primary</span></span>
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

### <span data-ttu-id="20f21-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="20f21-143">-PrivateIpAddress</span></span>
<span data-ttu-id="20f21-144">Specifica l'indirizzo IP statico della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="20f21-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="20f21-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="20f21-146">Specifica la versione dell'indirizzo IP di una configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="20f21-147">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="20f21-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="20f21-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="20f21-148">IPv4</span></span>
- <span data-ttu-id="20f21-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="20f21-149">IPv6</span></span>

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

### <span data-ttu-id="20f21-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="20f21-150">-PublicIpAddress</span></span>
<span data-ttu-id="20f21-151">Specifica un **oggetto PublicIPAddress.**</span><span class="sxs-lookup"><span data-stu-id="20f21-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="20f21-152">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="20f21-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="20f21-153">-PublicIpAddressId</span></span>
<span data-ttu-id="20f21-154">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="20f21-155">-Subnet</span><span class="sxs-lookup"><span data-stu-id="20f21-155">-Subnet</span></span>
<span data-ttu-id="20f21-156">Specifica un oggetto **Subnet.**</span><span class="sxs-lookup"><span data-stu-id="20f21-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="20f21-157">Questo cmdlet crea un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="20f21-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="20f21-158">-SubnetId</span></span>
<span data-ttu-id="20f21-159">Specifica un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="20f21-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="20f21-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f21-160">CommonParameters</span></span>
<span data-ttu-id="20f21-161">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f21-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f21-162">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f21-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f21-163">INPUT</span><span class="sxs-lookup"><span data-stu-id="20f21-163">INPUTS</span></span>

### <span data-ttu-id="20f21-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="20f21-164">System.String[]</span></span>

### <span data-ttu-id="20f21-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="20f21-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="20f21-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="20f21-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="20f21-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="20f21-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="20f21-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="20f21-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="20f21-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20f21-169">OUTPUTS</span></span>

### <span data-ttu-id="20f21-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="20f21-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="20f21-171">NOTE</span><span class="sxs-lookup"><span data-stu-id="20f21-171">NOTES</span></span>
* <span data-ttu-id="20f21-172">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="20f21-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="20f21-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20f21-173">RELATED LINKS</span></span>

[<span data-ttu-id="20f21-174">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="20f21-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="20f21-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="20f21-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="20f21-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="20f21-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="20f21-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="20f21-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
