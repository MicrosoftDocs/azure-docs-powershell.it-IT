---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: d41e71afc27129d2b2de40df97f12b0bb8f07ae5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179830"
---
# <span data-ttu-id="471d2-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="471d2-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="471d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="471d2-102">SYNOPSIS</span></span>
<span data-ttu-id="471d2-103">Elenca i percorsi annunciati da un gateway di rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="471d2-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="471d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="471d2-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="471d2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="471d2-105">DESCRIPTION</span></span>
<span data-ttu-id="471d2-106">Dato l'indirizzo IP di un peer BGP, enumera le route annunciate al peer dal gateway di rete virtuale di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="471d2-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="471d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="471d2-107">EXAMPLES</span></span>

### <span data-ttu-id="471d2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="471d2-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="471d2-109">Per il gateway di Azure denominato gatewayName nel gruppo di risorse resourceGroupName, recupera un elenco di route annunciate al peer BGP con IP 10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="471d2-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="471d2-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="471d2-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="471d2-111">Per il gateway di Azure denominato gatewayName nel gruppo di risorse resourceGroupName, recupera le route annunciate al primo peer BGP nell'elenco di peer BGP del gateway.</span><span class="sxs-lookup"><span data-stu-id="471d2-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="471d2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="471d2-112">PARAMETERS</span></span>

### <span data-ttu-id="471d2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="471d2-113">-AsJob</span></span>
<span data-ttu-id="471d2-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="471d2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="471d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="471d2-115">-DefaultProfile</span></span>
<span data-ttu-id="471d2-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="471d2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="471d2-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="471d2-117">-Peer</span></span>
<span data-ttu-id="471d2-118">Indirizzo IP del peer BGP.</span><span class="sxs-lookup"><span data-stu-id="471d2-118">BGP peer's IP address.</span></span> <span data-ttu-id="471d2-119">Deve trattarsi di un indirizzo IP nello spazio degli indirizzi accessibile all'interno della rete virtuale di Azure in cui è distribuito il gateway.</span><span class="sxs-lookup"><span data-stu-id="471d2-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="471d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="471d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="471d2-121">Nome del gruppo di risorse gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="471d2-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="471d2-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="471d2-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="471d2-123">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="471d2-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="471d2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="471d2-124">CommonParameters</span></span>
<span data-ttu-id="471d2-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="471d2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="471d2-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="471d2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="471d2-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="471d2-127">INPUTS</span></span>

### <span data-ttu-id="471d2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="471d2-128">System.String</span></span>

## <span data-ttu-id="471d2-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="471d2-129">OUTPUTS</span></span>

### <span data-ttu-id="471d2-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="471d2-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="471d2-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="471d2-131">NOTES</span></span>
<span data-ttu-id="471d2-132">Questo comando è applicabile solo ai gateway di rete virtuale di Azure con connessioni abilitate per BGP.</span><span class="sxs-lookup"><span data-stu-id="471d2-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="471d2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="471d2-133">RELATED LINKS</span></span>
