---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 144d04172f3169075a32c5e8111a90ff407532b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021187"
---
# <span data-ttu-id="b2257-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b2257-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="b2257-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2257-102">SYNOPSIS</span></span>
<span data-ttu-id="b2257-103">Crea una configurazione della subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2257-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="b2257-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2257-104">SYNTAX</span></span>

### <span data-ttu-id="b2257-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2257-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2257-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2257-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2257-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2257-107">DESCRIPTION</span></span>
<span data-ttu-id="b2257-108">**Il cmdlet New-AzVirtualNetworkSubnetConfig** crea una configurazione di subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2257-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="b2257-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2257-109">EXAMPLES</span></span>

### <span data-ttu-id="b2257-110">1: creare una rete virtuale con due subnet e un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="b2257-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
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

<span data-ttu-id="b2257-111">Questo esempio crea due nuove configurazioni di subnet usando il cmdlet New-AzVirtualSubnetConfig e le usa per creare una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2257-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="b2257-112">Il modello New-AzVirtualSubnetConfig crea solo una rappresentazione in memoria della subnet.</span><span class="sxs-lookup"><span data-stu-id="b2257-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="b2257-113">In questo esempio, frontendSubnet ha la notazione CIDR 10.0.1.0/24 e fa riferimento a un gruppo di sicurezza di rete che consente l'accesso RDP.</span><span class="sxs-lookup"><span data-stu-id="b2257-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="b2257-114">BackendSubnet ha la notazione CIDR 10.0.2.0/24 e fa riferimento allo stesso gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="b2257-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="b2257-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2257-115">PARAMETERS</span></span>

### <span data-ttu-id="b2257-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b2257-116">-AddressPrefix</span></span>
<span data-ttu-id="b2257-117">Specifica un intervallo di indirizzi IP per una configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="b2257-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="b2257-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2257-118">-DefaultProfile</span></span>
<span data-ttu-id="b2257-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2257-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2257-120">-Delega</span><span class="sxs-lookup"><span data-stu-id="b2257-120">-Delegation</span></span>
<span data-ttu-id="b2257-121">Elenco di servizi che dispongono delle autorizzazioni per eseguire operazioni in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="b2257-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="b2257-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2257-122">-InputObject</span></span>
<span data-ttu-id="b2257-123">Specifica il gateway NAT associato alla configurazione della subnet</span><span class="sxs-lookup"><span data-stu-id="b2257-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="b2257-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2257-124">-Name</span></span>
<span data-ttu-id="b2257-125">Specifica il nome della configurazione della subnet da creare.</span><span class="sxs-lookup"><span data-stu-id="b2257-125">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="b2257-126">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b2257-126">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b2257-127">Specifica un oggetto NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="b2257-127">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="b2257-128">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b2257-128">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="b2257-129">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="b2257-129">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="b2257-130">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="b2257-130">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="b2257-131">Configurare per abilitare o disabilitare l'applicazione di criteri di rete nell'endpoint privato nella subnet.</span><span class="sxs-lookup"><span data-stu-id="b2257-131">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="b2257-132">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="b2257-132">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="b2257-133">Configurare per abilitare o disabilitare l'applicazione di criteri di rete sul servizio di collegamento privato nella subnet.</span><span class="sxs-lookup"><span data-stu-id="b2257-133">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="b2257-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2257-134">-ResourceId</span></span>
<span data-ttu-id="b2257-135">Specifica l'ID della risorsa gateway NAT associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="b2257-135">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="b2257-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="b2257-136">-RouteTable</span></span>
<span data-ttu-id="b2257-137">Specifica la tabella route associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="b2257-137">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="b2257-138">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="b2257-138">-RouteTableId</span></span>
<span data-ttu-id="b2257-139">Specifica l'ID della tabella route associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="b2257-139">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="b2257-140">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b2257-140">-ServiceEndpoint</span></span>
<span data-ttu-id="b2257-141">Valore endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="b2257-141">Service Endpoint Value</span></span>

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

### <span data-ttu-id="b2257-142">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b2257-142">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="b2257-143">Criteri endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="b2257-143">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="b2257-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2257-144">CommonParameters</span></span>
<span data-ttu-id="b2257-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2257-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2257-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2257-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2257-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2257-147">INPUTS</span></span>

### <span data-ttu-id="b2257-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b2257-148">System.String</span></span>

### <span data-ttu-id="b2257-149">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b2257-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="b2257-150">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b2257-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="b2257-151">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="b2257-151">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="b2257-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="b2257-152">System.String[]</span></span>

### <span data-ttu-id="b2257-153">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="b2257-153">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="b2257-154">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="b2257-154">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="b2257-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2257-155">OUTPUTS</span></span>

### <span data-ttu-id="b2257-156">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b2257-156">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="b2257-157">Note</span><span class="sxs-lookup"><span data-stu-id="b2257-157">NOTES</span></span>

## <span data-ttu-id="b2257-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2257-158">RELATED LINKS</span></span>

[<span data-ttu-id="b2257-159">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b2257-159">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b2257-160">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b2257-160">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b2257-161">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b2257-161">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b2257-162">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b2257-162">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
