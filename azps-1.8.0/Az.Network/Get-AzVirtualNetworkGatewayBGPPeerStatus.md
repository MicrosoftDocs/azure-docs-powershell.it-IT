---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 416bc8910e651ca86ef064fda7bd934d67ed8056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678440"
---
# <span data-ttu-id="47899-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="47899-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="47899-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47899-102">SYNOPSIS</span></span>
<span data-ttu-id="47899-103">Elenca i peer BGP di Azure Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="47899-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="47899-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47899-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47899-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47899-105">DESCRIPTION</span></span>
<span data-ttu-id="47899-106">Questo comando enumera i peer BGP un gateway di rete virtuale di Azure è configurato per il peer con.</span><span class="sxs-lookup"><span data-stu-id="47899-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="47899-107">Viene assegnato anche lo stato di ogni peer.</span><span class="sxs-lookup"><span data-stu-id="47899-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="47899-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47899-108">EXAMPLES</span></span>

### <span data-ttu-id="47899-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="47899-109">Example 1</span></span>
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

<span data-ttu-id="47899-110">Recupera i peer BGP per il gateway di rete virtuale di Azure denominato GatewayName nel gruppo di risorse resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="47899-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="47899-111">Questo output di esempio mostra un peer BGP connesso, con un IP di 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="47899-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="47899-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47899-112">PARAMETERS</span></span>

### <span data-ttu-id="47899-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47899-113">-AsJob</span></span>
<span data-ttu-id="47899-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="47899-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47899-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47899-115">-DefaultProfile</span></span>
<span data-ttu-id="47899-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47899-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47899-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="47899-117">-Peer</span></span>
<span data-ttu-id="47899-118">IP del peer per recuperare lo stato per</span><span class="sxs-lookup"><span data-stu-id="47899-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="47899-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47899-119">-ResourceGroupName</span></span>
<span data-ttu-id="47899-120">Nome del gruppo risorse di Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="47899-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="47899-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="47899-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="47899-122">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="47899-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="47899-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47899-123">CommonParameters</span></span>
<span data-ttu-id="47899-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47899-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47899-125">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47899-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47899-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47899-126">INPUTS</span></span>

### <span data-ttu-id="47899-127">System. String</span><span class="sxs-lookup"><span data-stu-id="47899-127">System.String</span></span>

## <span data-ttu-id="47899-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47899-128">OUTPUTS</span></span>

### <span data-ttu-id="47899-129">Microsoft. Azure. Commands. Network. Models. PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="47899-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="47899-130">Note</span><span class="sxs-lookup"><span data-stu-id="47899-130">NOTES</span></span>

## <span data-ttu-id="47899-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47899-131">RELATED LINKS</span></span>