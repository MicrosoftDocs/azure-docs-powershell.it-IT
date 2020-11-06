---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: eb684d6b51cdbe6d640b8bb91e2bfdd9b5f8c0b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519909"
---
# <span data-ttu-id="c1025-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c1025-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="c1025-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1025-102">SYNOPSIS</span></span>
<span data-ttu-id="c1025-103">Configura lo stato dell'obiettivo per una configurazione della subnet in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1025-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1025-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1025-104">SYNTAX</span></span>

### <span data-ttu-id="c1025-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1025-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1025-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1025-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1025-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1025-107">DESCRIPTION</span></span>
<span data-ttu-id="c1025-108">Il cmdlet **set-AzureRmVirtualNetworkSubnetConfig** configura lo stato dell'obiettivo per una configurazione della subnet in una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="c1025-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="c1025-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1025-109">EXAMPLES</span></span>

### <span data-ttu-id="c1025-110">1: modificare il prefisso dell'indirizzo di una subnet</span><span class="sxs-lookup"><span data-stu-id="c1025-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="c1025-111">Questo esempio crea una rete virtuale con una subnet.</span><span class="sxs-lookup"><span data-stu-id="c1025-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="c1025-112">Chiama quindi Set-AzureRmVirtualNetworkSubnetConfig per modificare il AddressPrefix della subnet.</span><span class="sxs-lookup"><span data-stu-id="c1025-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="c1025-113">Questo ha un impatto solo sulla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1025-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="c1025-114">Set-AzureRmVirtualNetwork viene quindi chiamato per modificare la rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="c1025-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="c1025-115">2: aggiungere un gruppo di sicurezza di rete a una subnet</span><span class="sxs-lookup"><span data-stu-id="c1025-115">2: Add a network security group to a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="c1025-116">Questo esempio crea un gruppo di risorse con una rete virtuale che contiene una sola subnet.</span><span class="sxs-lookup"><span data-stu-id="c1025-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="c1025-117">Viene quindi creato un gruppo di sicurezza di rete con una regola Allow per il traffico RDP.</span><span class="sxs-lookup"><span data-stu-id="c1025-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="c1025-118">Il cmdlet Set-AzureRmVirtualNetworkSubnetConfig viene usato per modificare la rappresentazione in memoria della subnet frontend in modo che punti al gruppo di sicurezza di rete appena creato.</span><span class="sxs-lookup"><span data-stu-id="c1025-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="c1025-119">Il cmdlet Set-AzureRmVirtualNetwork viene quindi chiamato per scrivere di nuovo lo stato modificato nel servizio.</span><span class="sxs-lookup"><span data-stu-id="c1025-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="c1025-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1025-120">PARAMETERS</span></span>

### <span data-ttu-id="c1025-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c1025-121">-AddressPrefix</span></span>
<span data-ttu-id="c1025-122">Specifica un intervallo di indirizzi IP per una configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="c1025-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="c1025-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1025-123">-DefaultProfile</span></span>
<span data-ttu-id="c1025-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1025-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1025-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1025-125">-Name</span></span>
<span data-ttu-id="c1025-126">Specifica il nome di una configurazione della subnet configurata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1025-126">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="c1025-127">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c1025-127">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c1025-128">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="c1025-128">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="c1025-129">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c1025-129">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="c1025-130">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="c1025-130">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="c1025-131">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c1025-131">-RouteTable</span></span>
<span data-ttu-id="c1025-132">Specifica l'oggetto tabella route associato al gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="c1025-132">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="c1025-133">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="c1025-133">-RouteTableId</span></span>
<span data-ttu-id="c1025-134">Specifica l'ID dell'oggetto tabella route associato al gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="c1025-134">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="c1025-135">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1025-135">-ServiceEndpoint</span></span>
<span data-ttu-id="c1025-136">Valore endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="c1025-136">Service Endpoint Value</span></span>

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

### <span data-ttu-id="c1025-137">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c1025-137">-VirtualNetwork</span></span>
<span data-ttu-id="c1025-138">Specifica l'oggetto **virtualnetwork** che contiene la configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="c1025-138">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="c1025-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1025-139">CommonParameters</span></span>
<span data-ttu-id="c1025-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1025-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1025-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1025-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1025-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1025-142">INPUTS</span></span>

### <span data-ttu-id="c1025-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c1025-143">PSVirtualNetwork</span></span>
<span data-ttu-id="c1025-144">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c1025-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="c1025-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1025-145">OUTPUTS</span></span>

### <span data-ttu-id="c1025-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c1025-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c1025-147">Note</span><span class="sxs-lookup"><span data-stu-id="c1025-147">NOTES</span></span>

## <span data-ttu-id="c1025-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1025-148">RELATED LINKS</span></span>

[<span data-ttu-id="c1025-149">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c1025-149">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c1025-150">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c1025-150">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c1025-151">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c1025-151">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c1025-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c1025-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


