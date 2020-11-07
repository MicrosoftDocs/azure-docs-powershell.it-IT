---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5feeba4ffb4f73365e9b6df86a03e8920b74f88e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860310"
---
# <span data-ttu-id="329e7-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="329e7-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="329e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="329e7-102">SYNOPSIS</span></span>
<span data-ttu-id="329e7-103">Rimuove una configurazione peering Circuit ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="329e7-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="329e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="329e7-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="329e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="329e7-105">DESCRIPTION</span></span>
<span data-ttu-id="329e7-106">Il cmdlet **Remove-AzExpressRouteCircuitPeeringConfig** rimuove una configurazione peering Circuit ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="329e7-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="329e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="329e7-107">EXAMPLES</span></span>

### <span data-ttu-id="329e7-108">Esempio 1: rimuovere una configurazione peering da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="329e7-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="329e7-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="329e7-109">PARAMETERS</span></span>

### <span data-ttu-id="329e7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="329e7-110">-DefaultProfile</span></span>
<span data-ttu-id="329e7-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="329e7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="329e7-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="329e7-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="329e7-113">Il circuito ExpressRoute che contiene la configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="329e7-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="329e7-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="329e7-114">-Name</span></span>
<span data-ttu-id="329e7-115">Nome della configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="329e7-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="329e7-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="329e7-116">-PeerAddressType</span></span>
<span data-ttu-id="329e7-117">Famiglia di indirizzi del peering</span><span class="sxs-lookup"><span data-stu-id="329e7-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="329e7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="329e7-118">CommonParameters</span></span>
<span data-ttu-id="329e7-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="329e7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="329e7-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="329e7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="329e7-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="329e7-121">INPUTS</span></span>

### <span data-ttu-id="329e7-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="329e7-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="329e7-123">Il parametro ' ExpressRouteCircuit ' accetta il valore di tipo ' PSExpressRouteCircuit ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="329e7-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="329e7-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="329e7-124">OUTPUTS</span></span>

### <span data-ttu-id="329e7-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="329e7-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="329e7-126">Note</span><span class="sxs-lookup"><span data-stu-id="329e7-126">NOTES</span></span>

## <span data-ttu-id="329e7-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="329e7-127">RELATED LINKS</span></span>

[<span data-ttu-id="329e7-128">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="329e7-128">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="329e7-129">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="329e7-129">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="329e7-130">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="329e7-130">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="329e7-131">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="329e7-131">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
