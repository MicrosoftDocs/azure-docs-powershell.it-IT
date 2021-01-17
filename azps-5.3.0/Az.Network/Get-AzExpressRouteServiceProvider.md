---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476059"
---
# <span data-ttu-id="fdc33-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="fdc33-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="fdc33-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdc33-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc33-103">Ottiene un elenco dei provider di servizi ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="fdc33-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="fdc33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdc33-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdc33-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdc33-105">DESCRIPTION</span></span>
<span data-ttu-id="fdc33-106">Il cmdlet **Get-AzExpressRouteServiceProvider** recupera un elenco dei provider di servizi di ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="fdc33-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="fdc33-107">Gli attributi includono le opzioni di posizione e larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="fdc33-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="fdc33-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdc33-108">EXAMPLES</span></span>

### <span data-ttu-id="fdc33-109">Esempio 1: ottenere un elenco di provider di servizi con posizioni in "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="fdc33-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="fdc33-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdc33-110">PARAMETERS</span></span>

### <span data-ttu-id="fdc33-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc33-111">-DefaultProfile</span></span>
<span data-ttu-id="fdc33-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdc33-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdc33-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc33-113">CommonParameters</span></span>
<span data-ttu-id="fdc33-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdc33-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc33-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdc33-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc33-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdc33-116">INPUTS</span></span>

### <span data-ttu-id="fdc33-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fdc33-117">None</span></span>

## <span data-ttu-id="fdc33-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdc33-118">OUTPUTS</span></span>

### <span data-ttu-id="fdc33-119">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="fdc33-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="fdc33-120">Note</span><span class="sxs-lookup"><span data-stu-id="fdc33-120">NOTES</span></span>

## <span data-ttu-id="fdc33-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdc33-121">RELATED LINKS</span></span>

[<span data-ttu-id="fdc33-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="fdc33-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="fdc33-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="fdc33-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="fdc33-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fdc33-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="fdc33-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="fdc33-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
