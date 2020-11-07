---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864412"
---
# <span data-ttu-id="a67ae-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a67ae-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="a67ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a67ae-102">SYNOPSIS</span></span> 
<span data-ttu-id="a67ae-103">Disconnettere le connessioni client VPN connesse con un gateway di rete virtuale specifico.</span><span class="sxs-lookup"><span data-stu-id="a67ae-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="a67ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a67ae-104">SYNTAX</span></span>
### <span data-ttu-id="a67ae-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a67ae-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="a67ae-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a67ae-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="a67ae-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a67ae-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="a67ae-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a67ae-108">DESCRIPTION</span></span>
<span data-ttu-id="a67ae-109">Il cmdlet **Disconnect-AzVirtualNetworkGatewayVpnConnection** consente di disconnettere la connessione al client VPN connessa.</span><span class="sxs-lookup"><span data-stu-id="a67ae-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="a67ae-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a67ae-110">EXAMPLES</span></span>

### <span data-ttu-id="a67ae-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="a67ae-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="a67ae-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a67ae-112">PARAMETERS</span></span>

### <span data-ttu-id="a67ae-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a67ae-113">-ResourceGroupName</span></span>
<span data-ttu-id="a67ae-114">Nome del gruppo risorse di Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="a67ae-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="a67ae-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a67ae-115">-ResourceName</span></span>
<span data-ttu-id="a67ae-116">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a67ae-116">Virtual network gateway name</span></span>

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

### <span data-ttu-id="a67ae-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a67ae-117">-ResourceId</span></span>
<span data-ttu-id="a67ae-118">ID risorsa di Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="a67ae-118">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="a67ae-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="a67ae-119">-VpnConnectionId</span></span>
<span data-ttu-id="a67ae-120">ID connessione VPN</span><span class="sxs-lookup"><span data-stu-id="a67ae-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="a67ae-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a67ae-121">-InputObject</span></span>
<span data-ttu-id="a67ae-122">Oggetto gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a67ae-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="a67ae-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a67ae-123">-AsJob</span></span>
<span data-ttu-id="a67ae-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a67ae-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a67ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67ae-125">CommonParameters</span></span>
<span data-ttu-id="a67ae-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a67ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67ae-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a67ae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67ae-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a67ae-128">INPUTS</span></span>

### <span data-ttu-id="a67ae-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a67ae-129">System.String</span></span>

## <span data-ttu-id="a67ae-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a67ae-130">OUTPUTS</span></span>

### <span data-ttu-id="a67ae-131">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a67ae-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a67ae-132">Note</span><span class="sxs-lookup"><span data-stu-id="a67ae-132">NOTES</span></span>

## <span data-ttu-id="a67ae-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a67ae-133">RELATED LINKS</span></span>
