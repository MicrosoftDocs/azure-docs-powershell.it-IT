---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: 288a2382470682c8c7b55f7342d5a0f193446019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522030"
---
# <span data-ttu-id="20813-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="20813-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="20813-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20813-102">SYNOPSIS</span></span>
<span data-ttu-id="20813-103">Elenca le route annunciate da un gateway di rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="20813-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20813-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20813-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20813-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20813-105">DESCRIPTION</span></span>
<span data-ttu-id="20813-106">In base all'IP di un peer BGP, vengono enumerate le route annunciate a tale peer dal gateway di rete virtuale Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="20813-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="20813-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20813-107">EXAMPLES</span></span>

### <span data-ttu-id="20813-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="20813-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="20813-109">Per il gateway di Azure denominato GatewayName nel gruppo di risorse resourceGroupName, Retrives un elenco di route pubblicizzate nel peer BGP con IP 10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="20813-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="20813-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="20813-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="20813-111">Per il gateway di Azure denominato GatewayName nel gruppo di risorse resourceGroupName, recupera le route annunciate al primo peer BGP nell'elenco dei peer BGP del gateway.</span><span class="sxs-lookup"><span data-stu-id="20813-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="20813-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20813-112">PARAMETERS</span></span>

### <span data-ttu-id="20813-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20813-113">-AsJob</span></span>
<span data-ttu-id="20813-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="20813-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20813-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20813-115">-DefaultProfile</span></span>
<span data-ttu-id="20813-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20813-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20813-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="20813-117">-Peer</span></span>
<span data-ttu-id="20813-118">Indirizzo IP del peer BGP.</span><span class="sxs-lookup"><span data-stu-id="20813-118">BGP peer's IP address.</span></span> <span data-ttu-id="20813-119">Dovrebbe essere un IP all'interno dello spazio indirizzo accessibile dall'interno della rete virtuale Azure in cui è distribuito il gateway.</span><span class="sxs-lookup"><span data-stu-id="20813-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="20813-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20813-120">-ResourceGroupName</span></span>
<span data-ttu-id="20813-121">Nome del gruppo risorse di Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="20813-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="20813-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="20813-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="20813-123">Nome gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="20813-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="20813-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20813-124">CommonParameters</span></span>
<span data-ttu-id="20813-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20813-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20813-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20813-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20813-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20813-127">INPUTS</span></span>

### <span data-ttu-id="20813-128">System. String</span><span class="sxs-lookup"><span data-stu-id="20813-128">System.String</span></span>

## <span data-ttu-id="20813-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20813-129">OUTPUTS</span></span>

### <span data-ttu-id="20813-130">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="20813-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="20813-131">Note</span><span class="sxs-lookup"><span data-stu-id="20813-131">NOTES</span></span>
<span data-ttu-id="20813-132">Questo comando è applicabile solo ai gateway di rete virtuali di Azure con connessioni abilitate per BGP.</span><span class="sxs-lookup"><span data-stu-id="20813-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="20813-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20813-133">RELATED LINKS</span></span>
