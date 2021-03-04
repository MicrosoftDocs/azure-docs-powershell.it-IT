---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 47c56f2f55a07dc2567ca3ee2030e075d90dc324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952029"
---
# <span data-ttu-id="79c37-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="79c37-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="79c37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79c37-102">SYNOPSIS</span></span>
<span data-ttu-id="79c37-103">Aggiorna la configurazione della subnet per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="79c37-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="79c37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79c37-104">SYNTAX</span></span>

### <span data-ttu-id="79c37-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="79c37-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79c37-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="79c37-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79c37-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79c37-107">DESCRIPTION</span></span>
<span data-ttu-id="79c37-108">Il cmdlet **Set-AzVirtualNetworkSubnetConfig** aggiorna la configurazione della subnet per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="79c37-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="79c37-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79c37-109">EXAMPLES</span></span>

### <span data-ttu-id="79c37-110">1: Modificare il prefisso dell'indirizzo di una subnet</span><span class="sxs-lookup"><span data-stu-id="79c37-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="79c37-111">Questo esempio crea una rete virtuale con una subnet.</span><span class="sxs-lookup"><span data-stu-id="79c37-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="79c37-112">Viene quindi chiamato Set-AzVirtualNetworkSubnetConfig modificare il prefisso dell'indirizzo della subnet.</span><span class="sxs-lookup"><span data-stu-id="79c37-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="79c37-113">Questo influisce solo sulla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="79c37-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="79c37-114">Set-AzVirtualNetwork viene quindi chiamata per modificare la rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="79c37-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="79c37-115">2: Aggiungere un gruppo di sicurezza di rete a una subnet</span><span class="sxs-lookup"><span data-stu-id="79c37-115">2: Add a network security group to a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="79c37-116">Questo esempio crea un gruppo di risorse con una rete virtuale contenente una sola subnet.</span><span class="sxs-lookup"><span data-stu-id="79c37-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="79c37-117">Viene quindi creato un gruppo di sicurezza di rete con una regola consenti per il traffico RDP.</span><span class="sxs-lookup"><span data-stu-id="79c37-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="79c37-118">Il Set-AzVirtualNetworkSubnetConfig cmdlet viene usato per modificare la rappresentazione in memoria della subnet frontend in modo che punti al gruppo di sicurezza di rete appena creato.</span><span class="sxs-lookup"><span data-stu-id="79c37-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="79c37-119">Il Set-AzVirtualNetwork cmdlet viene quindi chiamato per scrivere di nuovo lo stato modificato nel servizio.</span><span class="sxs-lookup"><span data-stu-id="79c37-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="79c37-120">3: Collegare un gateway Nat a una subnet</span><span class="sxs-lookup"><span data-stu-id="79c37-120">3: Attach a Nat Gateway to a subnet</span></span>
```
$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natGateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" 

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -InputObject $natGateway 

$virtualNetwork | Set-AzVirtualNetwork
```

## <span data-ttu-id="79c37-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79c37-121">PARAMETERS</span></span>

### <span data-ttu-id="79c37-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="79c37-122">-AddressPrefix</span></span>
<span data-ttu-id="79c37-123">Specifica un intervallo di indirizzi IP per la configurazione di una subnet.</span><span class="sxs-lookup"><span data-stu-id="79c37-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c37-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c37-124">-DefaultProfile</span></span>
<span data-ttu-id="79c37-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79c37-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79c37-126">-Delegation</span><span class="sxs-lookup"><span data-stu-id="79c37-126">-Delegation</span></span>
<span data-ttu-id="79c37-127">Elenco dei servizi autorizzati a eseguire operazioni nella subnet.</span><span class="sxs-lookup"><span data-stu-id="79c37-127">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c37-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79c37-128">-InputObject</span></span>
<span data-ttu-id="79c37-129">Specifica il gateway NAT associato alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="79c37-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByResource
Aliases: NatGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c37-130">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="79c37-130">-IpAllocation</span></span>
<span data-ttu-id="79c37-131">Specifica IpAllocations per una subnet.</span><span class="sxs-lookup"><span data-stu-id="79c37-131">Specifies IpAllocations for a subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c37-132">-Name</span><span class="sxs-lookup"><span data-stu-id="79c37-132">-Name</span></span>
<span data-ttu-id="79c37-133">Specifica il nome di una configurazione subnet configurata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79c37-133">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="79c37-134">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="79c37-134">-NetworkSecurityGroup</span></span>
<span data-ttu-id="79c37-135">Specifica un **oggetto NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="79c37-135">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c37-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="79c37-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="79c37-137">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="79c37-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="79c37-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="79c37-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="79c37-139">Configura per abilitare o disabilitare l'applicazione di criteri di rete nell'endpoint privato nella subnet.</span><span class="sxs-lookup"><span data-stu-id="79c37-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="79c37-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="79c37-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="79c37-141">Configurare per abilitare o disabilitare l'applicazione di criteri di rete nel servizio di collegamento privato nella subnet.</span><span class="sxs-lookup"><span data-stu-id="79c37-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="79c37-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79c37-142">-ResourceId</span></span>
<span data-ttu-id="79c37-143">Specifica l'ID della risorsa Gateway NAT associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="79c37-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: NatGatewayId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c37-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="79c37-144">-RouteTable</span></span>
<span data-ttu-id="79c37-145">Specifica l'oggetto tabella di route associato al gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="79c37-145">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c37-146">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="79c37-146">-RouteTableId</span></span>
<span data-ttu-id="79c37-147">Specifica l'ID dell'oggetto tabella di route associato al gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="79c37-147">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="79c37-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="79c37-148">-ServiceEndpoint</span></span>
<span data-ttu-id="79c37-149">Valore endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="79c37-149">Service Endpoint Value</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c37-150">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="79c37-150">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="79c37-151">Criteri endpoint di servizio</span><span class="sxs-lookup"><span data-stu-id="79c37-151">Service Endpoint Policies</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c37-152">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="79c37-152">-VirtualNetwork</span></span>
<span data-ttu-id="79c37-153">Specifica **l'oggetto VirtualNetwork** che contiene la configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="79c37-153">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79c37-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c37-154">CommonParameters</span></span>
<span data-ttu-id="79c37-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c37-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c37-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79c37-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c37-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="79c37-157">INPUTS</span></span>

### <span data-ttu-id="79c37-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="79c37-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="79c37-159">System.String</span><span class="sxs-lookup"><span data-stu-id="79c37-159">System.String</span></span>

### <span data-ttu-id="79c37-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="79c37-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="79c37-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="79c37-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="79c37-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="79c37-162">System.String[]</span></span>

### <span data-ttu-id="79c37-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="79c37-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="79c37-164">Microsoft.Azure.Commands.Network.Models.PSDelegamento[]</span><span class="sxs-lookup"><span data-stu-id="79c37-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="79c37-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79c37-165">OUTPUTS</span></span>

### <span data-ttu-id="79c37-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="79c37-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="79c37-167">NOTE</span><span class="sxs-lookup"><span data-stu-id="79c37-167">NOTES</span></span>

## <span data-ttu-id="79c37-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79c37-168">RELATED LINKS</span></span>

[<span data-ttu-id="79c37-169">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="79c37-169">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="79c37-170">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="79c37-170">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="79c37-171">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="79c37-171">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="79c37-172">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="79c37-172">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
