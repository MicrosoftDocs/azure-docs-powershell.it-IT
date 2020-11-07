---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c8e821408f3d65ace31ab2340f544a0a47e120e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853249"
---
# <span data-ttu-id="780e5-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="780e5-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="780e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="780e5-102">SYNOPSIS</span></span>
<span data-ttu-id="780e5-103">Ottiene una configurazione peering Circuit ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="780e5-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="780e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="780e5-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="780e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="780e5-105">DESCRIPTION</span></span>
<span data-ttu-id="780e5-106">Il cmdlet **Get-AzExpressRouteCircuitPeeringConfig** recupera la configurazione di una relazione di peering per un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="780e5-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="780e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="780e5-107">EXAMPLES</span></span>

### <span data-ttu-id="780e5-108">Esempio 1: visualizzare la configurazione peering per un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="780e5-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="780e5-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="780e5-109">PARAMETERS</span></span>

### <span data-ttu-id="780e5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="780e5-110">-DefaultProfile</span></span>
<span data-ttu-id="780e5-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="780e5-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="780e5-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="780e5-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="780e5-113">L'oggetto Circuit ExpressRoute che contiene la configurazione peering.</span><span class="sxs-lookup"><span data-stu-id="780e5-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="780e5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="780e5-114">-Name</span></span>
<span data-ttu-id="780e5-115">Nome della configurazione peer da recuperare.</span><span class="sxs-lookup"><span data-stu-id="780e5-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780e5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="780e5-116">CommonParameters</span></span>
<span data-ttu-id="780e5-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="780e5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="780e5-118">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="780e5-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="780e5-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="780e5-119">INPUTS</span></span>

### <span data-ttu-id="780e5-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="780e5-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="780e5-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="780e5-121">OUTPUTS</span></span>

### <span data-ttu-id="780e5-122">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="780e5-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="780e5-123">Note</span><span class="sxs-lookup"><span data-stu-id="780e5-123">NOTES</span></span>

## <span data-ttu-id="780e5-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="780e5-124">RELATED LINKS</span></span>

[<span data-ttu-id="780e5-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="780e5-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="780e5-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="780e5-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="780e5-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="780e5-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="780e5-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="780e5-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
