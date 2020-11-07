---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 73649f0f04cf1de07d991cb454b44308c4ff6443
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862705"
---
# <span data-ttu-id="49667-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="49667-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="49667-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49667-102">SYNOPSIS</span></span>
<span data-ttu-id="49667-103">Configura lo stato dell'obiettivo per una configurazione della subnet in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="49667-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

## <span data-ttu-id="49667-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49667-104">SYNTAX</span></span>

### <span data-ttu-id="49667-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="49667-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49667-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="49667-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49667-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49667-107">DESCRIPTION</span></span>
<span data-ttu-id="49667-108">Il cmdlet **set-AzVirtualNetworkSubnetConfig** configura lo stato dell'obiettivo per una configurazione della subnet in una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="49667-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="49667-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49667-109">EXAMPLES</span></span>

### <span data-ttu-id="49667-110">1: modificare il prefisso dell'indirizzo di una subnet</span><span class="sxs-lookup"><span data-stu-id="49667-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="49667-111">Questo esempio crea una rete virtuale con una subnet.</span><span class="sxs-lookup"><span data-stu-id="49667-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="49667-112">Chiama quindi Set-AzVirtualNetworkSubnetConfig per modificare il AddressPrefix della subnet.</span><span class="sxs-lookup"><span data-stu-id="49667-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="49667-113">Questo ha un impatto solo sulla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="49667-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="49667-114">Set-AzVirtualNetwork viene quindi chiamato per modificare la rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="49667-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="49667-115">2: aggiungere un gruppo di sicurezza di rete a una subnet</span><span class="sxs-lookup"><span data-stu-id="49667-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="49667-116">Questo esempio crea un gruppo di risorse con una rete virtuale che contiene una sola subnet.</span><span class="sxs-lookup"><span data-stu-id="49667-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="49667-117">Viene quindi creato un gruppo di sicurezza di rete con una regola Allow per il traffico RDP.</span><span class="sxs-lookup"><span data-stu-id="49667-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="49667-118">Il cmdlet Set-AzVirtualNetworkSubnetConfig viene usato per modificare la rappresentazione in memoria della subnet frontend in modo che punti al gruppo di sicurezza di rete appena creato.</span><span class="sxs-lookup"><span data-stu-id="49667-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="49667-119">Il cmdlet Set-AzVirtualNetwork viene quindi chiamato per scrivere di nuovo lo stato modificato nel servizio.</span><span class="sxs-lookup"><span data-stu-id="49667-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="49667-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49667-120">PARAMETERS</span></span>

### <span data-ttu-id="49667-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="49667-121">-AddressPrefix</span></span>
<span data-ttu-id="49667-122">Specifica un intervallo di indirizzi IP per una configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="49667-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="49667-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49667-123">-DefaultProfile</span></span>
<span data-ttu-id="49667-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49667-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49667-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="49667-125">-Name</span></span>
<span data-ttu-id="49667-126">Specifica il nome di una configurazione della subnet configurata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49667-126">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="49667-127">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49667-127">-NetworkSecurityGroup</span></span>
<span data-ttu-id="49667-128">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="49667-128">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49667-129">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="49667-129">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="49667-130">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="49667-130">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49667-131">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="49667-131">-RouteTable</span></span>
<span data-ttu-id="49667-132">Specifica l'oggetto tabella route associato al gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="49667-132">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49667-133">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="49667-133">-RouteTableId</span></span>
<span data-ttu-id="49667-134">Specifica l'ID dell'oggetto tabella route associato al gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="49667-134">Specifies the ID of the route table object that is associated with the network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49667-135">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="49667-135">-ServiceEndpoint</span></span>
<span data-ttu-id="49667-136">Valore endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="49667-136">Service Endpoint Value</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49667-137">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="49667-137">-VirtualNetwork</span></span>
<span data-ttu-id="49667-138">Specifica l'oggetto **virtualnetwork** che contiene la configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="49667-138">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49667-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49667-139">CommonParameters</span></span>
<span data-ttu-id="49667-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49667-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49667-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49667-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49667-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49667-142">INPUTS</span></span>

### <span data-ttu-id="49667-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="49667-143">PSVirtualNetwork</span></span>
<span data-ttu-id="49667-144">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="49667-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="49667-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49667-145">OUTPUTS</span></span>

### <span data-ttu-id="49667-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="49667-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="49667-147">Note</span><span class="sxs-lookup"><span data-stu-id="49667-147">NOTES</span></span>

## <span data-ttu-id="49667-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49667-148">RELATED LINKS</span></span>

[<span data-ttu-id="49667-149">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="49667-149">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="49667-150">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="49667-150">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="49667-151">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="49667-151">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="49667-152">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="49667-152">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)


