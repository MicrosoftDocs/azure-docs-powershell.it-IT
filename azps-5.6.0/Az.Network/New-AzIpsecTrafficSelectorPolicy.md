---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: 6980ccc3e3ad9c69755253183da1d83f522973da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010318"
---
# <span data-ttu-id="8402b-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="8402b-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="8402b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8402b-102">SYNOPSIS</span></span>
<span data-ttu-id="8402b-103">Crea un criterio di selezione del traffico.</span><span class="sxs-lookup"><span data-stu-id="8402b-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="8402b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8402b-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8402b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8402b-105">DESCRIPTION</span></span>
<span data-ttu-id="8402b-106">Il New-AzTrafficSelectorPolicy cmdlet crea una proposta per il criterio di selezione del traffico da usare in una connessione gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8402b-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="8402b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8402b-107">EXAMPLES</span></span>

### <span data-ttu-id="8402b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8402b-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="8402b-109">Crea un'istanza di un criterio di selezione del traffico e la aggiunge come parametro durante la creazione di una connessione a un gateway di rete virtuale con un protocollo IKEv2.</span><span class="sxs-lookup"><span data-stu-id="8402b-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="8402b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8402b-110">PARAMETERS</span></span>

### <span data-ttu-id="8402b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8402b-111">-DefaultProfile</span></span>
<span data-ttu-id="8402b-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8402b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8402b-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="8402b-113">-LocalAddressRange</span></span>
<span data-ttu-id="8402b-114">Raccolta di intervalli di indirizzi CIDR</span><span class="sxs-lookup"><span data-stu-id="8402b-114">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8402b-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="8402b-115">-RemoteAddressRange</span></span>
<span data-ttu-id="8402b-116">Raccolta di intervalli di indirizzi CIDR</span><span class="sxs-lookup"><span data-stu-id="8402b-116">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8402b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8402b-117">CommonParameters</span></span>
<span data-ttu-id="8402b-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8402b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8402b-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8402b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8402b-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="8402b-120">INPUTS</span></span>

### <span data-ttu-id="8402b-121">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8402b-121">System.String[]</span></span>

## <span data-ttu-id="8402b-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8402b-122">OUTPUTS</span></span>

### <span data-ttu-id="8402b-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="8402b-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="8402b-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="8402b-124">NOTES</span></span>

## <span data-ttu-id="8402b-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8402b-125">RELATED LINKS</span></span>
