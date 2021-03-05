---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: 1cbbfcbc87ed1d9be869066f8ec6dd288ba3d4d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003709"
---
# <span data-ttu-id="b3b94-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b3b94-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="b3b94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3b94-102">SYNOPSIS</span></span> 
<span data-ttu-id="b3b94-103">Disconnettere le connessioni vpn connesse con un gateway di rete virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="b3b94-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="b3b94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3b94-104">SYNTAX</span></span>
### <span data-ttu-id="b3b94-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3b94-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="b3b94-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="b3b94-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="b3b94-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="b3b94-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="b3b94-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b3b94-108">DESCRIPTION</span></span>
<span data-ttu-id="b3b94-109">Il cmdlet **Disconnect-AzVirtualNetworkGatewayVpnConnection** consente di disconnettere una determinata connessione al client VPN connesso.</span><span class="sxs-lookup"><span data-stu-id="b3b94-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="b3b94-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3b94-110">EXAMPLES</span></span>

### <span data-ttu-id="b3b94-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="b3b94-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="b3b94-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3b94-112">PARAMETERS</span></span>

### <span data-ttu-id="b3b94-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3b94-113">-ResourceGroupName</span></span>
<span data-ttu-id="b3b94-114">Nome del gruppo di risorse del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b3b94-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b94-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b3b94-115">-ResourceName</span></span>
<span data-ttu-id="b3b94-116">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b3b94-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b94-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3b94-117">-ResourceId</span></span>
<span data-ttu-id="b3b94-118">ID risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b3b94-118">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b94-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="b3b94-119">-VpnConnectionId</span></span>
<span data-ttu-id="b3b94-120">ID connessione Vpn</span><span class="sxs-lookup"><span data-stu-id="b3b94-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="b3b94-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3b94-121">-InputObject</span></span>
<span data-ttu-id="b3b94-122">Oggetto Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b3b94-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b94-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3b94-123">-AsJob</span></span>
<span data-ttu-id="b3b94-124">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b3b94-124">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b94-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b94-125">CommonParameters</span></span>
<span data-ttu-id="b3b94-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b94-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b94-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b3b94-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b94-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="b3b94-128">INPUTS</span></span>

### <span data-ttu-id="b3b94-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b3b94-129">System.String</span></span>

## <span data-ttu-id="b3b94-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3b94-130">OUTPUTS</span></span>

### <span data-ttu-id="b3b94-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3b94-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b3b94-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="b3b94-132">NOTES</span></span>

## <span data-ttu-id="b3b94-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3b94-133">RELATED LINKS</span></span>
