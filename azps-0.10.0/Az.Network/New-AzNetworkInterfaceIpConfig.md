---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 7776bb57215ce3cb9b4291a0a71fdb01e028491e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860473"
---
# <span data-ttu-id="c1c74-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1c74-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="c1c74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1c74-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c74-103">Crea una configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="c1c74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1c74-104">SYNTAX</span></span>

### <span data-ttu-id="c1c74-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1c74-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1c74-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1c74-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1c74-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1c74-107">DESCRIPTION</span></span>
<span data-ttu-id="c1c74-108">Il cmdlet **New-AzNetworkInterfaceIpConfig** crea una configurazione IP di una interfaccia di rete Azure per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="c1c74-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1c74-109">EXAMPLES</span></span>

### <span data-ttu-id="c1c74-110">1: creare una configurazione IP con un indirizzo IP pubblico per un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="c1c74-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="c1c74-111">I primi due comandi ottengono una rete virtuale denominata myvnet e una subnet denominata sottoreti rispettivamente che sono state create in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c1c74-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="c1c74-112">Questi sono archiviati rispettivamente in $vnet e $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c1c74-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="c1c74-113">Il terzo comando ottiene un indirizzo IP pubblico creato in precedenza denominato PIP1.</span><span class="sxs-lookup"><span data-stu-id="c1c74-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="c1c74-114">Il comando Forth crea una nuova configurazione IP denominata "IPConfig-1" come configurazione IP primaria con un indirizzo IP pubblico associato.</span><span class="sxs-lookup"><span data-stu-id="c1c74-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="c1c74-115">L'ultimo comando crea quindi un'interfaccia di rete denominata mynic1 con questa configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="c1c74-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="c1c74-116">2: creare una configurazione IP con un indirizzo IP privato</span><span class="sxs-lookup"><span data-stu-id="c1c74-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="c1c74-117">I primi due comandi ottengono una rete virtuale denominata myvnet e una subnet denominata sottoreti rispettivamente che sono state create in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c1c74-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="c1c74-118">Questi sono archiviati rispettivamente in $vnet e $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c1c74-118">These are stored in $vnet and $Subnet respectively.</span></span>  <span data-ttu-id="c1c74-119">Il terzo comando crea una nuova configurazione IP denominata "IPConfig-2" con un indirizzo IP privato 10.0.0.5 associato.</span><span class="sxs-lookup"><span data-stu-id="c1c74-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="c1c74-120">L'ultimo comando crea quindi un'interfaccia di rete denominata mynic1 con questa configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="c1c74-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="c1c74-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1c74-121">PARAMETERS</span></span>

### <span data-ttu-id="c1c74-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1c74-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="c1c74-123">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="c1c74-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c1c74-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="c1c74-125">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="c1c74-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c1c74-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="c1c74-127">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="c1c74-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c1c74-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="c1c74-129">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="c1c74-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c74-130">-DefaultProfile</span></span>
<span data-ttu-id="c1c74-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1c74-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1c74-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1c74-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="c1c74-133">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="c1c74-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c1c74-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="c1c74-135">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="c1c74-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="c1c74-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="c1c74-137">Specifica una raccolta di riferimenti alle regole di NAT in ingresso di bilanciamento del carico a cui appartiene l'interfaccia di rete IPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c1c74-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="c1c74-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="c1c74-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="c1c74-139">Specifica una raccolta di riferimenti alle regole NAT (Network Address Translation) in ingresso di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="c1c74-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1c74-140">-Name</span></span>
<span data-ttu-id="c1c74-141">Specifica il nome della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="c1c74-142">-Primaria</span><span class="sxs-lookup"><span data-stu-id="c1c74-142">-Primary</span></span>
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

### <span data-ttu-id="c1c74-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="c1c74-143">-PrivateIpAddress</span></span>
<span data-ttu-id="c1c74-144">Specifica l'indirizzo IP statico della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-144">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c74-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="c1c74-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="c1c74-146">Specifica la versione dell'indirizzo IP di una configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-146">Specifies the IP address version of a network interface IP configuration.</span></span>

<span data-ttu-id="c1c74-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c1c74-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c1c74-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="c1c74-148">IPv4</span></span>
- <span data-ttu-id="c1c74-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="c1c74-149">IPv6</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c74-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c1c74-150">-PublicIpAddress</span></span>
<span data-ttu-id="c1c74-151">Specifica un oggetto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="c1c74-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="c1c74-152">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c74-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="c1c74-153">-PublicIpAddressId</span></span>
<span data-ttu-id="c1c74-154">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="c1c74-155">-Subnet</span><span class="sxs-lookup"><span data-stu-id="c1c74-155">-Subnet</span></span>
<span data-ttu-id="c1c74-156">Specifica un oggetto **subnet** .</span><span class="sxs-lookup"><span data-stu-id="c1c74-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="c1c74-157">Questo cmdlet crea un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c74-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c1c74-158">-SubnetId</span></span>
<span data-ttu-id="c1c74-159">Specifica un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c1c74-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="c1c74-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c74-160">CommonParameters</span></span>
<span data-ttu-id="c1c74-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1c74-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c74-162">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c74-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c74-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1c74-163">INPUTS</span></span>

## <span data-ttu-id="c1c74-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1c74-164">OUTPUTS</span></span>

### <span data-ttu-id="c1c74-165">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1c74-165">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="c1c74-166">Note</span><span class="sxs-lookup"><span data-stu-id="c1c74-166">NOTES</span></span>
* <span data-ttu-id="c1c74-167">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="c1c74-167">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c1c74-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1c74-168">RELATED LINKS</span></span>

[<span data-ttu-id="c1c74-169">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1c74-169">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c1c74-170">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1c74-170">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c1c74-171">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1c74-171">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c1c74-172">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1c74-172">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


