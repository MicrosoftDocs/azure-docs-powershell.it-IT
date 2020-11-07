---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: 9f1f4f916ea0756ebf034c12e1e9f92f3cd3c865
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867073"
---
# <span data-ttu-id="4821f-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4821f-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="4821f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4821f-102">SYNOPSIS</span></span>
<span data-ttu-id="4821f-103">Aggiunge una configurazione subnet a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4821f-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4821f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4821f-104">SYNTAX</span></span>

### <span data-ttu-id="4821f-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4821f-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4821f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4821f-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4821f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4821f-107">DESCRIPTION</span></span>
<span data-ttu-id="4821f-108">Il cmdlet **Add-AzureRmVirtualNetworkSubnetConfig** aggiunge una configurazione di subnet a una rete virtuale di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="4821f-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="4821f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4821f-109">EXAMPLES</span></span>

### <span data-ttu-id="4821f-110">1: aggiungere una subnet a una rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="4821f-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="4821f-111">Questo esempio crea prima di tutto un gruppo di risorse come contenitore delle risorse da creare.</span><span class="sxs-lookup"><span data-stu-id="4821f-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="4821f-112">Crea quindi una configurazione della subnet e la usa per creare una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4821f-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="4821f-113">Il Add-AzureRmVirtualNetworkSubnetConfig viene quindi usato per aggiungere una subnet alla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4821f-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="4821f-114">Il comando Set-AzureRmVirtualNetwork aggiorna la rete virtuale esistente con la nuova subnet.</span><span class="sxs-lookup"><span data-stu-id="4821f-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="4821f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4821f-115">PARAMETERS</span></span>

### <span data-ttu-id="4821f-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4821f-116">-AddressPrefix</span></span>
<span data-ttu-id="4821f-117">Specifica un intervallo di indirizzi IP per una configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="4821f-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="4821f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4821f-118">-DefaultProfile</span></span>
<span data-ttu-id="4821f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4821f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4821f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4821f-120">-Name</span></span>
<span data-ttu-id="4821f-121">Specifica il nome della configurazione della subnet da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="4821f-121">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="4821f-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4821f-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="4821f-123">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="4821f-123">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="4821f-124">Questo cmdlet aggiunge una configurazione di subnet della rete virtuale all'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4821f-124">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="4821f-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4821f-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="4821f-126">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="4821f-126">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="4821f-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4821f-127">-RouteTable</span></span>
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

### <span data-ttu-id="4821f-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="4821f-128">-RouteTableId</span></span>
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

### <span data-ttu-id="4821f-129">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4821f-129">-ServiceEndpoint</span></span>
<span data-ttu-id="4821f-130">Valore endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="4821f-130">Service Endpoint Value</span></span>

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

### <span data-ttu-id="4821f-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4821f-131">-VirtualNetwork</span></span>
<span data-ttu-id="4821f-132">Specifica l'oggetto **virtualnetwork** in cui aggiungere una configurazione di subnet.</span><span class="sxs-lookup"><span data-stu-id="4821f-132">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="4821f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4821f-133">CommonParameters</span></span>
<span data-ttu-id="4821f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4821f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4821f-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4821f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4821f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4821f-136">INPUTS</span></span>

### <span data-ttu-id="4821f-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4821f-137">PSVirtualNetwork</span></span>
<span data-ttu-id="4821f-138">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4821f-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="4821f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4821f-139">OUTPUTS</span></span>

### <span data-ttu-id="4821f-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4821f-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4821f-141">Note</span><span class="sxs-lookup"><span data-stu-id="4821f-141">NOTES</span></span>

## <span data-ttu-id="4821f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4821f-142">RELATED LINKS</span></span>

[<span data-ttu-id="4821f-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4821f-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4821f-144">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4821f-144">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4821f-145">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4821f-145">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4821f-146">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4821f-146">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


