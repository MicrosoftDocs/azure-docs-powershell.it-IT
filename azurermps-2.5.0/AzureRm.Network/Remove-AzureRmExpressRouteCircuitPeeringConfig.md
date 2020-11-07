---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 749f1b84ed033e903d3e50652e6199f184fffa2b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866047"
---
# <span data-ttu-id="bab37-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="bab37-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="bab37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bab37-102">SYNOPSIS</span></span>
<span data-ttu-id="bab37-103">Rimuove una configurazione peering Circuit ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bab37-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bab37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bab37-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bab37-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bab37-105">DESCRIPTION</span></span>
<span data-ttu-id="bab37-106">Il cmdlet **Remove-AzureRmExpressRouteCircuitPeeringConfig** rimuove una configurazione peering Circuit ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bab37-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="bab37-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bab37-107">EXAMPLES</span></span>

### <span data-ttu-id="bab37-108">Esempio 1: rimuovere una configurazione peering da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="bab37-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="bab37-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bab37-109">PARAMETERS</span></span>

### <span data-ttu-id="bab37-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab37-110">-DefaultProfile</span></span>
<span data-ttu-id="bab37-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bab37-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bab37-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bab37-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="bab37-113">Il circuito ExpressRoute che contiene la configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="bab37-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="bab37-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="bab37-114">-Name</span></span>
<span data-ttu-id="bab37-115">Nome della configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="bab37-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="bab37-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="bab37-116">-PeerAddressType</span></span>
<span data-ttu-id="bab37-117">Famiglia di indirizzi del peering</span><span class="sxs-lookup"><span data-stu-id="bab37-117">The Address family of the peering</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab37-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab37-118">CommonParameters</span></span>
<span data-ttu-id="bab37-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bab37-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab37-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab37-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab37-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bab37-121">INPUTS</span></span>

### <span data-ttu-id="bab37-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bab37-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="bab37-123">Il parametro ' ExpressRouteCircuit ' accetta il valore di tipo ' PSExpressRouteCircuit ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bab37-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="bab37-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bab37-124">OUTPUTS</span></span>

### <span data-ttu-id="bab37-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bab37-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="bab37-126">Note</span><span class="sxs-lookup"><span data-stu-id="bab37-126">NOTES</span></span>

## <span data-ttu-id="bab37-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bab37-127">RELATED LINKS</span></span>

[<span data-ttu-id="bab37-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="bab37-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="bab37-129">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bab37-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="bab37-130">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="bab37-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="bab37-131">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bab37-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
