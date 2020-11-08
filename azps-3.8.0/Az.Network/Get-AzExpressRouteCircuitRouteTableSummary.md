---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 78807c8504452479eef0cbe25a8e33cb017f4b9e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021334"
---
# <span data-ttu-id="f1186-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f1186-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="f1186-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1186-102">SYNOPSIS</span></span>
<span data-ttu-id="f1186-103">Ottiene un riepilogo della tabella di route di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f1186-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f1186-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1186-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1186-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1186-105">DESCRIPTION</span></span>
<span data-ttu-id="f1186-106">Il cmdlet **Get-AzExpressRouteCircuitRouteTableSummary** recupera un riepilogo delle informazioni adiacenti BGP per un particolare contesto di routing.</span><span class="sxs-lookup"><span data-stu-id="f1186-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="f1186-107">Queste informazioni sono utili per determinare per quanto tempo è stato stabilito un contesto di routing e il numero di prefissi di route pubblicizzati dal router peering.</span><span class="sxs-lookup"><span data-stu-id="f1186-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="f1186-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1186-108">EXAMPLES</span></span>

### <span data-ttu-id="f1186-109">Esempio 1: visualizzare il riepilogo della route per il percorso principale</span><span class="sxs-lookup"><span data-stu-id="f1186-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="f1186-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1186-110">PARAMETERS</span></span>

### <span data-ttu-id="f1186-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1186-111">-DefaultProfile</span></span>
<span data-ttu-id="f1186-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1186-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1186-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="f1186-113">-DevicePath</span></span>
<span data-ttu-id="f1186-114">I valori accettabili per questo parametro sono: `Primary` o `Secondary`</span><span class="sxs-lookup"><span data-stu-id="f1186-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="f1186-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="f1186-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="f1186-116">Nome del circuito di ExpressRoute esaminato.</span><span class="sxs-lookup"><span data-stu-id="f1186-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="f1186-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f1186-117">-PeeringType</span></span>
<span data-ttu-id="f1186-118">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f1186-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="f1186-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1186-119">-ResourceGroupName</span></span>
<span data-ttu-id="f1186-120">Nome del gruppo di risorse contenente il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f1186-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="f1186-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1186-121">CommonParameters</span></span>
<span data-ttu-id="f1186-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1186-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1186-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1186-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1186-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1186-124">INPUTS</span></span>

### <span data-ttu-id="f1186-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f1186-125">System.String</span></span>

## <span data-ttu-id="f1186-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1186-126">OUTPUTS</span></span>

### <span data-ttu-id="f1186-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="f1186-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="f1186-128">Note</span><span class="sxs-lookup"><span data-stu-id="f1186-128">NOTES</span></span>

## <span data-ttu-id="f1186-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1186-129">RELATED LINKS</span></span>

[<span data-ttu-id="f1186-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f1186-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="f1186-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1186-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="f1186-132">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="f1186-132">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
