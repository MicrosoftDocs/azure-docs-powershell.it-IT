---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: d88468647b02f2de3c5aba81d6829a6931df5750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688522"
---
# <span data-ttu-id="2ce2a-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2ce2a-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="2ce2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ce2a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce2a-103">Ottiene una configurazione peering Circuit ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2ce2a-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ce2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ce2a-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ce2a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ce2a-105">DESCRIPTION</span></span>
<span data-ttu-id="2ce2a-106">Il cmdlet **Get-AzureRmExpressRouteCircuitPeeringConfig** recupera la configurazione di una relazione di peering per un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2ce2a-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2ce2a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ce2a-107">EXAMPLES</span></span>

### <span data-ttu-id="2ce2a-108">Esempio 1: visualizzare la configurazione peering per un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="2ce2a-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="2ce2a-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ce2a-109">PARAMETERS</span></span>

### <span data-ttu-id="2ce2a-110">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2ce2a-110">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2ce2a-111">L'oggetto Circuit ExpressRoute che contiene la configurazione peering.</span><span class="sxs-lookup"><span data-stu-id="2ce2a-111">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="2ce2a-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ce2a-112">-Name</span></span>
<span data-ttu-id="2ce2a-113">Nome della configurazione peer da recuperare.</span><span class="sxs-lookup"><span data-stu-id="2ce2a-113">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="2ce2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce2a-114">-DefaultProfile</span></span>
<span data-ttu-id="2ce2a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ce2a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce2a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce2a-116">CommonParameters</span></span>
<span data-ttu-id="2ce2a-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ce2a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce2a-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ce2a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce2a-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ce2a-119">INPUTS</span></span>

### <span data-ttu-id="2ce2a-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2ce2a-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="2ce2a-121">Il parametro ' ExpressRouteCircuit ' accetta il valore di tipo ' PSExpressRouteCircuit ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2ce2a-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="2ce2a-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ce2a-122">OUTPUTS</span></span>

### <span data-ttu-id="2ce2a-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="2ce2a-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="2ce2a-124">Note</span><span class="sxs-lookup"><span data-stu-id="2ce2a-124">NOTES</span></span>

## <span data-ttu-id="2ce2a-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ce2a-125">RELATED LINKS</span></span>

[<span data-ttu-id="2ce2a-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2ce2a-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="2ce2a-127">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2ce2a-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="2ce2a-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2ce2a-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="2ce2a-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2ce2a-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
