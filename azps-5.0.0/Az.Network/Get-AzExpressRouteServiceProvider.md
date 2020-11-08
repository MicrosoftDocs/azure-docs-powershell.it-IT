---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193218"
---
# <span data-ttu-id="f4559-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="f4559-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="f4559-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4559-102">SYNOPSIS</span></span>
<span data-ttu-id="f4559-103">Ottiene un elenco dei provider di servizi ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="f4559-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="f4559-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4559-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4559-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4559-105">DESCRIPTION</span></span>
<span data-ttu-id="f4559-106">Il cmdlet **Get-AzExpressRouteServiceProvider** recupera un elenco dei provider di servizi di ExpressRoute e i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="f4559-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="f4559-107">Gli attributi includono le opzioni di posizione e larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="f4559-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="f4559-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4559-108">EXAMPLES</span></span>

### <span data-ttu-id="f4559-109">Esempio 1: ottenere un elenco di provider di servizi con posizioni in "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="f4559-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="f4559-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4559-110">PARAMETERS</span></span>

### <span data-ttu-id="f4559-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4559-111">-DefaultProfile</span></span>
<span data-ttu-id="f4559-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4559-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4559-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4559-113">CommonParameters</span></span>
<span data-ttu-id="f4559-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4559-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4559-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4559-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4559-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4559-116">INPUTS</span></span>

### <span data-ttu-id="f4559-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f4559-117">None</span></span>

## <span data-ttu-id="f4559-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4559-118">OUTPUTS</span></span>

### <span data-ttu-id="f4559-119">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="f4559-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="f4559-120">Note</span><span class="sxs-lookup"><span data-stu-id="f4559-120">NOTES</span></span>

## <span data-ttu-id="f4559-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4559-121">RELATED LINKS</span></span>

[<span data-ttu-id="f4559-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f4559-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="f4559-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f4559-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="f4559-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f4559-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="f4559-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="f4559-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
