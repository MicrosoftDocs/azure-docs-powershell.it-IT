---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 187921598b21747764436dd4ae6f988961d4a951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996405"
---
# <span data-ttu-id="aaed9-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="aaed9-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="aaed9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaed9-102">SYNOPSIS</span></span>
<span data-ttu-id="aaed9-103">Rimuove una configurazione di peering del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="aaed9-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="aaed9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaed9-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaed9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aaed9-105">DESCRIPTION</span></span>
<span data-ttu-id="aaed9-106">Il cmdlet **Remove-AzExpressRouteCircuitConfigingConfig** rimuove una configurazione di peering del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="aaed9-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="aaed9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaed9-107">EXAMPLES</span></span>

### <span data-ttu-id="aaed9-108">Esempio 1: Rimuovere una configurazione di peering da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="aaed9-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="aaed9-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaed9-109">PARAMETERS</span></span>

### <span data-ttu-id="aaed9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaed9-110">-DefaultProfile</span></span>
<span data-ttu-id="aaed9-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aaed9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaed9-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aaed9-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="aaed9-113">Circuito ExpressRoute contenente la configurazione di peering da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="aaed9-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="aaed9-114">-Name</span><span class="sxs-lookup"><span data-stu-id="aaed9-114">-Name</span></span>
<span data-ttu-id="aaed9-115">Nome della configurazione di peering da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="aaed9-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="aaed9-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="aaed9-116">-PeerAddressType</span></span>
<span data-ttu-id="aaed9-117">Famiglia di indirizzi del peering</span><span class="sxs-lookup"><span data-stu-id="aaed9-117">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaed9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaed9-118">CommonParameters</span></span>
<span data-ttu-id="aaed9-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaed9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaed9-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaed9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaed9-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="aaed9-121">INPUTS</span></span>

### <span data-ttu-id="aaed9-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aaed9-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="aaed9-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaed9-123">OUTPUTS</span></span>

### <span data-ttu-id="aaed9-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aaed9-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="aaed9-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="aaed9-125">NOTES</span></span>

## <span data-ttu-id="aaed9-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaed9-126">RELATED LINKS</span></span>

[<span data-ttu-id="aaed9-127">Add-AzExpressRouteCircuit DigitaingConfig</span><span class="sxs-lookup"><span data-stu-id="aaed9-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="aaed9-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aaed9-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="aaed9-129">New-AzExpressRouteCircuit DigitaingConfig</span><span class="sxs-lookup"><span data-stu-id="aaed9-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="aaed9-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aaed9-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
