---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: f335272bce6591c617d8111dd1d0d81af50ec255
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476529"
---
# <span data-ttu-id="2f3c1-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="2f3c1-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="2f3c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f3c1-102">SYNOPSIS</span></span>
<span data-ttu-id="2f3c1-103">Crea un criterio di selezione del traffico.</span><span class="sxs-lookup"><span data-stu-id="2f3c1-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="2f3c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f3c1-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f3c1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f3c1-105">DESCRIPTION</span></span>
<span data-ttu-id="2f3c1-106">Il cmdlet New-AzTrafficSelectorPolicy crea una proposta di criteri di selezione del traffico da usare in una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2f3c1-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="2f3c1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f3c1-107">EXAMPLES</span></span>

### <span data-ttu-id="2f3c1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2f3c1-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="2f3c1-109">Crea un'istanza di un criterio del selettore del traffico e lo aggiunge come parametro quando si crea una connessione virtuale del gateway di rete con un protocollo IKEv2.</span><span class="sxs-lookup"><span data-stu-id="2f3c1-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="2f3c1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f3c1-110">PARAMETERS</span></span>

### <span data-ttu-id="2f3c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f3c1-111">-DefaultProfile</span></span>
<span data-ttu-id="2f3c1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f3c1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f3c1-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="2f3c1-113">-LocalAddressRange</span></span>
<span data-ttu-id="2f3c1-114">Una raccolta di intervalli di indirizzi CIDR</span><span class="sxs-lookup"><span data-stu-id="2f3c1-114">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="2f3c1-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="2f3c1-115">-RemoteAddressRange</span></span>
<span data-ttu-id="2f3c1-116">Una raccolta di intervalli di indirizzi CIDR</span><span class="sxs-lookup"><span data-stu-id="2f3c1-116">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="2f3c1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f3c1-117">CommonParameters</span></span>
<span data-ttu-id="2f3c1-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f3c1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f3c1-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f3c1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f3c1-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f3c1-120">INPUTS</span></span>

### <span data-ttu-id="2f3c1-121">System. String []</span><span class="sxs-lookup"><span data-stu-id="2f3c1-121">System.String[]</span></span>

## <span data-ttu-id="2f3c1-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f3c1-122">OUTPUTS</span></span>

### <span data-ttu-id="2f3c1-123">Microsoft. Azure. Commands. Network. Models. PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="2f3c1-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="2f3c1-124">Note</span><span class="sxs-lookup"><span data-stu-id="2f3c1-124">NOTES</span></span>

## <span data-ttu-id="2f3c1-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f3c1-125">RELATED LINKS</span></span>
