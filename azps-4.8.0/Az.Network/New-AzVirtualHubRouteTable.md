---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 9648eb1561ae15501f7a395846f7fda71cf5a1f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192329"
---
# <span data-ttu-id="901d4-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="901d4-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="901d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="901d4-102">SYNOPSIS</span></span>
<span data-ttu-id="901d4-103">Crea un oggetto tabella route hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="901d4-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="901d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="901d4-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="901d4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="901d4-105">DESCRIPTION</span></span>
<span data-ttu-id="901d4-106">Crea un oggetto tabella route hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="901d4-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="901d4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="901d4-107">EXAMPLES</span></span>

### <span data-ttu-id="901d4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="901d4-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="901d4-109">Il precedente creerà una tabella di route composta da più route e collegata a un nuovo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="901d4-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="901d4-110">Si tratta di un oggetto in memoria che può essere usato per aggiungere una tabella di route a un nuovo o a un VirtualHub esistente.</span><span class="sxs-lookup"><span data-stu-id="901d4-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="901d4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="901d4-111">PARAMETERS</span></span>

### <span data-ttu-id="901d4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901d4-112">-DefaultProfile</span></span>
<span data-ttu-id="901d4-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="901d4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="901d4-114">-Route</span><span class="sxs-lookup"><span data-stu-id="901d4-114">-Route</span></span>
<span data-ttu-id="901d4-115">Elenco di route Hub virtuali.</span><span class="sxs-lookup"><span data-stu-id="901d4-115">List of virtual hub routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901d4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901d4-116">CommonParameters</span></span>
<span data-ttu-id="901d4-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="901d4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901d4-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="901d4-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901d4-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="901d4-119">INPUTS</span></span>

### <span data-ttu-id="901d4-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="901d4-120">None</span></span>

## <span data-ttu-id="901d4-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="901d4-121">OUTPUTS</span></span>

### <span data-ttu-id="901d4-122">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="901d4-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="901d4-123">Note</span><span class="sxs-lookup"><span data-stu-id="901d4-123">NOTES</span></span>

## <span data-ttu-id="901d4-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="901d4-124">RELATED LINKS</span></span>

[<span data-ttu-id="901d4-125">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="901d4-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)
