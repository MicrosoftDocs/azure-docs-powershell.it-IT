---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 9648eb1561ae15501f7a395846f7fda71cf5a1f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193550"
---
# <span data-ttu-id="f2f82-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f2f82-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="f2f82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2f82-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f82-103">Crea un oggetto tabella della route dell'hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f82-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="f2f82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2f82-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2f82-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f2f82-105">DESCRIPTION</span></span>
<span data-ttu-id="f2f82-106">Crea un oggetto tabella della route dell'hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f82-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="f2f82-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2f82-107">EXAMPLES</span></span>

### <span data-ttu-id="f2f82-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f2f82-108">Example 1</span></span>

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

<span data-ttu-id="f2f82-109">Come descritto sopra verrà creata una tabella di route composta da più route e collegata a un nuovo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2f82-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="f2f82-110">Si tratta di un oggetto in memoria che può essere usato per aggiungere una tabella route a un VirtualHub nuovo o esistente.</span><span class="sxs-lookup"><span data-stu-id="f2f82-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="f2f82-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2f82-111">PARAMETERS</span></span>

### <span data-ttu-id="f2f82-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f82-112">-DefaultProfile</span></span>
<span data-ttu-id="f2f82-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f82-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2f82-114">-Route</span><span class="sxs-lookup"><span data-stu-id="f2f82-114">-Route</span></span>
<span data-ttu-id="f2f82-115">Elenco delle route dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2f82-115">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="f2f82-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f82-116">CommonParameters</span></span>
<span data-ttu-id="f2f82-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f82-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f82-118">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2f82-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f82-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="f2f82-119">INPUTS</span></span>

### <span data-ttu-id="f2f82-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f2f82-120">None</span></span>

## <span data-ttu-id="f2f82-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2f82-121">OUTPUTS</span></span>

### <span data-ttu-id="f2f82-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f2f82-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="f2f82-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="f2f82-123">NOTES</span></span>

## <span data-ttu-id="f2f82-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2f82-124">RELATED LINKS</span></span>

[<span data-ttu-id="f2f82-125">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f2f82-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)
