---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4e0356f738bcc0abd52f0ec72c4c6766af8be550
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677908"
---
# <span data-ttu-id="3ccb6-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3ccb6-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="3ccb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ccb6-102">SYNOPSIS</span></span>
<span data-ttu-id="3ccb6-103">Aggiorna una configurazione della subnet per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="3ccb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ccb6-104">SYNTAX</span></span>

### <span data-ttu-id="3ccb6-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3ccb6-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ccb6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ccb6-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ccb6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ccb6-107">DESCRIPTION</span></span>
<span data-ttu-id="3ccb6-108">Il cmdlet **set-AzVirtualNetworkSubnetConfig** aggiorna una configurazione della subnet per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="3ccb6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ccb6-109">EXAMPLES</span></span>

### <span data-ttu-id="3ccb6-110">1: modificare il prefisso dell'indirizzo di una subnet</span><span class="sxs-lookup"><span data-stu-id="3ccb6-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="3ccb6-111">Questo esempio crea una rete virtuale con una subnet.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="3ccb6-112">Chiama quindi Set-AzVirtualNetworkSubnetConfig per modificare il AddressPrefix della subnet.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="3ccb6-113">Questo ha un impatto solo sulla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="3ccb6-114">Set-AzVirtualNetwork viene quindi chiamato per modificare la rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="3ccb6-115">2: aggiungere un gruppo di sicurezza di rete a una subnet</span><span class="sxs-lookup"><span data-stu-id="3ccb6-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="3ccb6-116">Questo esempio crea un gruppo di risorse con una rete virtuale che contiene una sola subnet.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="3ccb6-117">Viene quindi creato un gruppo di sicurezza di rete con una regola Allow per il traffico RDP.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="3ccb6-118">Il cmdlet Set-AzVirtualNetworkSubnetConfig viene usato per modificare la rappresentazione in memoria della subnet frontend in modo che punti al gruppo di sicurezza di rete appena creato.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="3ccb6-119">Il cmdlet Set-AzVirtualNetwork viene quindi chiamato per scrivere di nuovo lo stato modificato nel servizio.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="3ccb6-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ccb6-120">PARAMETERS</span></span>

### <span data-ttu-id="3ccb6-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3ccb6-121">-AddressPrefix</span></span>
<span data-ttu-id="3ccb6-122">Specifica un intervallo di indirizzi IP per una configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="3ccb6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ccb6-123">-DefaultProfile</span></span>
<span data-ttu-id="3ccb6-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ccb6-125">-Delega</span><span class="sxs-lookup"><span data-stu-id="3ccb6-125">-Delegation</span></span>
<span data-ttu-id="3ccb6-126">Elenco di servizi che dispongono delle autorizzazioni per eseguire operazioni in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="3ccb6-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ccb6-127">-Name</span></span>
<span data-ttu-id="3ccb6-128">Specifica il nome di una configurazione della subnet configurata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-128">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="3ccb6-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3ccb6-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="3ccb6-130">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="3ccb6-130">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="3ccb6-131">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3ccb6-131">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="3ccb6-132">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-132">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="3ccb6-133">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="3ccb6-133">-RouteTable</span></span>
<span data-ttu-id="3ccb6-134">Specifica l'oggetto tabella route associato al gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-134">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="3ccb6-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="3ccb6-135">-RouteTableId</span></span>
<span data-ttu-id="3ccb6-136">Specifica l'ID dell'oggetto tabella route associato al gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-136">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="3ccb6-137">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ccb6-137">-ServiceEndpoint</span></span>
<span data-ttu-id="3ccb6-138">Valore endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="3ccb6-138">Service Endpoint Value</span></span>

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

### <span data-ttu-id="3ccb6-139">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3ccb6-139">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="3ccb6-140">Criteri endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="3ccb6-140">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="3ccb6-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3ccb6-141">-VirtualNetwork</span></span>
<span data-ttu-id="3ccb6-142">Specifica l'oggetto **virtualnetwork** che contiene la configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-142">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="3ccb6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ccb6-143">CommonParameters</span></span>
<span data-ttu-id="3ccb6-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ccb6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ccb6-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ccb6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ccb6-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ccb6-146">INPUTS</span></span>

### <span data-ttu-id="3ccb6-147">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3ccb6-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="3ccb6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3ccb6-148">System.String</span></span>

### <span data-ttu-id="3ccb6-149">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3ccb6-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="3ccb6-150">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ccb6-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="3ccb6-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="3ccb6-151">System.String[]</span></span>

### <span data-ttu-id="3ccb6-152">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="3ccb6-152">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="3ccb6-153">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="3ccb6-153">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="3ccb6-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ccb6-154">OUTPUTS</span></span>

### <span data-ttu-id="3ccb6-155">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3ccb6-155">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="3ccb6-156">Note</span><span class="sxs-lookup"><span data-stu-id="3ccb6-156">NOTES</span></span>

## <span data-ttu-id="3ccb6-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ccb6-157">RELATED LINKS</span></span>

[<span data-ttu-id="3ccb6-158">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3ccb6-158">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="3ccb6-159">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3ccb6-159">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="3ccb6-160">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3ccb6-160">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="3ccb6-161">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3ccb6-161">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)