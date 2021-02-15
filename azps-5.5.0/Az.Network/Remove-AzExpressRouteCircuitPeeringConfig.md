---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 0a0d23824b82b6a150b9547ef41c106ef237671b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186959"
---
# <span data-ttu-id="cf53f-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cf53f-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="cf53f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf53f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf53f-103">Rimuove una configurazione di peering del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cf53f-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="cf53f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf53f-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf53f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cf53f-105">DESCRIPTION</span></span>
<span data-ttu-id="cf53f-106">Il cmdlet **Remove-AzExpressRouteCircuitConfigingConfig** rimuove una configurazione di peering del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cf53f-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="cf53f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf53f-107">EXAMPLES</span></span>

### <span data-ttu-id="cf53f-108">Esempio 1: Rimuovere una configurazione di peering da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="cf53f-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="cf53f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf53f-109">PARAMETERS</span></span>

### <span data-ttu-id="cf53f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf53f-110">-DefaultProfile</span></span>
<span data-ttu-id="cf53f-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf53f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf53f-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cf53f-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="cf53f-113">Circuito ExpressRoute contenente la configurazione di peering da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="cf53f-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="cf53f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="cf53f-114">-Name</span></span>
<span data-ttu-id="cf53f-115">Nome della configurazione di peering da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="cf53f-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="cf53f-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="cf53f-116">-PeerAddressType</span></span>
<span data-ttu-id="cf53f-117">Famiglia di indirizzi del peering</span><span class="sxs-lookup"><span data-stu-id="cf53f-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="cf53f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf53f-118">CommonParameters</span></span>
<span data-ttu-id="cf53f-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf53f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf53f-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf53f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf53f-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="cf53f-121">INPUTS</span></span>

### <span data-ttu-id="cf53f-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cf53f-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="cf53f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf53f-123">OUTPUTS</span></span>

### <span data-ttu-id="cf53f-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cf53f-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="cf53f-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="cf53f-125">NOTES</span></span>

## <span data-ttu-id="cf53f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf53f-126">RELATED LINKS</span></span>

[<span data-ttu-id="cf53f-127">Add-AzExpressRouteCircuit DigitaingConfig</span><span class="sxs-lookup"><span data-stu-id="cf53f-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cf53f-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cf53f-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="cf53f-129">New-AzExpressRouteCircuit DigitaingConfig</span><span class="sxs-lookup"><span data-stu-id="cf53f-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cf53f-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cf53f-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
