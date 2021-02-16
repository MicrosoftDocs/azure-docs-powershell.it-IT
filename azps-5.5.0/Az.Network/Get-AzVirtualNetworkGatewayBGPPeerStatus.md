---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 62fed5537cc22ee21679cbe1b8d126d9d30efb71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179814"
---
# <span data-ttu-id="a3120-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="a3120-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="a3120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3120-102">SYNOPSIS</span></span>
<span data-ttu-id="a3120-103">Elenca i peer BGP di un gateway di rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="a3120-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="a3120-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3120-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3120-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a3120-105">DESCRIPTION</span></span>
<span data-ttu-id="a3120-106">Questo comando enumera i peer BGP con cui è configurato un gateway di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="a3120-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="a3120-107">Viene fornito anche lo stato di ogni peer.</span><span class="sxs-lookup"><span data-stu-id="a3120-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="a3120-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3120-108">EXAMPLES</span></span>

### <span data-ttu-id="a3120-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3120-109">Example 1</span></span>
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

<span data-ttu-id="a3120-110">Recupera i peer BGP per il gateway di rete virtuale di Azure denominato gatewayName nel gruppo di risorse ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a3120-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="a3120-111">Questo output di esempio mostra un peer BGP connesso, con un indirizzo IP di 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="a3120-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="a3120-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3120-112">PARAMETERS</span></span>

### <span data-ttu-id="a3120-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3120-113">-AsJob</span></span>
<span data-ttu-id="a3120-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a3120-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3120-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3120-115">-DefaultProfile</span></span>
<span data-ttu-id="a3120-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3120-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3120-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="a3120-117">-Peer</span></span>
<span data-ttu-id="a3120-118">IP del peer per cui recuperare lo stato</span><span class="sxs-lookup"><span data-stu-id="a3120-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="a3120-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3120-119">-ResourceGroupName</span></span>
<span data-ttu-id="a3120-120">Nome del gruppo di risorse gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a3120-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="a3120-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a3120-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a3120-122">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a3120-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="a3120-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3120-123">CommonParameters</span></span>
<span data-ttu-id="a3120-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3120-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3120-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3120-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3120-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="a3120-126">INPUTS</span></span>

### <span data-ttu-id="a3120-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a3120-127">System.String</span></span>

## <span data-ttu-id="a3120-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3120-128">OUTPUTS</span></span>

### <span data-ttu-id="a3120-129">Microsoft.Azure.Commands.Network.Models.PSBGPStatus</span><span class="sxs-lookup"><span data-stu-id="a3120-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="a3120-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="a3120-130">NOTES</span></span>

## <span data-ttu-id="a3120-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3120-131">RELATED LINKS</span></span>
