---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfaceipconfig
schema: 2.0.0
ms.openlocfilehash: f37f6fe6211ab05b94249b924eb76c4b98d05082
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866835"
---
# <span data-ttu-id="7f309-101">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7f309-101">Set-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="7f309-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f309-102">SYNOPSIS</span></span>
<span data-ttu-id="7f309-103">Imposta lo stato obiettivo per una configurazione IP di interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="7f309-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f309-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f309-104">SYNTAX</span></span>

### <span data-ttu-id="7f309-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f309-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f309-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f309-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f309-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f309-107">DESCRIPTION</span></span>
<span data-ttu-id="7f309-108">Il cmdlet **set-AzureRmNetworkInterfaceIpConfig** imposta lo stato obiettivo per una configurazione IP di interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="7f309-108">The **Set-AzureRmNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="7f309-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f309-109">EXAMPLES</span></span>

### <span data-ttu-id="7f309-110">1: modifica dell'indirizzo IP di una configurazione IP</span><span class="sxs-lookup"><span data-stu-id="7f309-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="7f309-111">I primi due comandi ottengono una rete virtuale denominata myvnet e una subnet denominata sottoreti e la archiviano nelle variabili $vnet e $subnet rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="7f309-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="7f309-112">Il terzo comando ottiene l'interfaccia di rete NIC1 associata alla configurazione IP che deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="7f309-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="7f309-113">Il terzo comando imposta l'indirizzo IP privato della configurazione IP primaria Ipconfig1 in 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="7f309-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="7f309-114">Infine, l'ultimo comando Aggiorna l'interfaccia di rete garantendo che le modifiche siano state apportate correttamente.</span><span class="sxs-lookup"><span data-stu-id="7f309-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="7f309-115">2: associazione di una configurazione IP a un Groupp di sicurezza delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="7f309-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="7f309-116">In questo esempio la variabile $asg contiene un riferimento a un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f309-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="7f309-117">Il quarto comando consente di ottenere l'interfaccia di rete NIC1 associata alla configurazione IP che deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="7f309-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="7f309-118">La Set-AzureRmNetworkInterfaceIpConfig imposta l'indirizzo IP privato della configurazione di Ipconfig1 di IP principale in 10.0.0.11 e crea un'associazione con il gruppo di sicurezza dell'applicazione recuperata.</span><span class="sxs-lookup"><span data-stu-id="7f309-118">The Set-AzureRmNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="7f309-119">Infine, l'ultimo comando Aggiorna l'interfaccia di rete garantendo che le modifiche siano state apportate correttamente.</span><span class="sxs-lookup"><span data-stu-id="7f309-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="7f309-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f309-120">PARAMETERS</span></span>

### <span data-ttu-id="7f309-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7f309-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="7f309-122">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7f309-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7f309-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="7f309-124">Specifica una raccolta di riferimenti al pool di indirizzi backend di Application Gateway a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7f309-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f309-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="7f309-126">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7f309-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7f309-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="7f309-128">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7f309-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f309-129">-DefaultProfile</span></span>
<span data-ttu-id="7f309-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f309-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f309-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7f309-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="7f309-132">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7f309-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7f309-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="7f309-134">Specifica una raccolta di riferimenti al pool di indirizzi backend di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7f309-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="7f309-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="7f309-136">Specifica una raccolta di riferimenti alle regole NAT (Network Address Translation) in ingresso di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7f309-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="7f309-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="7f309-138">Specifica una raccolta di riferimenti alle regole di NAT in ingresso di bilanciamento del carico a cui appartiene questa configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7f309-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f309-139">-Name</span></span>
<span data-ttu-id="7f309-140">Specifica il nome della configurazione IP di rete per cui questo cmdlet imposta.</span><span class="sxs-lookup"><span data-stu-id="7f309-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="7f309-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7f309-141">-NetworkInterface</span></span>
<span data-ttu-id="7f309-142">Specifica un oggetto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="7f309-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="7f309-143">Questo cmdlet aggiunge una configurazione IP dell'interfaccia di rete all'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7f309-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f309-144">-Primaria</span><span class="sxs-lookup"><span data-stu-id="7f309-144">-Primary</span></span>
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

### <span data-ttu-id="7f309-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f309-145">-PrivateIpAddress</span></span>
<span data-ttu-id="7f309-146">Specifica l'indirizzo IP statico della configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="7f309-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7f309-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7f309-148">Specifica la versione dell'indirizzo IP di una configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="7f309-149">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f309-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f309-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="7f309-150">IPv4</span></span>
- <span data-ttu-id="7f309-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="7f309-151">IPv6</span></span>

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

### <span data-ttu-id="7f309-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f309-152">-PublicIpAddress</span></span>
<span data-ttu-id="7f309-153">Specifica un oggetto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="7f309-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="7f309-154">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="7f309-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7f309-155">-PublicIpAddressId</span></span>
<span data-ttu-id="7f309-156">Questo cmdlet crea un riferimento a un indirizzo IP pubblico da associare alla configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="7f309-157">-Subnet</span><span class="sxs-lookup"><span data-stu-id="7f309-157">-Subnet</span></span>
<span data-ttu-id="7f309-158">Specifica un oggetto **subnet** .</span><span class="sxs-lookup"><span data-stu-id="7f309-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="7f309-159">Questo cmdlet crea un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="7f309-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7f309-160">-SubnetId</span></span>
<span data-ttu-id="7f309-161">Questo cmdlet crea un riferimento a una subnet in cui viene creata la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f309-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="7f309-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f309-162">CommonParameters</span></span>
<span data-ttu-id="7f309-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f309-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f309-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f309-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f309-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f309-165">INPUTS</span></span>

### <span data-ttu-id="7f309-166">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7f309-166">PSNetworkInterface</span></span>
<span data-ttu-id="7f309-167">Il parametro ' NetworkInterface ' accetta il valore di tipo ' PSNetworkInterface ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7f309-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="7f309-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f309-168">OUTPUTS</span></span>

### <span data-ttu-id="7f309-169">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7f309-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7f309-170">Note</span><span class="sxs-lookup"><span data-stu-id="7f309-170">NOTES</span></span>
* <span data-ttu-id="7f309-171">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="7f309-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7f309-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f309-172">RELATED LINKS</span></span>

[<span data-ttu-id="7f309-173">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7f309-173">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7f309-174">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7f309-174">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7f309-175">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7f309-175">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7f309-176">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7f309-176">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)


