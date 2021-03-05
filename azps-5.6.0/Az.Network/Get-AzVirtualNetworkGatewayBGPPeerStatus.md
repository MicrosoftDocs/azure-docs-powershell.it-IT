---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: fd0bb4c3035eb2def0a1d0fa64038299cee4ec48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964270"
---
# <span data-ttu-id="2cb91-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="2cb91-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="2cb91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cb91-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb91-103">Elenca i peer BGP di un gateway di rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="2cb91-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="2cb91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cb91-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cb91-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2cb91-105">DESCRIPTION</span></span>
<span data-ttu-id="2cb91-106">Questo comando enumera i peer BGP con cui è configurato un gateway di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="2cb91-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="2cb91-107">Viene fornito anche lo stato di ogni peer.</span><span class="sxs-lookup"><span data-stu-id="2cb91-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="2cb91-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cb91-108">EXAMPLES</span></span>

### <span data-ttu-id="2cb91-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2cb91-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="2cb91-110">Recupera i peer BGP per il gateway di rete virtuale di Azure denominato gatewayName nel gruppo di risorse ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2cb91-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="2cb91-111">Questo output di esempio mostra un peer BGP connesso, con un indirizzo IP di 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="2cb91-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="2cb91-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cb91-112">PARAMETERS</span></span>

### <span data-ttu-id="2cb91-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cb91-113">-AsJob</span></span>
<span data-ttu-id="2cb91-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2cb91-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cb91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb91-115">-DefaultProfile</span></span>
<span data-ttu-id="2cb91-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cb91-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cb91-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="2cb91-117">-Peer</span></span>
<span data-ttu-id="2cb91-118">IP del peer per cui recuperare lo stato</span><span class="sxs-lookup"><span data-stu-id="2cb91-118">IP of the peer to retrieve status for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb91-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb91-119">-ResourceGroupName</span></span>
<span data-ttu-id="2cb91-120">Nome del gruppo di risorse del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2cb91-120">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb91-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="2cb91-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="2cb91-122">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2cb91-122">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb91-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb91-123">CommonParameters</span></span>
<span data-ttu-id="2cb91-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cb91-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb91-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2cb91-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb91-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="2cb91-126">INPUTS</span></span>

### <span data-ttu-id="2cb91-127">System.String</span><span class="sxs-lookup"><span data-stu-id="2cb91-127">System.String</span></span>

## <span data-ttu-id="2cb91-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cb91-128">OUTPUTS</span></span>

### <span data-ttu-id="2cb91-129">Microsoft.Azure.Commands.Network.Models.PSBGPStatus</span><span class="sxs-lookup"><span data-stu-id="2cb91-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="2cb91-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="2cb91-130">NOTES</span></span>

## <span data-ttu-id="2cb91-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cb91-131">RELATED LINKS</span></span>
