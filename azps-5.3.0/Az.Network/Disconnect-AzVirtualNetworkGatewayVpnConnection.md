---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385643"
---
# <span data-ttu-id="0b7f8-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="0b7f8-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="0b7f8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b7f8-102">SYNOPSIS</span></span> 
<span data-ttu-id="0b7f8-103">Disconnettere le connessioni client VPN connesse con un gateway di rete virtuale specifico.</span><span class="sxs-lookup"><span data-stu-id="0b7f8-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="0b7f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b7f8-104">SYNTAX</span></span>
### <span data-ttu-id="0b7f8-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b7f8-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="0b7f8-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="0b7f8-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="0b7f8-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="0b7f8-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="0b7f8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b7f8-108">DESCRIPTION</span></span>
<span data-ttu-id="0b7f8-109">Il cmdlet **Disconnect-AzVirtualNetworkGatewayVpnConnection** consente di disconnettere la connessione al client VPN connessa.</span><span class="sxs-lookup"><span data-stu-id="0b7f8-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="0b7f8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b7f8-110">EXAMPLES</span></span>

### <span data-ttu-id="0b7f8-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="0b7f8-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="0b7f8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b7f8-112">PARAMETERS</span></span>

### <span data-ttu-id="0b7f8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b7f8-113">-ResourceGroupName</span></span>
<span data-ttu-id="0b7f8-114">Nome del gruppo risorse di Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="0b7f8-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="0b7f8-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0b7f8-115">-ResourceName</span></span>
<span data-ttu-id="0b7f8-116">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0b7f8-116">Virtual network gateway name</span></span>

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

### <span data-ttu-id="0b7f8-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b7f8-117">-ResourceId</span></span>
<span data-ttu-id="0b7f8-118">ID risorsa di Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="0b7f8-118">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="0b7f8-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="0b7f8-119">-VpnConnectionId</span></span>
<span data-ttu-id="0b7f8-120">ID connessione VPN</span><span class="sxs-lookup"><span data-stu-id="0b7f8-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="0b7f8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b7f8-121">-InputObject</span></span>
<span data-ttu-id="0b7f8-122">Oggetto gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0b7f8-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="0b7f8-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b7f8-123">-AsJob</span></span>
<span data-ttu-id="0b7f8-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0b7f8-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b7f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b7f8-125">CommonParameters</span></span>
<span data-ttu-id="0b7f8-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b7f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b7f8-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b7f8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b7f8-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b7f8-128">INPUTS</span></span>

### <span data-ttu-id="0b7f8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0b7f8-129">System.String</span></span>

## <span data-ttu-id="0b7f8-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b7f8-130">OUTPUTS</span></span>

### <span data-ttu-id="0b7f8-131">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0b7f8-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="0b7f8-132">Note</span><span class="sxs-lookup"><span data-stu-id="0b7f8-132">NOTES</span></span>

## <span data-ttu-id="0b7f8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b7f8-133">RELATED LINKS</span></span>
