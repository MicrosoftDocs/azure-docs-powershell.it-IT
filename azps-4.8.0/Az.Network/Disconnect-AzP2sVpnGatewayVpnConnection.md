---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azp2svpngatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2sVpnGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2sVpnGatewayVpnConnection.md
ms.openlocfilehash: ee14842a636ff451e100a75db427934f9f0a1043
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032979"
---
# <span data-ttu-id="ef9be-101">Disconnect-AzP2sVpnGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ef9be-101">Disconnect-AzP2sVpnGatewayVpnConnection</span></span>

## <span data-ttu-id="ef9be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef9be-102">SYNOPSIS</span></span>
<span data-ttu-id="ef9be-103">Disconnettere le connessioni client VPN connesse con un gateway VPN di P2S specifico</span><span class="sxs-lookup"><span data-stu-id="ef9be-103">Disconnect given connected vpn client connections with a given p2s vpn gateway</span></span>

## <span data-ttu-id="ef9be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef9be-104">SYNTAX</span></span>

### <span data-ttu-id="ef9be-105">ByP2SVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef9be-105">ByP2SVpnGatewayName (Default)</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -Name <String> -ResourceGroupName <String>
 -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="ef9be-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ef9be-106">ByP2SVpnGatewayObject</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="ef9be-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ef9be-107">ByP2SVpnGatewayResourceId</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="ef9be-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef9be-108">DESCRIPTION</span></span>
<span data-ttu-id="ef9be-109">Il cmdlet **Disconnect-AzP2sVpnGatewayVpnConnection** consente di disconnettere il punto corrente alla connessione del sito da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="ef9be-109">The **Disconnect-AzP2sVpnGatewayVpnConnection** cmdlet enables you to disconnect given current point to site connection from P2SVpnGateway.</span></span>

## <span data-ttu-id="ef9be-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef9be-110">EXAMPLES</span></span>

### <span data-ttu-id="ef9be-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef9be-111">Example 1</span></span>
```powershell
PS C:\> Disconnect-AzP2sVpnGatewayVpnConnection -ResourceName 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

## <span data-ttu-id="ef9be-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef9be-112">PARAMETERS</span></span>

### <span data-ttu-id="ef9be-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef9be-113">-InputObject</span></span>
<span data-ttu-id="ef9be-114">L'oggetto gateway VPN di P2S da modificare</span><span class="sxs-lookup"><span data-stu-id="ef9be-114">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef9be-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef9be-115">-Name</span></span>
<span data-ttu-id="ef9be-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ef9be-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9be-117">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="ef9be-117">-VpnConnectionId</span></span>
<span data-ttu-id="ef9be-118">Ida di connessione VPN</span><span class="sxs-lookup"><span data-stu-id="ef9be-118">Vpn Connection Ida</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef9be-119">-ResourceGroupName</span></span>
<span data-ttu-id="ef9be-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ef9be-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9be-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef9be-121">-ResourceId</span></span>
<span data-ttu-id="ef9be-122">ID risorsa gateway di rete virtuale P2S</span><span class="sxs-lookup"><span data-stu-id="ef9be-122">P2s Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef9be-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef9be-123">CommonParameters</span></span>
<span data-ttu-id="ef9be-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef9be-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef9be-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef9be-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef9be-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef9be-126">INPUTS</span></span>

### <span data-ttu-id="ef9be-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ef9be-127">System.String</span></span>

## <span data-ttu-id="ef9be-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef9be-128">OUTPUTS</span></span>

### <span data-ttu-id="ef9be-129">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ef9be-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="ef9be-130">Note</span><span class="sxs-lookup"><span data-stu-id="ef9be-130">NOTES</span></span>

## <span data-ttu-id="ef9be-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef9be-131">RELATED LINKS</span></span>
