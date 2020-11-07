---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
ms.openlocfilehash: 0097cd022387b3ac2ee8ceb1fa2a831b60c4256d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865765"
---
# <span data-ttu-id="2308f-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="2308f-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="2308f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2308f-102">SYNOPSIS</span></span>
<span data-ttu-id="2308f-103">Elenca le route annunciate da un gateway di rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="2308f-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2308f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2308f-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2308f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2308f-105">DESCRIPTION</span></span>
<span data-ttu-id="2308f-106">In base all'IP di un peer BGP, vengono enumerate le route annunciate a tale peer dal gateway di rete virtuale Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="2308f-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="2308f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2308f-107">EXAMPLES</span></span>

### <span data-ttu-id="2308f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2308f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="2308f-109">Per il gateway di Azure denominato GatewayName nel gruppo di risorse resourceGroupName, Retrives un elenco di route pubblicizzate nel peer BGP con IP 10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="2308f-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="2308f-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2308f-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="2308f-111">Per il gateway di Azure denominato GatewayName nel gruppo di risorse resourceGroupName, recupera le route annunciate al primo peer BGP nell'elenco dei peer BGP del gateway.</span><span class="sxs-lookup"><span data-stu-id="2308f-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="2308f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2308f-112">PARAMETERS</span></span>

### <span data-ttu-id="2308f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2308f-113">-AsJob</span></span>
<span data-ttu-id="2308f-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2308f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2308f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2308f-115">-DefaultProfile</span></span>
<span data-ttu-id="2308f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2308f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2308f-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="2308f-117">-Peer</span></span>
<span data-ttu-id="2308f-118">Indirizzo IP del peer BGP.</span><span class="sxs-lookup"><span data-stu-id="2308f-118">BGP peer's IP address.</span></span> <span data-ttu-id="2308f-119">Dovrebbe essere un IP all'interno dello spazio indirizzo accessibile dall'interno della rete virtuale Azure in cui è distribuito il gateway.</span><span class="sxs-lookup"><span data-stu-id="2308f-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="2308f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2308f-120">-ResourceGroupName</span></span>
<span data-ttu-id="2308f-121">Nome del gruppo risorse di Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="2308f-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="2308f-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="2308f-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="2308f-123">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2308f-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="2308f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2308f-124">CommonParameters</span></span>
<span data-ttu-id="2308f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2308f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2308f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2308f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2308f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2308f-127">INPUTS</span></span>

### <span data-ttu-id="2308f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2308f-128">System.String</span></span>

## <span data-ttu-id="2308f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2308f-129">OUTPUTS</span></span>

### <span data-ttu-id="2308f-130">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="2308f-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="2308f-131">Note</span><span class="sxs-lookup"><span data-stu-id="2308f-131">NOTES</span></span>
<span data-ttu-id="2308f-132">Questo comando è applicabile solo ai gateway di rete virtuali di Azure con connessioni abilitate per BGP.</span><span class="sxs-lookup"><span data-stu-id="2308f-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="2308f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2308f-133">RELATED LINKS</span></span>

