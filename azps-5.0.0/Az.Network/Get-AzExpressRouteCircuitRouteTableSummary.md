---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199692"
---
# <span data-ttu-id="bafb7-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bafb7-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="bafb7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bafb7-102">SYNOPSIS</span></span>
<span data-ttu-id="bafb7-103">Ottiene un riepilogo della tabella di route di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bafb7-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="bafb7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bafb7-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bafb7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bafb7-105">DESCRIPTION</span></span>
<span data-ttu-id="bafb7-106">Il cmdlet **Get-AzExpressRouteCircuitRouteTableSummary** recupera un riepilogo delle informazioni adiacenti BGP per un particolare contesto di routing.</span><span class="sxs-lookup"><span data-stu-id="bafb7-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="bafb7-107">Queste informazioni sono utili per determinare per quanto tempo è stato stabilito un contesto di routing e il numero di prefissi di route pubblicizzati dal router peering.</span><span class="sxs-lookup"><span data-stu-id="bafb7-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="bafb7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bafb7-108">EXAMPLES</span></span>

### <span data-ttu-id="bafb7-109">Esempio 1: visualizzare il riepilogo della route per il percorso principale</span><span class="sxs-lookup"><span data-stu-id="bafb7-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="bafb7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bafb7-110">PARAMETERS</span></span>

### <span data-ttu-id="bafb7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafb7-111">-DefaultProfile</span></span>
<span data-ttu-id="bafb7-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bafb7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bafb7-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="bafb7-113">-DevicePath</span></span>
<span data-ttu-id="bafb7-114">I valori accettabili per questo parametro sono: `Primary` o `Secondary`</span><span class="sxs-lookup"><span data-stu-id="bafb7-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafb7-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="bafb7-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="bafb7-116">Nome del circuito di ExpressRoute esaminato.</span><span class="sxs-lookup"><span data-stu-id="bafb7-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="bafb7-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="bafb7-117">-PeeringType</span></span>
<span data-ttu-id="bafb7-118">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="bafb7-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafb7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bafb7-119">-ResourceGroupName</span></span>
<span data-ttu-id="bafb7-120">Nome del gruppo di risorse contenente il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bafb7-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="bafb7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafb7-121">CommonParameters</span></span>
<span data-ttu-id="bafb7-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bafb7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafb7-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bafb7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafb7-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bafb7-124">INPUTS</span></span>

### <span data-ttu-id="bafb7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bafb7-125">System.String</span></span>

## <span data-ttu-id="bafb7-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bafb7-126">OUTPUTS</span></span>

### <span data-ttu-id="bafb7-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="bafb7-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="bafb7-128">Note</span><span class="sxs-lookup"><span data-stu-id="bafb7-128">NOTES</span></span>

## <span data-ttu-id="bafb7-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bafb7-129">RELATED LINKS</span></span>

[<span data-ttu-id="bafb7-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="bafb7-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="bafb7-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="bafb7-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="bafb7-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="bafb7-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
