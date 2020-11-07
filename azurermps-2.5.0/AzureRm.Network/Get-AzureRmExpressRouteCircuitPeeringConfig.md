---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 187b7848dc3634ee67521e03f46f4684f23b9913
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866087"
---
# <span data-ttu-id="60a20-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="60a20-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="60a20-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60a20-102">SYNOPSIS</span></span>
<span data-ttu-id="60a20-103">Ottiene una configurazione peering Circuit ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60a20-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60a20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60a20-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60a20-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60a20-105">DESCRIPTION</span></span>
<span data-ttu-id="60a20-106">Il cmdlet **Get-AzureRmExpressRouteCircuitPeeringConfig** recupera la configurazione di una relazione di peering per un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60a20-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="60a20-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60a20-107">EXAMPLES</span></span>

### <span data-ttu-id="60a20-108">Esempio 1: visualizzare la configurazione peering per un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="60a20-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="60a20-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60a20-109">PARAMETERS</span></span>

### <span data-ttu-id="60a20-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a20-110">-DefaultProfile</span></span>
<span data-ttu-id="60a20-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60a20-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60a20-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60a20-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="60a20-113">L'oggetto Circuit ExpressRoute che contiene la configurazione peering.</span><span class="sxs-lookup"><span data-stu-id="60a20-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60a20-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="60a20-114">-Name</span></span>
<span data-ttu-id="60a20-115">Nome della configurazione peer da recuperare.</span><span class="sxs-lookup"><span data-stu-id="60a20-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a20-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a20-116">CommonParameters</span></span>
<span data-ttu-id="60a20-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a20-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a20-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a20-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a20-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60a20-119">INPUTS</span></span>

### <span data-ttu-id="60a20-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60a20-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="60a20-121">Il parametro ' ExpressRouteCircuit ' accetta il valore di tipo ' PSExpressRouteCircuit ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="60a20-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="60a20-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60a20-122">OUTPUTS</span></span>

### <span data-ttu-id="60a20-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="60a20-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="60a20-124">Note</span><span class="sxs-lookup"><span data-stu-id="60a20-124">NOTES</span></span>

## <span data-ttu-id="60a20-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60a20-125">RELATED LINKS</span></span>

[<span data-ttu-id="60a20-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="60a20-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="60a20-127">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="60a20-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="60a20-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="60a20-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="60a20-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60a20-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
