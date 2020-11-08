---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 15b02ce4693e452bda370c9fb1ae9c69012e9574
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201808"
---
# <span data-ttu-id="79609-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="79609-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="79609-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79609-102">SYNOPSIS</span></span>
<span data-ttu-id="79609-103">Ottiene statistiche sull'utilizzo di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="79609-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="79609-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79609-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79609-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79609-105">DESCRIPTION</span></span>
<span data-ttu-id="79609-106">Il cmdlet **Get-AzExpressRouteCircuitStat** recupera le statistiche del traffico per un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="79609-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="79609-107">Le statistiche includono il numero di byte inviati e ricevuti sia sulle route primarie che secondarie.</span><span class="sxs-lookup"><span data-stu-id="79609-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="79609-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79609-108">EXAMPLES</span></span>

### <span data-ttu-id="79609-109">Esempio 1: visualizzare le statistiche del traffico per un peer ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="79609-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="79609-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79609-110">PARAMETERS</span></span>

### <span data-ttu-id="79609-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79609-111">-DefaultProfile</span></span>
<span data-ttu-id="79609-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79609-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79609-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="79609-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="79609-114">Nome del circuito di ExpressRoute esaminato.</span><span class="sxs-lookup"><span data-stu-id="79609-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="79609-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="79609-115">-PeeringType</span></span>
<span data-ttu-id="79609-116">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="79609-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="79609-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79609-117">-ResourceGroupName</span></span>
<span data-ttu-id="79609-118">Nome del gruppo di risorse contenente il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="79609-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="79609-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79609-119">CommonParameters</span></span>
<span data-ttu-id="79609-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79609-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79609-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79609-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79609-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79609-122">INPUTS</span></span>

### <span data-ttu-id="79609-123">System. String</span><span class="sxs-lookup"><span data-stu-id="79609-123">System.String</span></span>

## <span data-ttu-id="79609-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79609-124">OUTPUTS</span></span>

### <span data-ttu-id="79609-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="79609-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="79609-126">Note</span><span class="sxs-lookup"><span data-stu-id="79609-126">NOTES</span></span>

## <span data-ttu-id="79609-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79609-127">RELATED LINKS</span></span>

[<span data-ttu-id="79609-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="79609-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="79609-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="79609-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="79609-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="79609-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
