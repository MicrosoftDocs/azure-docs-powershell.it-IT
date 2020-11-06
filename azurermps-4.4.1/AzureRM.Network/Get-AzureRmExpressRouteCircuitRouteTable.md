---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
ms.openlocfilehash: d2be2927be03895f80a537f70e80c53e246e16f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519140"
---
# <span data-ttu-id="da277-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="da277-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="da277-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da277-102">SYNOPSIS</span></span>
<span data-ttu-id="da277-103">Ottiene una tabella di route da un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="da277-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da277-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da277-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da277-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da277-105">DESCRIPTION</span></span>
<span data-ttu-id="da277-106">Il cmdlet **Get-AzureRmExpressRouteCircuitRouteTable** recupera una tabella di route dettagliata di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="da277-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="da277-107">La tabella route mostrerà tutte le route o può essere filtrata per visualizzare le route per un tipo di peering specifico.</span><span class="sxs-lookup"><span data-stu-id="da277-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="da277-108">È possibile usare la tabella route per convalidare la configurazione e la connettività di peering.</span><span class="sxs-lookup"><span data-stu-id="da277-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="da277-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da277-109">EXAMPLES</span></span>

### <span data-ttu-id="da277-110">Esempio 1: visualizzare la tabella route per il percorso principale</span><span class="sxs-lookup"><span data-stu-id="da277-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="da277-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da277-111">PARAMETERS</span></span>

### <span data-ttu-id="da277-112">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="da277-112">-DevicePath</span></span>
<span data-ttu-id="da277-113">I valori accettabili per questo parametro sono: `Primary` o `Secondary`</span><span class="sxs-lookup"><span data-stu-id="da277-113">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="da277-114">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="da277-114">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="da277-115">Nome del circuito di ExpressRoute esaminato.</span><span class="sxs-lookup"><span data-stu-id="da277-115">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="da277-116">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="da277-116">-PeeringType</span></span>
<span data-ttu-id="da277-117">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="da277-117">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="da277-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da277-118">-ResourceGroupName</span></span>
<span data-ttu-id="da277-119">Nome del gruppo di risorse contenente il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="da277-119">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="da277-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da277-120">-DefaultProfile</span></span>
<span data-ttu-id="da277-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da277-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da277-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da277-122">CommonParameters</span></span>
<span data-ttu-id="da277-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da277-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da277-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da277-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da277-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da277-125">INPUTS</span></span>

## <span data-ttu-id="da277-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da277-126">OUTPUTS</span></span>

### <span data-ttu-id="da277-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="da277-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="da277-128">Note</span><span class="sxs-lookup"><span data-stu-id="da277-128">NOTES</span></span>

## <span data-ttu-id="da277-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da277-129">RELATED LINKS</span></span>

[<span data-ttu-id="da277-130">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="da277-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="da277-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="da277-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="da277-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="da277-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
