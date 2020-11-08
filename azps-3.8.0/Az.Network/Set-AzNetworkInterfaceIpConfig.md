---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c8dd4df4c3dd2d9aac8491b3d04e1755e6b4c38
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020451"
---
# <span data-ttu-id="22ebd-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="22ebd-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="22ebd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="22ebd-103">Aggiorna una configurazione IP per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="22ebd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22ebd-104">SYNTAX</span></span>

### <span data-ttu-id="22ebd-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22ebd-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22ebd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="22ebd-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22ebd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22ebd-107">DESCRIPTION</span></span>
<span data-ttu-id="22ebd-108">Il cmdlet **set-AzNetworkInterfaceIpConfig** aggiorna una configurazione IP per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="22ebd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22ebd-109">EXAMPLES</span></span>

### <span data-ttu-id="22ebd-110">1: modifica dell'indirizzo IP di una configurazione IP</span><span class="sxs-lookup"><span data-stu-id="22ebd-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="22ebd-111">I primi due comandi ottengono una rete virtuale denominata myvnet e una subnet denominata sottoreti e la archiviano nelle variabili $vnet e $subnet rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="22ebd-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="22ebd-112">Il terzo comando ottiene l'interfaccia di rete NIC1 associata alla configurazione IP che deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="22ebd-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="22ebd-113">Il terzo comando imposta l'indirizzo IP privato della configurazione IP primaria Ipconfig1 in 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="22ebd-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="22ebd-114">Infine, l'ultimo comando Aggiorna l'interfaccia di rete garantendo che le modifiche siano state apportate correttamente.</span><span class="sxs-lookup"><span data-stu-id="22ebd-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="22ebd-115">2: associazione di una configurazione IP a un gruppo di sicurezza dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="22ebd-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="22ebd-116">In questo esempio la variabile $asg contiene un riferimento a un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="22ebd-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="22ebd-117">Il quarto comando consente di ottenere l'interfaccia di rete NIC1 associata alla configurazione IP che deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="22ebd-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="22ebd-118">La Set-AzNetworkInterfaceIpConfig imposta l'indirizzo IP privato della configurazione di Ipconfig1 di IP principale in 10.0.0.11 e crea un'associazione con il gruppo di sicurezza dell'applicazione recuperata.</span><span class="sxs-lookup"><span data-stu-id="22ebd-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="22ebd-119">Infine, l'ultimo comando Aggiorna l'interfaccia di rete garantendo che le modifiche siano state apportate correttamente.</span><span class="sxs-lookup"><span data-stu-id="22ebd-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="22ebd-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22ebd-120">PARAMETERS</span></span>

### <span data-ttu-id="22ebd-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="22ebd-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="22ebd-122">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="22ebd-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="22ebd-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="22ebd-124">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="22ebd-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="22ebd-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="22ebd-126">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="22ebd-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="22ebd-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="22ebd-128">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="22ebd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ebd-129">-DefaultProfile</span></span>
<span data-ttu-id="22ebd-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22ebd-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22ebd-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="22ebd-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="22ebd-132">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="22ebd-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="22ebd-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="22ebd-134">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="22ebd-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="22ebd-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="22ebd-136">Specifica una raccolta di riferimenti alle regole NAT (Network Address Translation) in ingresso di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="22ebd-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="22ebd-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="22ebd-138">Specifica una raccolta di riferimenti alle regole di NAT in ingresso di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="22ebd-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="22ebd-139">-Name</span></span>
<span data-ttu-id="22ebd-140">Specifica il nome della configurazione IP di rete per cui questo cmdlet imposta.</span><span class="sxs-lookup"><span data-stu-id="22ebd-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="22ebd-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="22ebd-141">-NetworkInterface</span></span>
<span data-ttu-id="22ebd-142">Specifica un oggetto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="22ebd-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="22ebd-143">Questo cmdlet aggiunge una configurazione IP dell'interfaccia di rete all'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="22ebd-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="22ebd-144">-Primaria</span><span class="sxs-lookup"><span data-stu-id="22ebd-144">-Primary</span></span>
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

### <span data-ttu-id="22ebd-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="22ebd-145">-PrivateIpAddress</span></span>
<span data-ttu-id="22ebd-146">Specifica l'indirizzo IP statico della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="22ebd-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="22ebd-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="22ebd-148">Specifica la versione dell'indirizzo IP di una configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="22ebd-149">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="22ebd-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22ebd-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="22ebd-150">IPv4</span></span>
- <span data-ttu-id="22ebd-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="22ebd-151">IPv6</span></span>

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

### <span data-ttu-id="22ebd-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="22ebd-152">-PublicIpAddress</span></span>
<span data-ttu-id="22ebd-153">Specifica un oggetto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="22ebd-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="22ebd-154">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="22ebd-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="22ebd-155">-PublicIpAddressId</span></span>
<span data-ttu-id="22ebd-156">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="22ebd-157">-Subnet</span><span class="sxs-lookup"><span data-stu-id="22ebd-157">-Subnet</span></span>
<span data-ttu-id="22ebd-158">Specifica un oggetto **subnet** .</span><span class="sxs-lookup"><span data-stu-id="22ebd-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="22ebd-159">Questo cmdlet crea un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="22ebd-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="22ebd-160">-SubnetId</span></span>
<span data-ttu-id="22ebd-161">Questo cmdlet crea un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="22ebd-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="22ebd-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ebd-162">CommonParameters</span></span>
<span data-ttu-id="22ebd-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ebd-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ebd-164">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22ebd-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ebd-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22ebd-165">INPUTS</span></span>

### <span data-ttu-id="22ebd-166">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="22ebd-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="22ebd-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="22ebd-167">System.String[]</span></span>

### <span data-ttu-id="22ebd-168">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="22ebd-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="22ebd-169">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="22ebd-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="22ebd-170">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="22ebd-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="22ebd-171">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="22ebd-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="22ebd-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22ebd-172">OUTPUTS</span></span>

### <span data-ttu-id="22ebd-173">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="22ebd-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="22ebd-174">Note</span><span class="sxs-lookup"><span data-stu-id="22ebd-174">NOTES</span></span>
* <span data-ttu-id="22ebd-175">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="22ebd-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="22ebd-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22ebd-176">RELATED LINKS</span></span>

[<span data-ttu-id="22ebd-177">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="22ebd-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="22ebd-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="22ebd-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="22ebd-179">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="22ebd-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="22ebd-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="22ebd-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
