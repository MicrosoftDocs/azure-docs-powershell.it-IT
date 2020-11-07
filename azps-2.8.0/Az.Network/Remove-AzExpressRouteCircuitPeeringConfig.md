---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c7d60c3d2f69e7ea18bcd256d8ad4a943817769a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854293"
---
# <span data-ttu-id="3e712-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3e712-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="3e712-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e712-102">SYNOPSIS</span></span>
<span data-ttu-id="3e712-103">Rimuove una configurazione peering Circuit ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3e712-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="3e712-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e712-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e712-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e712-105">DESCRIPTION</span></span>
<span data-ttu-id="3e712-106">Il cmdlet **Remove-AzExpressRouteCircuitPeeringConfig** rimuove una configurazione peering Circuit ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3e712-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="3e712-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e712-107">EXAMPLES</span></span>

### <span data-ttu-id="3e712-108">Esempio 1: rimuovere una configurazione peering da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3e712-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="3e712-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e712-109">PARAMETERS</span></span>

### <span data-ttu-id="3e712-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e712-110">-DefaultProfile</span></span>
<span data-ttu-id="3e712-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e712-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e712-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e712-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3e712-113">Il circuito ExpressRoute che contiene la configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3e712-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="3e712-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e712-114">-Name</span></span>
<span data-ttu-id="3e712-115">Nome della configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3e712-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="3e712-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="3e712-116">-PeerAddressType</span></span>
<span data-ttu-id="3e712-117">Famiglia di indirizzi del peering</span><span class="sxs-lookup"><span data-stu-id="3e712-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="3e712-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e712-118">CommonParameters</span></span>
<span data-ttu-id="3e712-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e712-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e712-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e712-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e712-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e712-121">INPUTS</span></span>

### <span data-ttu-id="3e712-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e712-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3e712-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e712-123">OUTPUTS</span></span>

### <span data-ttu-id="3e712-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e712-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3e712-125">Note</span><span class="sxs-lookup"><span data-stu-id="3e712-125">NOTES</span></span>

## <span data-ttu-id="3e712-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e712-126">RELATED LINKS</span></span>

[<span data-ttu-id="3e712-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3e712-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3e712-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e712-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="3e712-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3e712-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3e712-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e712-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
