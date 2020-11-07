---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9c52ff23d4e92af0d1f62cdfc5d5fda01b3221da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860809"
---
# <span data-ttu-id="f2ee4-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f2ee4-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="f2ee4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ee4-103">Ottiene una configurazione peering Circuit ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f2ee4-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="f2ee4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2ee4-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2ee4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2ee4-105">DESCRIPTION</span></span>
<span data-ttu-id="f2ee4-106">Il cmdlet **Get-AzExpressRouteCircuitPeeringConfig** recupera la configurazione di una relazione di peering per un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f2ee4-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f2ee4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2ee4-107">EXAMPLES</span></span>

### <span data-ttu-id="f2ee4-108">Esempio 1: visualizzare la configurazione peering per un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f2ee4-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="f2ee4-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2ee4-109">PARAMETERS</span></span>

### <span data-ttu-id="f2ee4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ee4-110">-DefaultProfile</span></span>
<span data-ttu-id="f2ee4-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2ee4-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2ee4-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2ee4-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f2ee4-113">L'oggetto Circuit ExpressRoute che contiene la configurazione peering.</span><span class="sxs-lookup"><span data-stu-id="f2ee4-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="f2ee4-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2ee4-114">-Name</span></span>
<span data-ttu-id="f2ee4-115">Nome della configurazione peer da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f2ee4-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="f2ee4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ee4-116">CommonParameters</span></span>
<span data-ttu-id="f2ee4-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2ee4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ee4-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2ee4-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ee4-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2ee4-119">INPUTS</span></span>

### <span data-ttu-id="f2ee4-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2ee4-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="f2ee4-121">Il parametro ' ExpressRouteCircuit ' accetta il valore di tipo ' PSExpressRouteCircuit ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f2ee4-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="f2ee4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2ee4-122">OUTPUTS</span></span>

### <span data-ttu-id="f2ee4-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="f2ee4-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="f2ee4-124">Note</span><span class="sxs-lookup"><span data-stu-id="f2ee4-124">NOTES</span></span>

## <span data-ttu-id="f2ee4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2ee4-125">RELATED LINKS</span></span>

[<span data-ttu-id="f2ee4-126">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f2ee4-126">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f2ee4-127">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f2ee4-127">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f2ee4-128">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f2ee4-128">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f2ee4-129">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2ee4-129">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
