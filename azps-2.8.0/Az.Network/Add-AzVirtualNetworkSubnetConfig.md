---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: fea7f3f3d24595cdddd9635e73e3073efe5cb867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853858"
---
# <span data-ttu-id="8b009-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8b009-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="8b009-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b009-102">SYNOPSIS</span></span>
<span data-ttu-id="8b009-103">Aggiunge una configurazione subnet a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b009-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="8b009-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b009-104">SYNTAX</span></span>

### <span data-ttu-id="8b009-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b009-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b009-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b009-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b009-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b009-107">DESCRIPTION</span></span>
<span data-ttu-id="8b009-108">Il cmdlet **Add-AzVirtualNetworkSubnetConfig** aggiunge una configurazione di subnet a una rete virtuale di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="8b009-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="8b009-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b009-109">EXAMPLES</span></span>

### <span data-ttu-id="8b009-110">1: aggiungere una subnet a una rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="8b009-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="8b009-111">Questo esempio crea prima di tutto un gruppo di risorse come contenitore delle risorse da creare.</span><span class="sxs-lookup"><span data-stu-id="8b009-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="8b009-112">Crea quindi una configurazione della subnet e la usa per creare una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b009-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="8b009-113">Il Add-AzVirtualNetworkSubnetConfig viene quindi usato per aggiungere una subnet alla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b009-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="8b009-114">Il comando Set-AzVirtualNetwork aggiorna la rete virtuale esistente con la nuova subnet.</span><span class="sxs-lookup"><span data-stu-id="8b009-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="8b009-115">2: aggiungere una delega a una subnet aggiunta a una rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="8b009-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="8b009-116">Questo esempio ottiene prima un VNET esistente.</span><span class="sxs-lookup"><span data-stu-id="8b009-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="8b009-117">Crea quindi un oggetto delega in memoria.</span><span class="sxs-lookup"><span data-stu-id="8b009-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="8b009-118">Infine, crea una nuova subnet con la delega aggiunta a vnet.</span><span class="sxs-lookup"><span data-stu-id="8b009-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="8b009-119">La configurazione modificata viene quindi inviata al server.</span><span class="sxs-lookup"><span data-stu-id="8b009-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="8b009-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b009-120">PARAMETERS</span></span>

### <span data-ttu-id="8b009-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8b009-121">-AddressPrefix</span></span>
<span data-ttu-id="8b009-122">Specifica un intervallo di indirizzi IP per una configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="8b009-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="8b009-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b009-123">-DefaultProfile</span></span>
<span data-ttu-id="8b009-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b009-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b009-125">-Delega</span><span class="sxs-lookup"><span data-stu-id="8b009-125">-Delegation</span></span>
<span data-ttu-id="8b009-126">Elenco di servizi che dispongono delle autorizzazioni per eseguire operazioni in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="8b009-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="8b009-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b009-127">-InputObject</span></span>
<span data-ttu-id="8b009-128">Specifica il gateway NAT associato alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="8b009-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="8b009-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b009-129">-Name</span></span>
<span data-ttu-id="8b009-130">Specifica il nome della configurazione della subnet da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="8b009-130">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="8b009-131">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8b009-131">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8b009-132">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="8b009-132">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="8b009-133">Questo cmdlet aggiunge una configurazione di subnet della rete virtuale all'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8b009-133">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b009-134">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8b009-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="8b009-135">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="8b009-135">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="8b009-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="8b009-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="8b009-137">Configurare per abilitare o disabilitare l'applicazione di criteri di rete nell'endpoint privato nella subnet.</span><span class="sxs-lookup"><span data-stu-id="8b009-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="8b009-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="8b009-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="8b009-139">Configurare per abilitare o disabilitare l'applicazione di criteri di rete sul servizio di collegamento privato nella subnet.</span><span class="sxs-lookup"><span data-stu-id="8b009-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="8b009-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b009-140">-ResourceId</span></span>
<span data-ttu-id="8b009-141">Specifica l'ID della risorsa gateway NAT associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="8b009-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="8b009-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="8b009-142">-RouteTable</span></span>
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

### <span data-ttu-id="8b009-143">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="8b009-143">-RouteTableId</span></span>
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

### <span data-ttu-id="8b009-144">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b009-144">-ServiceEndpoint</span></span>
<span data-ttu-id="8b009-145">Valore endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="8b009-145">Service Endpoint Value</span></span>

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

### <span data-ttu-id="8b009-146">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8b009-146">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="8b009-147">Criteri endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="8b009-147">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="8b009-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8b009-148">-VirtualNetwork</span></span>
<span data-ttu-id="8b009-149">Specifica l'oggetto **virtualnetwork** in cui aggiungere una configurazione di subnet.</span><span class="sxs-lookup"><span data-stu-id="8b009-149">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="8b009-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b009-150">CommonParameters</span></span>
<span data-ttu-id="8b009-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b009-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b009-152">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b009-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b009-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b009-153">INPUTS</span></span>

### <span data-ttu-id="8b009-154">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8b009-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="8b009-155">System. String</span><span class="sxs-lookup"><span data-stu-id="8b009-155">System.String</span></span>

### <span data-ttu-id="8b009-156">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8b009-156">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="8b009-157">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="8b009-157">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="8b009-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="8b009-158">System.String[]</span></span>

### <span data-ttu-id="8b009-159">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="8b009-159">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="8b009-160">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="8b009-160">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="8b009-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b009-161">OUTPUTS</span></span>

### <span data-ttu-id="8b009-162">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8b009-162">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="8b009-163">Note</span><span class="sxs-lookup"><span data-stu-id="8b009-163">NOTES</span></span>

## <span data-ttu-id="8b009-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b009-164">RELATED LINKS</span></span>

[<span data-ttu-id="8b009-165">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8b009-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8b009-166">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8b009-166">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8b009-167">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8b009-167">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8b009-168">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8b009-168">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
