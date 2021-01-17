---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c3d01639d428820578ffe8a319bddd591c007e00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475122"
---
# <span data-ttu-id="e7ee0-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e7ee0-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="e7ee0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ee0-103">Aggiunge una configurazione subnet a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="e7ee0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7ee0-104">SYNTAX</span></span>

### <span data-ttu-id="e7ee0-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e7ee0-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ee0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ee0-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7ee0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7ee0-107">DESCRIPTION</span></span>
<span data-ttu-id="e7ee0-108">Il cmdlet **Add-AzVirtualNetworkSubnetConfig** aggiunge una configurazione di subnet a una rete virtuale di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="e7ee0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7ee0-109">EXAMPLES</span></span>

### <span data-ttu-id="e7ee0-110">Esempio 1: aggiungere una subnet a una rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="e7ee0-110">Example 1: Add a subnet to an existing virtual network</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="e7ee0-111">Questo esempio crea prima di tutto un gruppo di risorse come contenitore delle risorse da creare.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="e7ee0-112">Crea quindi una configurazione della subnet e la usa per creare una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="e7ee0-113">Il Add-AzVirtualNetworkSubnetConfig viene quindi usato per aggiungere una subnet alla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="e7ee0-114">Il comando Set-AzVirtualNetwork aggiorna la rete virtuale esistente con la nuova subnet.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="e7ee0-115">Esempio 2: aggiungere una delega a una subnet aggiunta a una rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="e7ee0-115">Example 2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="e7ee0-116">Questo esempio ottiene prima un VNET esistente.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="e7ee0-117">Crea quindi un oggetto delega in memoria.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="e7ee0-118">Infine, crea una nuova subnet con la delega aggiunta a vnet.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="e7ee0-119">La configurazione modificata viene quindi inviata al server.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="e7ee0-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7ee0-120">PARAMETERS</span></span>

### <span data-ttu-id="e7ee0-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e7ee0-121">-AddressPrefix</span></span>
<span data-ttu-id="e7ee0-122">Specifica un intervallo di indirizzi IP per una configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="e7ee0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ee0-123">-DefaultProfile</span></span>
<span data-ttu-id="e7ee0-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7ee0-125">-Delega</span><span class="sxs-lookup"><span data-stu-id="e7ee0-125">-Delegation</span></span>
<span data-ttu-id="e7ee0-126">Elenco di servizi che dispongono delle autorizzazioni per eseguire operazioni in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="e7ee0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7ee0-127">-InputObject</span></span>
<span data-ttu-id="e7ee0-128">Specifica il gateway NAT associato alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="e7ee0-129">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="e7ee0-129">-IpAllocation</span></span>
<span data-ttu-id="e7ee0-130">Specifica IpAllocations per una subnet.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-130">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="e7ee0-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7ee0-131">-Name</span></span>
<span data-ttu-id="e7ee0-132">Specifica il nome della configurazione della subnet da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-132">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="e7ee0-133">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7ee0-133">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e7ee0-134">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="e7ee0-134">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="e7ee0-135">Questo cmdlet aggiunge una configurazione di subnet della rete virtuale all'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-135">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="e7ee0-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e7ee0-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e7ee0-137">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="e7ee0-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="e7ee0-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="e7ee0-139">Configurare per abilitare o disabilitare l'applicazione di criteri di rete nell'endpoint privato nella subnet.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="e7ee0-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="e7ee0-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="e7ee0-141">Configurare per abilitare o disabilitare l'applicazione di criteri di rete sul servizio di collegamento privato nella subnet.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="e7ee0-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ee0-142">-ResourceId</span></span>
<span data-ttu-id="e7ee0-143">Specifica l'ID della risorsa gateway NAT associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="e7ee0-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e7ee0-144">-RouteTable</span></span>
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

### <span data-ttu-id="e7ee0-145">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="e7ee0-145">-RouteTableId</span></span>
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

### <span data-ttu-id="e7ee0-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7ee0-146">-ServiceEndpoint</span></span>
<span data-ttu-id="e7ee0-147">Valore endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="e7ee0-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="e7ee0-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e7ee0-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e7ee0-149">Criteri endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="e7ee0-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="e7ee0-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e7ee0-150">-VirtualNetwork</span></span>
<span data-ttu-id="e7ee0-151">Specifica l'oggetto **virtualnetwork** in cui aggiungere una configurazione di subnet.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-151">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="e7ee0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ee0-152">CommonParameters</span></span>
<span data-ttu-id="e7ee0-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ee0-154">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7ee0-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ee0-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7ee0-155">INPUTS</span></span>

### <span data-ttu-id="e7ee0-156">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e7ee0-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="e7ee0-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e7ee0-157">System.String</span></span>

### <span data-ttu-id="e7ee0-158">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7ee0-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="e7ee0-159">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e7ee0-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="e7ee0-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="e7ee0-160">System.String[]</span></span>

### <span data-ttu-id="e7ee0-161">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="e7ee0-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="e7ee0-162">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="e7ee0-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="e7ee0-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7ee0-163">OUTPUTS</span></span>

### <span data-ttu-id="e7ee0-164">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e7ee0-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e7ee0-165">Note</span><span class="sxs-lookup"><span data-stu-id="e7ee0-165">NOTES</span></span>

## <span data-ttu-id="e7ee0-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7ee0-166">RELATED LINKS</span></span>

[<span data-ttu-id="e7ee0-167">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e7ee0-167">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e7ee0-168">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e7ee0-168">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e7ee0-169">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e7ee0-169">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e7ee0-170">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e7ee0-170">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
