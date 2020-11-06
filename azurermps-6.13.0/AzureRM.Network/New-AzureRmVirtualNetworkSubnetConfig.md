---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 37202e0e852f0171ce48c2c3d61d13151b05148c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511687"
---
# <span data-ttu-id="dcf38-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dcf38-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="dcf38-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dcf38-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf38-103">Crea una configurazione della subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="dcf38-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcf38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dcf38-104">SYNTAX</span></span>

### <span data-ttu-id="dcf38-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dcf38-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcf38-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dcf38-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcf38-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dcf38-107">DESCRIPTION</span></span>
<span data-ttu-id="dcf38-108">**Il cmdlet New-AzureRmVirtualNetworkSubnetConfig** crea una configurazione di subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="dcf38-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="dcf38-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dcf38-109">EXAMPLES</span></span>

### <span data-ttu-id="dcf38-110">1: creare una rete virtuale con due subnet e un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="dcf38-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="dcf38-111">Questo esempio crea due nuove configurazioni di subnet usando il cmdlet New-AzureRmVirtualSubnetConfig e le usa per creare una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="dcf38-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="dcf38-112">Il modello New-AzureRmVirtualSubnetConfig crea solo una rappresentazione in memoria della subnet.</span><span class="sxs-lookup"><span data-stu-id="dcf38-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="dcf38-113">In questo esempio, frontendSubnet ha la notazione CIDR 10.0.1.0/24 e fa riferimento a un gruppo di sicurezza di rete che consente l'accesso RDP.</span><span class="sxs-lookup"><span data-stu-id="dcf38-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="dcf38-114">BackendSubnet ha la notazione CIDR 10.0.2.0/24 e fa riferimento allo stesso gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="dcf38-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="dcf38-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dcf38-115">PARAMETERS</span></span>

### <span data-ttu-id="dcf38-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="dcf38-116">-AddressPrefix</span></span>
<span data-ttu-id="dcf38-117">Specifica un intervallo di indirizzi IP per una configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="dcf38-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf38-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf38-118">-DefaultProfile</span></span>
<span data-ttu-id="dcf38-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf38-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf38-120">-Delega</span><span class="sxs-lookup"><span data-stu-id="dcf38-120">-Delegation</span></span>
<span data-ttu-id="dcf38-121">Elenco di servizi che dispongono delle autorizzazioni per eseguire operazioni in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="dcf38-121">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf38-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcf38-122">-Name</span></span>
<span data-ttu-id="dcf38-123">Specifica il nome della configurazione della subnet da creare.</span><span class="sxs-lookup"><span data-stu-id="dcf38-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="dcf38-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dcf38-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="dcf38-125">Specifica un oggetto NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="dcf38-125">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="dcf38-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="dcf38-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="dcf38-127">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="dcf38-127">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="dcf38-128">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="dcf38-128">-RouteTable</span></span>
<span data-ttu-id="dcf38-129">Specifica la tabella route associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="dcf38-129">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="dcf38-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="dcf38-130">-RouteTableId</span></span>
<span data-ttu-id="dcf38-131">Specifica l'ID della tabella route associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="dcf38-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="dcf38-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcf38-132">-ServiceEndpoint</span></span>
<span data-ttu-id="dcf38-133">Valore endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="dcf38-133">Service Endpoint Value</span></span>

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

### <span data-ttu-id="dcf38-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="dcf38-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="dcf38-135">Criteri endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="dcf38-135">Service Endpoint Policies</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf38-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf38-136">CommonParameters</span></span>
<span data-ttu-id="dcf38-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf38-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf38-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcf38-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf38-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dcf38-139">INPUTS</span></span>

### <span data-ttu-id="dcf38-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dcf38-140">System.String</span></span>

### <span data-ttu-id="dcf38-141">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dcf38-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="dcf38-142">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="dcf38-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="dcf38-143">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="dcf38-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="dcf38-144">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dcf38-144">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="dcf38-145">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dcf38-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dcf38-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dcf38-146">OUTPUTS</span></span>

### <span data-ttu-id="dcf38-147">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="dcf38-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="dcf38-148">Note</span><span class="sxs-lookup"><span data-stu-id="dcf38-148">NOTES</span></span>

## <span data-ttu-id="dcf38-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dcf38-149">RELATED LINKS</span></span>

[<span data-ttu-id="dcf38-150">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dcf38-150">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dcf38-151">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dcf38-151">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dcf38-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dcf38-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dcf38-153">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dcf38-153">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


