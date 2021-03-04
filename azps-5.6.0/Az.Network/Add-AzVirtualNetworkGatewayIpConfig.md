---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b69945e57572d226957a3cd44edee76c557443ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979741"
---
# <span data-ttu-id="59efa-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="59efa-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="59efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59efa-102">SYNOPSIS</span></span>
<span data-ttu-id="59efa-103">Aggiunge una configurazione IP a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="59efa-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="59efa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59efa-104">SYNTAX</span></span>

### <span data-ttu-id="59efa-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="59efa-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59efa-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="59efa-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59efa-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="59efa-107">DESCRIPTION</span></span>
<span data-ttu-id="59efa-108">Il cmdlet **Add-AzVirtualNetworkGatewayIpConfig aggiunge** una configurazione IP a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="59efa-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="59efa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59efa-109">EXAMPLES</span></span>

### <span data-ttu-id="59efa-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="59efa-110">Example 1</span></span>
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

## <span data-ttu-id="59efa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59efa-111">PARAMETERS</span></span>

### <span data-ttu-id="59efa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59efa-112">-DefaultProfile</span></span>
<span data-ttu-id="59efa-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59efa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59efa-114">-Name</span><span class="sxs-lookup"><span data-stu-id="59efa-114">-Name</span></span>
<span data-ttu-id="59efa-115">Specifica il nome della configurazione IP del gateway da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="59efa-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="59efa-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="59efa-116">-PrivateIpAddress</span></span>
<span data-ttu-id="59efa-117">Specifica l'indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="59efa-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="59efa-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="59efa-118">-PublicIpAddress</span></span>
<span data-ttu-id="59efa-119">Specifica l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="59efa-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="59efa-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="59efa-120">-PublicIpAddressId</span></span>
<span data-ttu-id="59efa-121">Specifica l'ID dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="59efa-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="59efa-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="59efa-122">-Subnet</span></span>
<span data-ttu-id="59efa-123">Specifica un **oggetto PSSubnet.**</span><span class="sxs-lookup"><span data-stu-id="59efa-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="59efa-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="59efa-124">-SubnetId</span></span>
<span data-ttu-id="59efa-125">Specifica l'ID della subnet.</span><span class="sxs-lookup"><span data-stu-id="59efa-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="59efa-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59efa-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="59efa-127">Specifica un **oggetto PSVirtualNetworkGateway.**</span><span class="sxs-lookup"><span data-stu-id="59efa-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="59efa-128">Questo cmdlet modifica **l'oggetto PSVirtualNetworkGateway** specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="59efa-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="59efa-129">È possibile usare il cmdlet Get-AzVirtualNetworkGateway per recuperare un **oggetto PSVirtualNetworkGateway.**</span><span class="sxs-lookup"><span data-stu-id="59efa-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="59efa-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59efa-130">-Confirm</span></span>
<span data-ttu-id="59efa-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59efa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59efa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59efa-132">-WhatIf</span></span>
<span data-ttu-id="59efa-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59efa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59efa-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59efa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59efa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59efa-135">CommonParameters</span></span>
<span data-ttu-id="59efa-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59efa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59efa-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59efa-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59efa-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="59efa-138">INPUTS</span></span>

### <span data-ttu-id="59efa-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59efa-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="59efa-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59efa-140">OUTPUTS</span></span>

### <span data-ttu-id="59efa-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59efa-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="59efa-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="59efa-142">NOTES</span></span>

## <span data-ttu-id="59efa-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59efa-143">RELATED LINKS</span></span>

[<span data-ttu-id="59efa-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59efa-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="59efa-145">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="59efa-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="59efa-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="59efa-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
