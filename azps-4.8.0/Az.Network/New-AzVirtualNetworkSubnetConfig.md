---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7afedb15ea5e7b5e2968dbb425a662f7de7e2ac1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192773"
---
# <span data-ttu-id="0d692-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0d692-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="0d692-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d692-102">SYNOPSIS</span></span>
<span data-ttu-id="0d692-103">Crea una configurazione della subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d692-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="0d692-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d692-104">SYNTAX</span></span>

### <span data-ttu-id="0d692-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0d692-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d692-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0d692-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d692-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d692-107">DESCRIPTION</span></span>
<span data-ttu-id="0d692-108">**Il cmdlet New-AzVirtualNetworkSubnetConfig** crea una configurazione di subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d692-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="0d692-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d692-109">EXAMPLES</span></span>

### <span data-ttu-id="0d692-110">Esempio 1: creare una rete virtuale con due subnet e un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="0d692-110">Example 1: Create a virtual network with two subnets and a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$natGatewaySubnet = New-AzVirtualNetworkSubnetConfig -Name natGatewaySubnet `
   -AddressPrefix "10.0.3.0/24" -InputObject $natGateway

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet,$natGatewaySubnet
```

<span data-ttu-id="0d692-111">Questo esempio crea due nuove configurazioni di subnet usando il cmdlet New-AzVirtualSubnetConfig e le usa per creare una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d692-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="0d692-112">Il modello New-AzVirtualSubnetConfig crea solo una rappresentazione in memoria della subnet.</span><span class="sxs-lookup"><span data-stu-id="0d692-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="0d692-113">In questo esempio, frontendSubnet ha la notazione CIDR 10.0.1.0/24 e fa riferimento a un gruppo di sicurezza di rete che consente l'accesso RDP.</span><span class="sxs-lookup"><span data-stu-id="0d692-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="0d692-114">BackendSubnet ha la notazione CIDR 10.0.2.0/24 e fa riferimento allo stesso gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="0d692-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="0d692-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d692-115">PARAMETERS</span></span>

### <span data-ttu-id="0d692-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0d692-116">-AddressPrefix</span></span>
<span data-ttu-id="0d692-117">Specifica un intervallo di indirizzi IP per una configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="0d692-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="0d692-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d692-118">-DefaultProfile</span></span>
<span data-ttu-id="0d692-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d692-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d692-120">-Delega</span><span class="sxs-lookup"><span data-stu-id="0d692-120">-Delegation</span></span>
<span data-ttu-id="0d692-121">Elenco di servizi che dispongono delle autorizzazioni per eseguire operazioni in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="0d692-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="0d692-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d692-122">-InputObject</span></span>
<span data-ttu-id="0d692-123">Specifica il gateway NAT associato alla configurazione della subnet</span><span class="sxs-lookup"><span data-stu-id="0d692-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="0d692-124">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="0d692-124">-IpAllocation</span></span>
<span data-ttu-id="0d692-125">Specifica IpAllocations per una subnet.</span><span class="sxs-lookup"><span data-stu-id="0d692-125">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="0d692-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d692-126">-Name</span></span>
<span data-ttu-id="0d692-127">Specifica il nome della configurazione della subnet da creare.</span><span class="sxs-lookup"><span data-stu-id="0d692-127">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="0d692-128">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0d692-128">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0d692-129">Specifica un oggetto NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="0d692-129">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="0d692-130">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0d692-130">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="0d692-131">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="0d692-131">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="0d692-132">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="0d692-132">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="0d692-133">Configurare per abilitare o disabilitare l'applicazione di criteri di rete nell'endpoint privato nella subnet.</span><span class="sxs-lookup"><span data-stu-id="0d692-133">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="0d692-134">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="0d692-134">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="0d692-135">Configurare per abilitare o disabilitare l'applicazione di criteri di rete sul servizio di collegamento privato nella subnet.</span><span class="sxs-lookup"><span data-stu-id="0d692-135">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="0d692-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d692-136">-ResourceId</span></span>
<span data-ttu-id="0d692-137">Specifica l'ID della risorsa gateway NAT associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="0d692-137">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="0d692-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="0d692-138">-RouteTable</span></span>
<span data-ttu-id="0d692-139">Specifica la tabella route associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="0d692-139">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="0d692-140">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="0d692-140">-RouteTableId</span></span>
<span data-ttu-id="0d692-141">Specifica l'ID della tabella route associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="0d692-141">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="0d692-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d692-142">-ServiceEndpoint</span></span>
<span data-ttu-id="0d692-143">Valore endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="0d692-143">Service Endpoint Value</span></span>

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

### <span data-ttu-id="0d692-144">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0d692-144">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="0d692-145">Criteri endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="0d692-145">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="0d692-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d692-146">CommonParameters</span></span>
<span data-ttu-id="0d692-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d692-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d692-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d692-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d692-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d692-149">INPUTS</span></span>

### <span data-ttu-id="0d692-150">System. String</span><span class="sxs-lookup"><span data-stu-id="0d692-150">System.String</span></span>

### <span data-ttu-id="0d692-151">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0d692-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="0d692-152">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d692-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="0d692-153">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="0d692-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="0d692-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="0d692-154">System.String[]</span></span>

### <span data-ttu-id="0d692-155">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="0d692-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="0d692-156">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="0d692-156">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="0d692-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d692-157">OUTPUTS</span></span>

### <span data-ttu-id="0d692-158">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="0d692-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="0d692-159">Note</span><span class="sxs-lookup"><span data-stu-id="0d692-159">NOTES</span></span>

## <span data-ttu-id="0d692-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d692-160">RELATED LINKS</span></span>

[<span data-ttu-id="0d692-161">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0d692-161">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="0d692-162">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0d692-162">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="0d692-163">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0d692-163">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="0d692-164">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0d692-164">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)