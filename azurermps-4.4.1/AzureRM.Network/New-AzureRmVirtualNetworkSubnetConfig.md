---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4211e39555f98fd21a78085f3f49749da60c2b4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510472"
---
# <span data-ttu-id="29394-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="29394-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="29394-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29394-102">SYNOPSIS</span></span>
<span data-ttu-id="29394-103">Crea una configurazione della subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="29394-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29394-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29394-104">SYNTAX</span></span>

### <span data-ttu-id="29394-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="29394-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29394-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="29394-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29394-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29394-107">DESCRIPTION</span></span>
<span data-ttu-id="29394-108">**Il cmdlet New-AzureRmVirtualNetworkSubnetConfig** crea una configurazione di subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="29394-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="29394-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29394-109">EXAMPLES</span></span>

### <span data-ttu-id="29394-110">1: creare una rete virtuale con due subnet e un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="29394-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
    $networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
    New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="29394-111">Questo esempio crea due nuove configurazioni di subnet usando il cmdlet New-AzureRmVirtualSubnetConfig e le usa per creare una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="29394-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="29394-112">Il modello New-AzureRmVirtualSubnetConfig crea solo una rappresentazione in memoria della subnet.</span><span class="sxs-lookup"><span data-stu-id="29394-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="29394-113">In questo esempio, frontendSubnet ha la notazione CIDR 10.0.1.0/24 e fa riferimento a un gruppo di sicurezza di rete che consente l'accesso RDP.</span><span class="sxs-lookup"><span data-stu-id="29394-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="29394-114">BackendSubnet ha la notazione CIDR 10.0.2.0/24 e fa riferimento allo stesso gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="29394-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="29394-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29394-115">PARAMETERS</span></span>

### <span data-ttu-id="29394-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="29394-116">-AddressPrefix</span></span>
<span data-ttu-id="29394-117">Specifica un intervallo di indirizzi IP per una configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="29394-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="29394-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="29394-118">-Name</span></span>
<span data-ttu-id="29394-119">Specifica il nome della configurazione della subnet da creare.</span><span class="sxs-lookup"><span data-stu-id="29394-119">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="29394-120">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="29394-120">-NetworkSecurityGroup</span></span>
<span data-ttu-id="29394-121">Specifica un oggetto NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="29394-121">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="29394-122">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="29394-122">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="29394-123">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="29394-123">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="29394-124">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="29394-124">-RouteTable</span></span>
<span data-ttu-id="29394-125">Specifica la tabella route associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="29394-125">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="29394-126">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="29394-126">-RouteTableId</span></span>
<span data-ttu-id="29394-127">Specifica l'ID della tabella route associata alla configurazione della subnet.</span><span class="sxs-lookup"><span data-stu-id="29394-127">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="29394-128">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="29394-128">-ServiceEndpoint</span></span>
<span data-ttu-id="29394-129">Valore endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="29394-129">Service Endpoint Value</span></span>

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

### <span data-ttu-id="29394-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29394-130">-DefaultProfile</span></span>
<span data-ttu-id="29394-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29394-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29394-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29394-132">CommonParameters</span></span>
<span data-ttu-id="29394-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29394-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29394-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29394-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29394-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29394-135">INPUTS</span></span>

## <span data-ttu-id="29394-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29394-136">OUTPUTS</span></span>

### <span data-ttu-id="29394-137">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="29394-137">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="29394-138">Note</span><span class="sxs-lookup"><span data-stu-id="29394-138">NOTES</span></span>

## <span data-ttu-id="29394-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29394-139">RELATED LINKS</span></span>

[<span data-ttu-id="29394-140">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="29394-140">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="29394-141">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="29394-141">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="29394-142">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="29394-142">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="29394-143">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="29394-143">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


