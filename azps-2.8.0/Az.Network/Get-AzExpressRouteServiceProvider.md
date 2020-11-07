---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: afa217565dc90bed1f047bc18b9407141b98dd0c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853734"
---
# <span data-ttu-id="ff6d4-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ff6d4-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="ff6d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff6d4-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6d4-103">Ottiene un elenco dei provider di servizi ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="ff6d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff6d4-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff6d4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff6d4-105">DESCRIPTION</span></span>
<span data-ttu-id="ff6d4-106">Il cmdlet **Get-AzExpressRouteServiceProvider** recupera un elenco dei provider di servizi di ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="ff6d4-107">Gli attributi includono le opzioni di posizione e larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="ff6d4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff6d4-108">EXAMPLES</span></span>

### <span data-ttu-id="ff6d4-109">Esempio 1: ottenere un elenco di provider di servizi con posizioni in "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="ff6d4-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="ff6d4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff6d4-110">PARAMETERS</span></span>

### <span data-ttu-id="ff6d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff6d4-111">-DefaultProfile</span></span>
<span data-ttu-id="ff6d4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff6d4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6d4-113">CommonParameters</span></span>
<span data-ttu-id="ff6d4-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6d4-115">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff6d4-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6d4-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff6d4-116">INPUTS</span></span>

### <span data-ttu-id="ff6d4-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ff6d4-117">None</span></span>

## <span data-ttu-id="ff6d4-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff6d4-118">OUTPUTS</span></span>

### <span data-ttu-id="ff6d4-119">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ff6d4-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="ff6d4-120">Note</span><span class="sxs-lookup"><span data-stu-id="ff6d4-120">NOTES</span></span>

## <span data-ttu-id="ff6d4-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff6d4-121">RELATED LINKS</span></span>

[<span data-ttu-id="ff6d4-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ff6d4-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="ff6d4-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff6d4-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="ff6d4-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ff6d4-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="ff6d4-125">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="ff6d4-125">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
