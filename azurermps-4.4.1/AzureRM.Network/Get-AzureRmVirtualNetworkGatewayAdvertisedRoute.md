---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: a9b8cd9f13de8c1c4e3a7f20a0ffe410211f8973
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686224"
---
# <span data-ttu-id="9fe65-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="9fe65-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="9fe65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9fe65-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe65-103">Elenca le route annunciate da un gateway di rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="9fe65-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fe65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fe65-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fe65-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fe65-105">DESCRIPTION</span></span>
<span data-ttu-id="9fe65-106">In base all'IP di un peer BGP, vengono enumerate le route annunciate a tale peer dal gateway di rete virtuale Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="9fe65-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="9fe65-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fe65-107">EXAMPLES</span></span>

### <span data-ttu-id="9fe65-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9fe65-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="9fe65-109">Per il gateway di Azure denominato GatewayName nel gruppo di risorse resourceGroupName, Retrives un elenco di route pubblicizzate nel peer BGP con IP 10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="9fe65-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="9fe65-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9fe65-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="9fe65-111">Per il gateway di Azure denominato GatewayName nel gruppo di risorse resourceGroupName, recupera le route annunciate al primo peer BGP nell'elenco dei peer BGP del gateway.</span><span class="sxs-lookup"><span data-stu-id="9fe65-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="9fe65-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9fe65-112">PARAMETERS</span></span>

### <span data-ttu-id="9fe65-113">-Peer</span><span class="sxs-lookup"><span data-stu-id="9fe65-113">-Peer</span></span>
<span data-ttu-id="9fe65-114">Indirizzo IP del peer BGP.</span><span class="sxs-lookup"><span data-stu-id="9fe65-114">BGP peer's IP address.</span></span> <span data-ttu-id="9fe65-115">Dovrebbe essere un IP all'interno dello spazio indirizzo accessibile dall'interno della rete virtuale Azure in cui è distribuito il gateway.</span><span class="sxs-lookup"><span data-stu-id="9fe65-115">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="9fe65-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe65-116">-ResourceGroupName</span></span>
<span data-ttu-id="9fe65-117">Nome del gruppo risorse di Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="9fe65-117">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="9fe65-118">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="9fe65-118">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="9fe65-119">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="9fe65-119">Virtual network gateway name</span></span>

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

### <span data-ttu-id="9fe65-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe65-120">-DefaultProfile</span></span>
<span data-ttu-id="9fe65-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fe65-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fe65-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe65-122">CommonParameters</span></span>
<span data-ttu-id="9fe65-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fe65-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe65-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe65-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe65-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9fe65-125">INPUTS</span></span>

### <span data-ttu-id="9fe65-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9fe65-126">System.String</span></span>

## <span data-ttu-id="9fe65-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fe65-127">OUTPUTS</span></span>

### <span data-ttu-id="9fe65-128">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="9fe65-128">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="9fe65-129">Note</span><span class="sxs-lookup"><span data-stu-id="9fe65-129">NOTES</span></span>
<span data-ttu-id="9fe65-130">Questo comando è applicabile solo ai gateway di rete virtuali di Azure con connessioni abilitate per BGP.</span><span class="sxs-lookup"><span data-stu-id="9fe65-130">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="9fe65-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fe65-131">RELATED LINKS</span></span>

