---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: d9978c50186b520d8e956dc20581d1ceb615b673
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688087"
---
# <span data-ttu-id="fa76f-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="fa76f-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="fa76f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa76f-102">SYNOPSIS</span></span>
<span data-ttu-id="fa76f-103">Ottiene statistiche sull'utilizzo di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fa76f-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa76f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa76f-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa76f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa76f-105">DESCRIPTION</span></span>
<span data-ttu-id="fa76f-106">Il cmdlet **Get-AzureRmExpressRouteCircuitStats** recupera le statistiche del traffico per un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fa76f-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="fa76f-107">Le statistiche includono il numero di byte inviati e ricevuti sia sulle route primarie che secondarie.</span><span class="sxs-lookup"><span data-stu-id="fa76f-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="fa76f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa76f-108">EXAMPLES</span></span>

### <span data-ttu-id="fa76f-109">Esempio 1: visualizzare le statistiche del traffico per un peer ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="fa76f-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="fa76f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa76f-110">PARAMETERS</span></span>

### <span data-ttu-id="fa76f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa76f-111">-DefaultProfile</span></span>
<span data-ttu-id="fa76f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa76f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa76f-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="fa76f-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="fa76f-114">Nome del circuito di ExpressRoute esaminato.</span><span class="sxs-lookup"><span data-stu-id="fa76f-114">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa76f-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="fa76f-115">-PeeringType</span></span>
<span data-ttu-id="fa76f-116">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="fa76f-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa76f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa76f-117">-ResourceGroupName</span></span>
<span data-ttu-id="fa76f-118">Nome del gruppo di risorse contenente il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fa76f-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa76f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa76f-119">CommonParameters</span></span>
<span data-ttu-id="fa76f-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa76f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa76f-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa76f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa76f-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa76f-122">INPUTS</span></span>

### <span data-ttu-id="fa76f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="fa76f-123">System.String</span></span>

## <span data-ttu-id="fa76f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa76f-124">OUTPUTS</span></span>

### <span data-ttu-id="fa76f-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="fa76f-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="fa76f-126">Note</span><span class="sxs-lookup"><span data-stu-id="fa76f-126">NOTES</span></span>

## <span data-ttu-id="fa76f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa76f-127">RELATED LINKS</span></span>

[<span data-ttu-id="fa76f-128">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="fa76f-128">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="fa76f-129">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="fa76f-129">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="fa76f-130">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fa76f-130">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)