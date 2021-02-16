---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 7871625f9313179523fd4fad146107690f68a826
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412521"
---
# <span data-ttu-id="89c0b-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="89c0b-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="89c0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="89c0b-103">Ottiene un elenco di provider di servizi ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="89c0b-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="89c0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89c0b-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89c0b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="89c0b-105">DESCRIPTION</span></span>
<span data-ttu-id="89c0b-106">Il cmdlet **Get-AzExpressRouteServiceProvider** recupera un elenco di provider di servizi ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="89c0b-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="89c0b-107">L'attributo include opzioni per la posizione e la larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="89c0b-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="89c0b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89c0b-108">EXAMPLES</span></span>

### <span data-ttu-id="89c0b-109">Esempio 1: Ottenere un elenco di provider di servizi con posizioni nella "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="89c0b-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="89c0b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89c0b-110">PARAMETERS</span></span>

### <span data-ttu-id="89c0b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c0b-111">-DefaultProfile</span></span>
<span data-ttu-id="89c0b-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89c0b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89c0b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c0b-113">CommonParameters</span></span>
<span data-ttu-id="89c0b-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89c0b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c0b-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="89c0b-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c0b-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="89c0b-116">INPUTS</span></span>

### <span data-ttu-id="89c0b-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="89c0b-117">None</span></span>

## <span data-ttu-id="89c0b-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89c0b-118">OUTPUTS</span></span>

### <span data-ttu-id="89c0b-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="89c0b-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="89c0b-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="89c0b-120">NOTES</span></span>

## <span data-ttu-id="89c0b-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89c0b-121">RELATED LINKS</span></span>

[<span data-ttu-id="89c0b-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="89c0b-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="89c0b-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="89c0b-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="89c0b-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="89c0b-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="89c0b-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="89c0b-125">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
