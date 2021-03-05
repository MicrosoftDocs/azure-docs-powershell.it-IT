---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: 13a81733ac748d2593df967268021f10d60de50b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964286"
---
# <span data-ttu-id="db289-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="db289-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="db289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db289-102">SYNOPSIS</span></span>
<span data-ttu-id="db289-103">Elenca le route annunciate da un gateway di rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="db289-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="db289-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db289-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db289-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="db289-105">DESCRIPTION</span></span>
<span data-ttu-id="db289-106">Dato l'indirizzo IP di un peer BGP, enumera le route annunciate al peer dal gateway di rete virtuale di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="db289-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="db289-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db289-107">EXAMPLES</span></span>

### <span data-ttu-id="db289-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db289-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="db289-109">Per il gateway di Azure denominato gatewayName nel gruppo di risorse resourceGroupName, recupera un elenco di route annunciate al peer BGP con IP 10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="db289-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="db289-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="db289-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="db289-111">Per il gateway di Azure denominato gatewayName nel gruppo di risorse resourceGroupName, recupera le route annunciate al primo peer BGP nell'elenco di peer BGP del gateway.</span><span class="sxs-lookup"><span data-stu-id="db289-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="db289-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db289-112">PARAMETERS</span></span>

### <span data-ttu-id="db289-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db289-113">-AsJob</span></span>
<span data-ttu-id="db289-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="db289-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db289-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db289-115">-DefaultProfile</span></span>
<span data-ttu-id="db289-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db289-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db289-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="db289-117">-Peer</span></span>
<span data-ttu-id="db289-118">Indirizzo IP del peer BGP.</span><span class="sxs-lookup"><span data-stu-id="db289-118">BGP peer's IP address.</span></span> <span data-ttu-id="db289-119">Deve trattarsi di un indirizzo IP nello spazio degli indirizzi accessibile all'interno della rete virtuale di Azure in cui è distribuito il gateway.</span><span class="sxs-lookup"><span data-stu-id="db289-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="db289-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db289-120">-ResourceGroupName</span></span>
<span data-ttu-id="db289-121">Nome del gruppo di risorse del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="db289-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="db289-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="db289-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="db289-123">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="db289-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="db289-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db289-124">CommonParameters</span></span>
<span data-ttu-id="db289-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db289-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db289-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db289-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db289-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="db289-127">INPUTS</span></span>

### <span data-ttu-id="db289-128">System.String</span><span class="sxs-lookup"><span data-stu-id="db289-128">System.String</span></span>

## <span data-ttu-id="db289-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db289-129">OUTPUTS</span></span>

### <span data-ttu-id="db289-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="db289-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="db289-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="db289-131">NOTES</span></span>
<span data-ttu-id="db289-132">Questo comando è applicabile solo ai gateway di rete virtuale di Azure con connessioni abilitate per BGP.</span><span class="sxs-lookup"><span data-stu-id="db289-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="db289-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db289-133">RELATED LINKS</span></span>
