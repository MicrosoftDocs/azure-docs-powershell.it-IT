---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: d8d5abedd0deaf5af341995552ad72bef4703058
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685612"
---
# <span data-ttu-id="15723-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="15723-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="15723-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15723-102">SYNOPSIS</span></span>
<span data-ttu-id="15723-103">Ottiene un elenco dei provider di servizi ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="15723-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15723-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15723-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15723-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15723-105">DESCRIPTION</span></span>
<span data-ttu-id="15723-106">Il cmdlet **Get-AzureRmExpressRouteServiceProvider** recupera un elenco dei provider di servizi di ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="15723-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="15723-107">Gli attributi includono le opzioni di posizione e larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="15723-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="15723-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15723-108">EXAMPLES</span></span>

### <span data-ttu-id="15723-109">Esempio 1: ottenere un elenco di provider di servizi con posizioni in "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="15723-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="15723-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15723-110">PARAMETERS</span></span>

### <span data-ttu-id="15723-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15723-111">-DefaultProfile</span></span>
<span data-ttu-id="15723-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15723-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15723-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15723-113">CommonParameters</span></span>
<span data-ttu-id="15723-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15723-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15723-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15723-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15723-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15723-116">INPUTS</span></span>

### <span data-ttu-id="15723-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="15723-117">None</span></span>
<span data-ttu-id="15723-118">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="15723-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="15723-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15723-119">OUTPUTS</span></span>

### <span data-ttu-id="15723-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="15723-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="15723-121">Note</span><span class="sxs-lookup"><span data-stu-id="15723-121">NOTES</span></span>

## <span data-ttu-id="15723-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15723-122">RELATED LINKS</span></span>

[<span data-ttu-id="15723-123">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="15723-123">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="15723-124">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="15723-124">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="15723-125">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="15723-125">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="15723-126">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="15723-126">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
