---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4c206bfe4681bfdc1cb622ec90170776e5528ebe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979726"
---
# <span data-ttu-id="fd5b5-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fd5b5-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="fd5b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd5b5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd5b5-103">Aggiunge una configurazione subnet a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="fd5b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd5b5-104">SYNTAX</span></span>

### <span data-ttu-id="fd5b5-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="fd5b5-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd5b5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd5b5-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd5b5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fd5b5-107">DESCRIPTION</span></span>
<span data-ttu-id="fd5b5-108">Il cmdlet **Add-AzVirtualNetworkSubnetConfig aggiunge** una configurazione subnet a una rete virtuale di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="fd5b5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd5b5-109">EXAMPLES</span></span>

### <span data-ttu-id="fd5b5-110">Esempio 1: Aggiungere una subnet a una rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="fd5b5-110">Example 1: Add a subnet to an existing virtual network</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="fd5b5-111">Questo esempio crea prima di tutto un gruppo di risorse come contenitore delle risorse da creare.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="fd5b5-112">Crea quindi una configurazione della subnet e la usa per creare una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="fd5b5-113">Il Add-AzVirtualNetworkSubnetConfig viene quindi usato per aggiungere una subnet alla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="fd5b5-114">Il Set-AzVirtualNetwork aggiorna la rete virtuale esistente con la nuova subnet.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="fd5b5-115">Esempio 2: Aggiungere una delega a una subnet aggiunta a una rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="fd5b5-115">Example 2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="fd5b5-116">Questo esempio ottiene prima una vnet esistente.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="fd5b5-117">Crea quindi un oggetto di delega in memoria.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="fd5b5-118">Infine, crea una nuova subnet con la delega aggiunta alla vnet.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="fd5b5-119">La configurazione modificata viene quindi inviata al server.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="fd5b5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd5b5-120">PARAMETERS</span></span>

### <span data-ttu-id="fd5b5-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fd5b5-121">-AddressPrefix</span></span>
<span data-ttu-id="fd5b5-122">Specifica un intervallo di indirizzi IP per la configurazione di una subnet.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="fd5b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd5b5-123">-DefaultProfile</span></span>
<span data-ttu-id="fd5b5-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd5b5-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="fd5b5-125">-Delegation</span></span>
<span data-ttu-id="fd5b5-126">Elenco dei servizi autorizzati a eseguire operazioni nella subnet.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="fd5b5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd5b5-127">-InputObject</span></span>
<span data-ttu-id="fd5b5-128">Specifica il gateway NAT associato alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="fd5b5-129">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="fd5b5-129">-IpAllocation</span></span>
<span data-ttu-id="fd5b5-130">Specifica IpAllocations per una subnet.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-130">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="fd5b5-131">-Name</span><span class="sxs-lookup"><span data-stu-id="fd5b5-131">-Name</span></span>
<span data-ttu-id="fd5b5-132">Specifica il nome della configurazione della subnet da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-132">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="fd5b5-133">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fd5b5-133">-NetworkSecurityGroup</span></span>
<span data-ttu-id="fd5b5-134">Specifica un **oggetto NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="fd5b5-134">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="fd5b5-135">Questo cmdlet aggiunge una configurazione subnet della rete virtuale all'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-135">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="fd5b5-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="fd5b5-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="fd5b5-137">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="fd5b5-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="fd5b5-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="fd5b5-139">Configura per abilitare o disabilitare l'applicazione di criteri di rete nell'endpoint privato nella subnet.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="fd5b5-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="fd5b5-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="fd5b5-141">Configurare per abilitare o disabilitare l'applicazione di criteri di rete nel servizio di collegamento privato nella subnet.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="fd5b5-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd5b5-142">-ResourceId</span></span>
<span data-ttu-id="fd5b5-143">Specifica l'ID della risorsa Gateway NAT associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="fd5b5-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="fd5b5-144">-RouteTable</span></span>
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

### <span data-ttu-id="fd5b5-145">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="fd5b5-145">-RouteTableId</span></span>
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

### <span data-ttu-id="fd5b5-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="fd5b5-146">-ServiceEndpoint</span></span>
<span data-ttu-id="fd5b5-147">Valore endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="fd5b5-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="fd5b5-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fd5b5-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="fd5b5-149">Criteri endpoint di servizio</span><span class="sxs-lookup"><span data-stu-id="fd5b5-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="fd5b5-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fd5b5-150">-VirtualNetwork</span></span>
<span data-ttu-id="fd5b5-151">Specifica **l'oggetto VirtualNetwork** in cui aggiungere una configurazione subnet.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-151">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="fd5b5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd5b5-152">CommonParameters</span></span>
<span data-ttu-id="fd5b5-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd5b5-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fd5b5-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd5b5-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="fd5b5-155">INPUTS</span></span>

### <span data-ttu-id="fd5b5-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fd5b5-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="fd5b5-157">System.String</span><span class="sxs-lookup"><span data-stu-id="fd5b5-157">System.String</span></span>

### <span data-ttu-id="fd5b5-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fd5b5-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="fd5b5-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="fd5b5-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="fd5b5-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="fd5b5-160">System.String[]</span></span>

### <span data-ttu-id="fd5b5-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="fd5b5-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="fd5b5-162">Microsoft.Azure.Commands.Network.Models.PSDelegamento[]</span><span class="sxs-lookup"><span data-stu-id="fd5b5-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="fd5b5-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd5b5-163">OUTPUTS</span></span>

### <span data-ttu-id="fd5b5-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fd5b5-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="fd5b5-165">NOTE</span><span class="sxs-lookup"><span data-stu-id="fd5b5-165">NOTES</span></span>

## <span data-ttu-id="fd5b5-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd5b5-166">RELATED LINKS</span></span>

[<span data-ttu-id="fd5b5-167">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fd5b5-167">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="fd5b5-168">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fd5b5-168">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="fd5b5-169">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fd5b5-169">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="fd5b5-170">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fd5b5-170">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
