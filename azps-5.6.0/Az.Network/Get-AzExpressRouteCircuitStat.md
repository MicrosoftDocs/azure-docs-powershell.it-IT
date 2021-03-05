---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: e0f4b24581860f17024c9b01e62b3c84616c6f81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997735"
---
# <span data-ttu-id="ddf7f-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="ddf7f-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="ddf7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddf7f-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf7f-103">Recupera le statistiche di utilizzo di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ddf7f-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ddf7f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddf7f-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddf7f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ddf7f-105">DESCRIPTION</span></span>
<span data-ttu-id="ddf7f-106">Il cmdlet **Get-AzExpressRouteCircuitStat** recupera le statistiche di traffico per un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ddf7f-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="ddf7f-107">Le statistiche includono il numero di byte inviati e ricevuti sulle route primaria e secondaria.</span><span class="sxs-lookup"><span data-stu-id="ddf7f-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="ddf7f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddf7f-108">EXAMPLES</span></span>

### <span data-ttu-id="ddf7f-109">Esempio 1: Visualizzare le statistiche di traffico per un peer ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ddf7f-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="ddf7f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddf7f-110">PARAMETERS</span></span>

### <span data-ttu-id="ddf7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf7f-111">-DefaultProfile</span></span>
<span data-ttu-id="ddf7f-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddf7f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddf7f-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="ddf7f-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="ddf7f-114">Nome del circuito ExpressRoute da esaminare.</span><span class="sxs-lookup"><span data-stu-id="ddf7f-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="ddf7f-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ddf7f-115">-PeeringType</span></span>
<span data-ttu-id="ddf7f-116">I valori accettabili per questo parametro sono: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ddf7f-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ddf7f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf7f-117">-ResourceGroupName</span></span>
<span data-ttu-id="ddf7f-118">Nome del gruppo di risorse che contiene il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ddf7f-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="ddf7f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf7f-119">CommonParameters</span></span>
<span data-ttu-id="ddf7f-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf7f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf7f-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ddf7f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf7f-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="ddf7f-122">INPUTS</span></span>

### <span data-ttu-id="ddf7f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="ddf7f-123">System.String</span></span>

## <span data-ttu-id="ddf7f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddf7f-124">OUTPUTS</span></span>

### <span data-ttu-id="ddf7f-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="ddf7f-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="ddf7f-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="ddf7f-126">NOTES</span></span>

## <span data-ttu-id="ddf7f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddf7f-127">RELATED LINKS</span></span>

[<span data-ttu-id="ddf7f-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ddf7f-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="ddf7f-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ddf7f-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="ddf7f-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ddf7f-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
