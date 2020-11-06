---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: b4e93b89a11d4341b6a04de1b5625084e9348c67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519566"
---
# <span data-ttu-id="0de55-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0de55-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="0de55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0de55-102">SYNOPSIS</span></span>
<span data-ttu-id="0de55-103">Ottiene un riepilogo della tabella di route di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0de55-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0de55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0de55-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0de55-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0de55-105">DESCRIPTION</span></span>
<span data-ttu-id="0de55-106">Il cmdlet **Get-AzureRmExpressRouteCircuitRouteTableSummary** recupera un riepilogo delle informazioni adiacenti BGP per un particolare contesto di routing.</span><span class="sxs-lookup"><span data-stu-id="0de55-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="0de55-107">Queste informazioni sono utili per determinare per quanto tempo è stato stabilito un contesto di routing e il numero di prefissi di route pubblicizzati dal router peering.</span><span class="sxs-lookup"><span data-stu-id="0de55-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="0de55-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0de55-108">EXAMPLES</span></span>

### <span data-ttu-id="0de55-109">Esempio 1: visualizzare il riepilogo della route per il percorso principale</span><span class="sxs-lookup"><span data-stu-id="0de55-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="0de55-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0de55-110">PARAMETERS</span></span>

### <span data-ttu-id="0de55-111">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="0de55-111">-DevicePath</span></span>
<span data-ttu-id="0de55-112">I valori accettabili per questo parametro sono: `Primary` o `Secondary`</span><span class="sxs-lookup"><span data-stu-id="0de55-112">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="0de55-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="0de55-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="0de55-114">Nome del circuito di ExpressRoute esaminato.</span><span class="sxs-lookup"><span data-stu-id="0de55-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="0de55-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="0de55-115">-PeeringType</span></span>
<span data-ttu-id="0de55-116">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="0de55-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="0de55-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de55-117">-ResourceGroupName</span></span>
<span data-ttu-id="0de55-118">Nome del gruppo di risorse contenente il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0de55-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="0de55-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de55-119">-DefaultProfile</span></span>
<span data-ttu-id="0de55-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0de55-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0de55-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de55-121">CommonParameters</span></span>
<span data-ttu-id="0de55-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0de55-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de55-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0de55-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de55-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0de55-124">INPUTS</span></span>

## <span data-ttu-id="0de55-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0de55-125">OUTPUTS</span></span>

### <span data-ttu-id="0de55-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="0de55-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="0de55-127">Note</span><span class="sxs-lookup"><span data-stu-id="0de55-127">NOTES</span></span>

## <span data-ttu-id="0de55-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0de55-128">RELATED LINKS</span></span>

[<span data-ttu-id="0de55-129">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0de55-129">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="0de55-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0de55-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="0de55-131">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="0de55-131">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
