---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9996a42311ebfdf523b12822c1550b2faa78b6b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184742"
---
# <span data-ttu-id="5d71f-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="5d71f-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="5d71f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d71f-102">SYNOPSIS</span></span>
<span data-ttu-id="5d71f-103">Ottiene una configurazione di peering del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5d71f-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="5d71f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d71f-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d71f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5d71f-105">DESCRIPTION</span></span>
<span data-ttu-id="5d71f-106">Il cmdlet **Get-AzExpressRouteCircuit DigitaingConfig** recupera la configurazione di una relazione di peering per un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5d71f-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="5d71f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d71f-107">EXAMPLES</span></span>

### <span data-ttu-id="5d71f-108">Esempio 1: Visualizzare la configurazione del peering per un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="5d71f-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="5d71f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d71f-109">PARAMETERS</span></span>

### <span data-ttu-id="5d71f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d71f-110">-DefaultProfile</span></span>
<span data-ttu-id="5d71f-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d71f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d71f-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5d71f-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5d71f-113">Oggetto circuito ExpressRoute contenente la configurazione di peering.</span><span class="sxs-lookup"><span data-stu-id="5d71f-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="5d71f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="5d71f-114">-Name</span></span>
<span data-ttu-id="5d71f-115">Nome della configurazione di peering da recuperare.</span><span class="sxs-lookup"><span data-stu-id="5d71f-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="5d71f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d71f-116">CommonParameters</span></span>
<span data-ttu-id="5d71f-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d71f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d71f-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d71f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d71f-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="5d71f-119">INPUTS</span></span>

### <span data-ttu-id="5d71f-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5d71f-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5d71f-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d71f-121">OUTPUTS</span></span>

### <span data-ttu-id="5d71f-122">Microsoft.Azure.Commands.Network.Models.PSCollectioning</span><span class="sxs-lookup"><span data-stu-id="5d71f-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="5d71f-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="5d71f-123">NOTES</span></span>

## <span data-ttu-id="5d71f-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d71f-124">RELATED LINKS</span></span>

[<span data-ttu-id="5d71f-125">Add-AzExpressRouteCircuit DigitaingConfig</span><span class="sxs-lookup"><span data-stu-id="5d71f-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5d71f-126">New-AzExpressRouteCircuit DigitaingConfig</span><span class="sxs-lookup"><span data-stu-id="5d71f-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5d71f-127">Remove-AzExpressRouteCircuit DigitaingConfig</span><span class="sxs-lookup"><span data-stu-id="5d71f-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5d71f-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5d71f-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
