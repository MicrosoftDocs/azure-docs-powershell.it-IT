---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
ms.openlocfilehash: 7e4febe620b8a440d1f9a5eb0c9432da9ff47c74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866292"
---
# <span data-ttu-id="8f2d5-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="8f2d5-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="8f2d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f2d5-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2d5-103">Ottiene un elenco dei provider di servizi ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f2d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f2d5-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f2d5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f2d5-105">DESCRIPTION</span></span>
<span data-ttu-id="8f2d5-106">Il cmdlet **Get-AzureRmExpressRouteServiceProvider** recupera un elenco dei provider di servizi di ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="8f2d5-107">Gli attributi includono le opzioni di posizione e larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="8f2d5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f2d5-108">EXAMPLES</span></span>

### <span data-ttu-id="8f2d5-109">Esempio 1: ottenere un elenco di provider di servizi con posizioni in "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="8f2d5-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="8f2d5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f2d5-110">PARAMETERS</span></span>

### <span data-ttu-id="8f2d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2d5-111">-DefaultProfile</span></span>
<span data-ttu-id="8f2d5-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f2d5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2d5-113">CommonParameters</span></span>
<span data-ttu-id="8f2d5-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2d5-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f2d5-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2d5-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f2d5-116">INPUTS</span></span>

## <span data-ttu-id="8f2d5-117">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f2d5-117">OUTPUTS</span></span>

### <span data-ttu-id="8f2d5-118">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="8f2d5-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="8f2d5-119">Note</span><span class="sxs-lookup"><span data-stu-id="8f2d5-119">NOTES</span></span>

## <span data-ttu-id="8f2d5-120">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f2d5-120">RELATED LINKS</span></span>

[<span data-ttu-id="8f2d5-121">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8f2d5-121">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="8f2d5-122">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8f2d5-122">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="8f2d5-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8f2d5-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="8f2d5-124">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="8f2d5-124">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
