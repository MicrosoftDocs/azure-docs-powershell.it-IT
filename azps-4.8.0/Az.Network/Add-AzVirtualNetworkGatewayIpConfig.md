---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: f8de9ce0aab60aad729d990c233acfaf75ae50b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191007"
---
# <span data-ttu-id="ed27c-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed27c-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="ed27c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed27c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed27c-103">Aggiunge una configurazione IP a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ed27c-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="ed27c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed27c-104">SYNTAX</span></span>

### <span data-ttu-id="ed27c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed27c-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed27c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ed27c-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed27c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed27c-107">DESCRIPTION</span></span>
<span data-ttu-id="ed27c-108">Il cmdlet **Add-AzVirtualNetworkGatewayIpConfig** aggiunge una configurazione IP a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ed27c-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="ed27c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed27c-109">EXAMPLES</span></span>

### <span data-ttu-id="ed27c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed27c-110">Example 1</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gw -Name GWIPConfig2 -Subnet $subnet -PublicIpAddress $gwpip2


Name                   : VNet7GW
ResourceGroupName      : VPNGatewayV3
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW
Etag                   : W/"d27a784f-3c3f-4150-863d-764649b6e8e7"
ResourceGuid           : 3c2478a7-d5d4-4e80-8532-7ea2ad577598
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworks/Vnet7/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/VNet7GW_IP"
                             },
                             "Name": "default",
                             "Etag": "W/\"d27a784f-3c3f-4150-863d-764649b6e8e7\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW/ipConfigurations/default"
                           },
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/delIPConfig"
                             },
                             "Name": "GWIPConfig2",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupNotSet/providers/Microsoft.Network/virtualNetworkGateways/VirtualNetworkGatewayNameNotSet/virtualNetworkGatewayIpConfiguration/GWIPConfig2"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : True
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65534,
                           "BgpPeeringAddress": "10.7.255.254",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="ed27c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed27c-111">PARAMETERS</span></span>

### <span data-ttu-id="ed27c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed27c-112">-DefaultProfile</span></span>
<span data-ttu-id="ed27c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed27c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed27c-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed27c-114">-Name</span></span>
<span data-ttu-id="ed27c-115">Specifica il nome della configurazione IP del gateway da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="ed27c-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="ed27c-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="ed27c-116">-PrivateIpAddress</span></span>
<span data-ttu-id="ed27c-117">Specifica l'indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="ed27c-117">Specifies the private IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed27c-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ed27c-118">-PublicIpAddress</span></span>
<span data-ttu-id="ed27c-119">Specifica l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ed27c-119">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed27c-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="ed27c-120">-PublicIpAddressId</span></span>
<span data-ttu-id="ed27c-121">Specifica l'ID dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ed27c-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed27c-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="ed27c-122">-Subnet</span></span>
<span data-ttu-id="ed27c-123">Specifica un oggetto **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="ed27c-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed27c-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ed27c-124">-SubnetId</span></span>
<span data-ttu-id="ed27c-125">Specifica l'ID della subnet.</span><span class="sxs-lookup"><span data-stu-id="ed27c-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed27c-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed27c-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="ed27c-127">Specifica un oggetto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="ed27c-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="ed27c-128">Questo cmdlet modifica l'oggetto **PSVirtualNetworkGateway** specificato.</span><span class="sxs-lookup"><span data-stu-id="ed27c-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="ed27c-129">Puoi usare il cmdlet Get-AzVirtualNetworkGateway per recuperare un oggetto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="ed27c-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed27c-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed27c-130">-Confirm</span></span>
<span data-ttu-id="ed27c-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed27c-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed27c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed27c-132">-WhatIf</span></span>
<span data-ttu-id="ed27c-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed27c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed27c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed27c-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed27c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed27c-135">CommonParameters</span></span>
<span data-ttu-id="ed27c-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed27c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed27c-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed27c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed27c-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed27c-138">INPUTS</span></span>

### <span data-ttu-id="ed27c-139">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed27c-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ed27c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed27c-140">OUTPUTS</span></span>

### <span data-ttu-id="ed27c-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed27c-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ed27c-142">Note</span><span class="sxs-lookup"><span data-stu-id="ed27c-142">NOTES</span></span>

## <span data-ttu-id="ed27c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed27c-143">RELATED LINKS</span></span>

[<span data-ttu-id="ed27c-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed27c-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ed27c-145">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed27c-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="ed27c-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed27c-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
