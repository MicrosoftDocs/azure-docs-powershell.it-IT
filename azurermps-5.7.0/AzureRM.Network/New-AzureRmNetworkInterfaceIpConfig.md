---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4499daa24230b9ec0b4731aa7be17c6f040db7d6
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "93688666"
---
# <span data-ttu-id="de851-101">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="de851-101">New-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="de851-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de851-102">SYNOPSIS</span></span>
<span data-ttu-id="de851-103">Crea una configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-103">Creates a network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de851-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de851-104">SYNTAX</span></span>

### <span data-ttu-id="de851-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de851-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de851-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="de851-106">SetByResourceId</span></span>
```
New-AzureRmNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de851-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de851-107">DESCRIPTION</span></span>
<span data-ttu-id="de851-108">Il cmdlet **New-AzureRmNetworkInterfaceIpConfig** crea una configurazione IP di una interfaccia di rete Azure per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-108">The **New-AzureRmNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="de851-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de851-109">EXAMPLES</span></span>

### <span data-ttu-id="de851-110">1: creare una configurazione IP con un indirizzo IP pubblico per un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="de851-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzureRmPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzureRmNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="de851-111">I primi due comandi ottengono una rete virtuale denominata myvnet e una subnet denominata sottoreti rispettivamente che sono state create in precedenza.</span><span class="sxs-lookup"><span data-stu-id="de851-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="de851-112">Questi sono archiviati rispettivamente in $vnet e $Subnet.</span><span class="sxs-lookup"><span data-stu-id="de851-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="de851-113">Il terzo comando ottiene un indirizzo IP pubblico creato in precedenza denominato PIP1.</span><span class="sxs-lookup"><span data-stu-id="de851-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="de851-114">Il comando Forth crea una nuova configurazione IP denominata "IPConfig-1" come configurazione IP primaria con un indirizzo IP pubblico associato.</span><span class="sxs-lookup"><span data-stu-id="de851-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="de851-115">L'ultimo comando crea quindi un'interfaccia di rete denominata mynic1 con questa configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="de851-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="de851-116">2: creare una configurazione IP con un indirizzo IP privato</span><span class="sxs-lookup"><span data-stu-id="de851-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzureRmNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzureRmNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="de851-117">I primi due comandi ottengono una rete virtuale denominata myvnet e una subnet denominata sottoreti rispettivamente che sono state create in precedenza.</span><span class="sxs-lookup"><span data-stu-id="de851-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="de851-118">Questi sono archiviati rispettivamente in $vnet e $Subnet.</span><span class="sxs-lookup"><span data-stu-id="de851-118">These are stored in $vnet and $Subnet respectively.</span></span>  <span data-ttu-id="de851-119">Il terzo comando crea una nuova configurazione IP denominata "IPConfig-2" con un indirizzo IP privato 10.0.0.5 associato.</span><span class="sxs-lookup"><span data-stu-id="de851-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="de851-120">L'ultimo comando crea quindi un'interfaccia di rete denominata mynic1 con questa configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="de851-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="de851-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de851-121">PARAMETERS</span></span>

### <span data-ttu-id="de851-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="de851-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="de851-123">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="de851-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="de851-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="de851-125">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="de851-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="de851-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="de851-127">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="de851-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="de851-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="de851-129">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="de851-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de851-130">-DefaultProfile</span></span>
<span data-ttu-id="de851-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de851-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de851-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="de851-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="de851-133">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="de851-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="de851-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="de851-135">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="de851-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="de851-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="de851-137">Specifica una raccolta di riferimenti alle regole di NAT in ingresso di bilanciamento del carico a cui appartiene l'interfaccia di rete IPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="de851-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="de851-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="de851-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="de851-139">Specifica una raccolta di riferimenti alle regole NAT (Network Address Translation) in ingresso di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="de851-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="de851-140">-Name</span></span>
<span data-ttu-id="de851-141">Specifica il nome della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="de851-142">-Primaria</span><span class="sxs-lookup"><span data-stu-id="de851-142">-Primary</span></span>
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

### <span data-ttu-id="de851-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="de851-143">-PrivateIpAddress</span></span>
<span data-ttu-id="de851-144">Specifica l'indirizzo IP statico della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="de851-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="de851-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="de851-146">Specifica la versione dell'indirizzo IP di una configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-146">Specifies the IP address version of a network interface IP configuration.</span></span>

<span data-ttu-id="de851-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="de851-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="de851-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="de851-148">IPv4</span></span>
- <span data-ttu-id="de851-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="de851-149">IPv6</span></span>

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

### <span data-ttu-id="de851-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="de851-150">-PublicIpAddress</span></span>
<span data-ttu-id="de851-151">Specifica un oggetto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="de851-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="de851-152">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="de851-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="de851-153">-PublicIpAddressId</span></span>
<span data-ttu-id="de851-154">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="de851-155">-Subnet</span><span class="sxs-lookup"><span data-stu-id="de851-155">-Subnet</span></span>
<span data-ttu-id="de851-156">Specifica un oggetto **subnet** .</span><span class="sxs-lookup"><span data-stu-id="de851-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="de851-157">Questo cmdlet crea un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="de851-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="de851-158">-SubnetId</span></span>
<span data-ttu-id="de851-159">Specifica un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="de851-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="de851-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de851-160">CommonParameters</span></span>
<span data-ttu-id="de851-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de851-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de851-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de851-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de851-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de851-163">INPUTS</span></span>

### <span data-ttu-id="de851-164">Nessuno</span><span class="sxs-lookup"><span data-stu-id="de851-164">None</span></span>
<span data-ttu-id="de851-165">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="de851-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de851-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de851-166">OUTPUTS</span></span>

### <span data-ttu-id="de851-167">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="de851-167">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="de851-168">Note</span><span class="sxs-lookup"><span data-stu-id="de851-168">NOTES</span></span>
* <span data-ttu-id="de851-169">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="de851-169">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="de851-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de851-170">RELATED LINKS</span></span>

[<span data-ttu-id="de851-171">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="de851-171">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="de851-172">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="de851-172">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="de851-173">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="de851-173">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="de851-174">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="de851-174">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


