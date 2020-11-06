---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 09a3457127646c28c96007532f0e83d1dc1232f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513619"
---
# <span data-ttu-id="b9ad2-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b9ad2-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="b9ad2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ad2-103">Rimuove una configurazione IP da un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b9ad2-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9ad2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9ad2-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9ad2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="b9ad2-106">Rimuove una configurazione IP da un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b9ad2-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="b9ad2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9ad2-107">EXAMPLES</span></span>

### <span data-ttu-id="b9ad2-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="b9ad2-108">Example 1:</span></span>
```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gateway -Name ActiveActive

Name                   : myGateway
ResourceGroupName      : myRG
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft
                         .Network/virtualNetworkGateways/VNet8GW
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/800000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/virtualNetworks/VNet8/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/publicIPAddresses/VNet8GWIP"
                             },
                             "Name": "gwipconfig1",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provider
                         s/Microsoft.Network/virtualNetworkGateways/VNet8GW/ipConfigurations/gwipconfig1"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : True
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "192.0.2.4,192.0.2.5",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="b9ad2-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9ad2-109">PARAMETERS</span></span>

### <span data-ttu-id="b9ad2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ad2-110">-DefaultProfile</span></span>
<span data-ttu-id="b9ad2-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ad2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9ad2-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9ad2-112">-Name</span></span>
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

### <span data-ttu-id="b9ad2-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9ad2-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="b9ad2-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9ad2-114">-Confirm</span></span>
<span data-ttu-id="b9ad2-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9ad2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9ad2-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9ad2-116">-WhatIf</span></span>
<span data-ttu-id="b9ad2-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9ad2-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9ad2-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9ad2-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9ad2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ad2-119">CommonParameters</span></span>
<span data-ttu-id="b9ad2-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ad2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ad2-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9ad2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ad2-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9ad2-122">INPUTS</span></span>

### <span data-ttu-id="b9ad2-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9ad2-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="b9ad2-124">Parametri: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b9ad2-124">Parameters: VirtualNetworkGateway (ByValue)</span></span>

## <span data-ttu-id="b9ad2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9ad2-125">OUTPUTS</span></span>

### <span data-ttu-id="b9ad2-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9ad2-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b9ad2-127">Note</span><span class="sxs-lookup"><span data-stu-id="b9ad2-127">NOTES</span></span>

## <span data-ttu-id="b9ad2-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9ad2-128">RELATED LINKS</span></span>
