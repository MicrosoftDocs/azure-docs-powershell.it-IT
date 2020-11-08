---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: fe92609b47cadedd1772b1a75baae33b9fb89e65
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021335"
---
# <span data-ttu-id="2c323-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2c323-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="2c323-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c323-102">SYNOPSIS</span></span>
<span data-ttu-id="2c323-103">Ottiene una tabella di route da un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2c323-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2c323-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c323-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c323-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c323-105">DESCRIPTION</span></span>
<span data-ttu-id="2c323-106">Il cmdlet **Get-AzExpressRouteCircuitRouteTable** recupera una tabella di route dettagliata di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2c323-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="2c323-107">La tabella route mostrerà tutte le route o può essere filtrata per visualizzare le route per un tipo di peering specifico.</span><span class="sxs-lookup"><span data-stu-id="2c323-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="2c323-108">È possibile usare la tabella route per convalidare la configurazione e la connettività di peering.</span><span class="sxs-lookup"><span data-stu-id="2c323-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="2c323-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c323-109">EXAMPLES</span></span>

### <span data-ttu-id="2c323-110">Esempio 1: visualizzare la tabella route per il percorso principale</span><span class="sxs-lookup"><span data-stu-id="2c323-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="2c323-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c323-111">PARAMETERS</span></span>

### <span data-ttu-id="2c323-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c323-112">-DefaultProfile</span></span>
<span data-ttu-id="2c323-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c323-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c323-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="2c323-114">-DevicePath</span></span>
<span data-ttu-id="2c323-115">I valori accettabili per questo parametro sono: `Primary` o `Secondary`</span><span class="sxs-lookup"><span data-stu-id="2c323-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="2c323-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="2c323-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="2c323-117">Nome del circuito di ExpressRoute esaminato.</span><span class="sxs-lookup"><span data-stu-id="2c323-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="2c323-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="2c323-118">-PeeringType</span></span>
<span data-ttu-id="2c323-119">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="2c323-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="2c323-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c323-120">-ResourceGroupName</span></span>
<span data-ttu-id="2c323-121">Nome del gruppo di risorse contenente il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2c323-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="2c323-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c323-122">CommonParameters</span></span>
<span data-ttu-id="2c323-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c323-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c323-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c323-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c323-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c323-125">INPUTS</span></span>

### <span data-ttu-id="2c323-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2c323-126">System.String</span></span>

## <span data-ttu-id="2c323-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c323-127">OUTPUTS</span></span>

### <span data-ttu-id="2c323-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="2c323-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="2c323-129">Note</span><span class="sxs-lookup"><span data-stu-id="2c323-129">NOTES</span></span>

## <span data-ttu-id="2c323-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c323-130">RELATED LINKS</span></span>

[<span data-ttu-id="2c323-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2c323-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="2c323-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2c323-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="2c323-133">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="2c323-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
