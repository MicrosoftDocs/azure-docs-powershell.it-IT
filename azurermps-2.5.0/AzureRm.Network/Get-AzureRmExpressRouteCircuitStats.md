---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
ms.openlocfilehash: 68579ea2adecbf7ad6a97fd11f4f32da9adeb48f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866889"
---
# <span data-ttu-id="12784-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="12784-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="12784-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12784-102">SYNOPSIS</span></span>
<span data-ttu-id="12784-103">Ottiene statistiche sull'utilizzo di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="12784-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12784-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12784-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12784-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12784-105">DESCRIPTION</span></span>
<span data-ttu-id="12784-106">Il cmdlet **Get-AzureRmExpressRouteCircuitStats** recupera le statistiche del traffico per un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="12784-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="12784-107">Le statistiche includono il numero di byte inviati e ricevuti sia sulle route primarie che secondarie.</span><span class="sxs-lookup"><span data-stu-id="12784-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="12784-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12784-108">EXAMPLES</span></span>

### <span data-ttu-id="12784-109">Esempio 1: visualizzare le statistiche del traffico per un peer ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="12784-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="12784-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12784-110">PARAMETERS</span></span>

### <span data-ttu-id="12784-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12784-111">-DefaultProfile</span></span>
<span data-ttu-id="12784-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12784-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12784-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="12784-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="12784-114">Nome del circuito di ExpressRoute esaminato.</span><span class="sxs-lookup"><span data-stu-id="12784-114">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12784-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="12784-115">-PeeringType</span></span>
<span data-ttu-id="12784-116">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="12784-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12784-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12784-117">-ResourceGroupName</span></span>
<span data-ttu-id="12784-118">Nome del gruppo di risorse contenente il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="12784-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12784-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12784-119">CommonParameters</span></span>
<span data-ttu-id="12784-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12784-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12784-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12784-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12784-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12784-122">INPUTS</span></span>

## <span data-ttu-id="12784-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12784-123">OUTPUTS</span></span>

### <span data-ttu-id="12784-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="12784-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="12784-125">Note</span><span class="sxs-lookup"><span data-stu-id="12784-125">NOTES</span></span>

## <span data-ttu-id="12784-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12784-126">RELATED LINKS</span></span>

[<span data-ttu-id="12784-127">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="12784-127">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="12784-128">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="12784-128">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="12784-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="12784-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
