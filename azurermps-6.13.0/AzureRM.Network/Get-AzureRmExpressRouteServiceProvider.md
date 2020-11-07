---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: 0c7beb4bc53635a8bf4293abf50441b0f15b66b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688082"
---
# <span data-ttu-id="ad6cf-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ad6cf-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="ad6cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6cf-103">Ottiene un elenco dei provider di servizi ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="ad6cf-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad6cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad6cf-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad6cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad6cf-105">DESCRIPTION</span></span>
<span data-ttu-id="ad6cf-106">Il cmdlet **Get-AzureRmExpressRouteServiceProvider** recupera un elenco dei provider di servizi di ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="ad6cf-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="ad6cf-107">Gli attributi includono le opzioni di posizione e larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="ad6cf-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="ad6cf-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad6cf-108">EXAMPLES</span></span>

### <span data-ttu-id="ad6cf-109">Esempio 1: ottenere un elenco di provider di servizi con posizioni in "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="ad6cf-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="ad6cf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad6cf-110">PARAMETERS</span></span>

### <span data-ttu-id="ad6cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6cf-111">-DefaultProfile</span></span>
<span data-ttu-id="ad6cf-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad6cf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad6cf-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6cf-113">CommonParameters</span></span>
<span data-ttu-id="ad6cf-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6cf-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6cf-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad6cf-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6cf-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad6cf-116">INPUTS</span></span>

### <span data-ttu-id="ad6cf-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ad6cf-117">None</span></span>

## <span data-ttu-id="ad6cf-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad6cf-118">OUTPUTS</span></span>

### <span data-ttu-id="ad6cf-119">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ad6cf-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="ad6cf-120">Note</span><span class="sxs-lookup"><span data-stu-id="ad6cf-120">NOTES</span></span>

## <span data-ttu-id="ad6cf-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad6cf-121">RELATED LINKS</span></span>

[<span data-ttu-id="ad6cf-122">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ad6cf-122">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="ad6cf-123">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad6cf-123">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="ad6cf-124">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ad6cf-124">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="ad6cf-125">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="ad6cf-125">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)