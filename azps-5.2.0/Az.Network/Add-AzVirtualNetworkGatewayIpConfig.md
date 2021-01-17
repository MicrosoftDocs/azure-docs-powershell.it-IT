---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: f8de9ce0aab60aad729d990c233acfaf75ae50b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359684"
---
# <span data-ttu-id="35467-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="35467-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="35467-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35467-102">SYNOPSIS</span></span>
<span data-ttu-id="35467-103">Aggiunge una configurazione IP a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="35467-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="35467-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35467-104">SYNTAX</span></span>

### <span data-ttu-id="35467-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="35467-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35467-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="35467-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35467-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35467-107">DESCRIPTION</span></span>
<span data-ttu-id="35467-108">Il cmdlet **Add-AzVirtualNetworkGatewayIpConfig** aggiunge una configurazione IP a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="35467-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="35467-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35467-109">EXAMPLES</span></span>

### <span data-ttu-id="35467-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35467-110">Example 1</span></span>
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

## <span data-ttu-id="35467-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35467-111">PARAMETERS</span></span>

### <span data-ttu-id="35467-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35467-112">-DefaultProfile</span></span>
<span data-ttu-id="35467-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35467-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35467-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="35467-114">-Name</span></span>
<span data-ttu-id="35467-115">Specifica il nome della configurazione IP del gateway da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="35467-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="35467-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="35467-116">-PrivateIpAddress</span></span>
<span data-ttu-id="35467-117">Specifica l'indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="35467-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="35467-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="35467-118">-PublicIpAddress</span></span>
<span data-ttu-id="35467-119">Specifica l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="35467-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="35467-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="35467-120">-PublicIpAddressId</span></span>
<span data-ttu-id="35467-121">Specifica l'ID dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="35467-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="35467-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="35467-122">-Subnet</span></span>
<span data-ttu-id="35467-123">Specifica un oggetto **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="35467-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="35467-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="35467-124">-SubnetId</span></span>
<span data-ttu-id="35467-125">Specifica l'ID della subnet.</span><span class="sxs-lookup"><span data-stu-id="35467-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="35467-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="35467-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="35467-127">Specifica un oggetto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="35467-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="35467-128">Questo cmdlet modifica l'oggetto **PSVirtualNetworkGateway** specificato.</span><span class="sxs-lookup"><span data-stu-id="35467-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="35467-129">Puoi usare il cmdlet Get-AzVirtualNetworkGateway per recuperare un oggetto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="35467-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="35467-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35467-130">-Confirm</span></span>
<span data-ttu-id="35467-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35467-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35467-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35467-132">-WhatIf</span></span>
<span data-ttu-id="35467-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35467-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35467-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35467-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35467-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35467-135">CommonParameters</span></span>
<span data-ttu-id="35467-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35467-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35467-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35467-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35467-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35467-138">INPUTS</span></span>

### <span data-ttu-id="35467-139">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="35467-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="35467-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35467-140">OUTPUTS</span></span>

### <span data-ttu-id="35467-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="35467-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="35467-142">Note</span><span class="sxs-lookup"><span data-stu-id="35467-142">NOTES</span></span>

## <span data-ttu-id="35467-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35467-143">RELATED LINKS</span></span>

[<span data-ttu-id="35467-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="35467-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="35467-145">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="35467-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="35467-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="35467-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
