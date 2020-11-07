---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: f92b211befbf019f46869f733fa012e74e72c327
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860669"
---
# <span data-ttu-id="ef9a9-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="ef9a9-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="ef9a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ef9a9-103">Elenca i peer BGP di Azure Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="ef9a9-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="ef9a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef9a9-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef9a9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="ef9a9-106">Questo comando enumera i peer BGP un gateway di rete virtuale di Azure è configurato per il peer con.</span><span class="sxs-lookup"><span data-stu-id="ef9a9-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="ef9a9-107">Viene assegnato anche lo stato di ogni peer.</span><span class="sxs-lookup"><span data-stu-id="ef9a9-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="ef9a9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef9a9-108">EXAMPLES</span></span>

### <span data-ttu-id="ef9a9-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef9a9-109">Example 1</span></span>
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

<span data-ttu-id="ef9a9-110">Recupera i peer BGP per il gateway di rete virtuale di Azure denominato GatewayName nel gruppo di risorse resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ef9a9-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>

<span data-ttu-id="ef9a9-111">Questo output di esempio mostra un peer BGP connesso, con un IP di 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="ef9a9-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="ef9a9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef9a9-112">PARAMETERS</span></span>

### <span data-ttu-id="ef9a9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef9a9-113">-AsJob</span></span>
<span data-ttu-id="ef9a9-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ef9a9-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef9a9-115">-DefaultProfile</span></span>
<span data-ttu-id="ef9a9-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef9a9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9a9-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="ef9a9-117">-Peer</span></span>
<span data-ttu-id="ef9a9-118">IP del peer per recuperare lo stato per</span><span class="sxs-lookup"><span data-stu-id="ef9a9-118">IP of the peer to retrieve status for</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef9a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef9a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="ef9a9-120">Nome del gruppo risorse di Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="ef9a9-120">Virtual network gateway resource group's name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef9a9-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ef9a9-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ef9a9-122">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ef9a9-122">Virtual network gateway name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef9a9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef9a9-123">CommonParameters</span></span>
<span data-ttu-id="ef9a9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef9a9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef9a9-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef9a9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef9a9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef9a9-126">INPUTS</span></span>

### <span data-ttu-id="ef9a9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ef9a9-127">System.String</span></span>

## <span data-ttu-id="ef9a9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef9a9-128">OUTPUTS</span></span>

### <span data-ttu-id="ef9a9-129">Microsoft. Azure. Commands. Network. Models. PSBGPPeerStatus []</span><span class="sxs-lookup"><span data-stu-id="ef9a9-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus[]</span></span>

## <span data-ttu-id="ef9a9-130">Note</span><span class="sxs-lookup"><span data-stu-id="ef9a9-130">NOTES</span></span>

## <span data-ttu-id="ef9a9-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef9a9-131">RELATED LINKS</span></span>

