---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: c7b4f51e868522533756534b52fd0b0cf5c17f0c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401284"
---
# <span data-ttu-id="d2ad7-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d2ad7-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="d2ad7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ad7-103">Ottiene una tabella di route da un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="d2ad7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2ad7-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2ad7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d2ad7-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ad7-106">Il cmdlet **Get-AzExpressRouteCircuitRouteTable** recupera una tabella di route dettagliata di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="d2ad7-107">La tabella dei percorsi mostra tutti i percorsi o può essere filtrata in modo da mostrare i percorsi per uno specifico tipo di peering.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="d2ad7-108">È possibile usare la tabella delle route per convalidare la configurazione e la connettività del peering.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="d2ad7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2ad7-109">EXAMPLES</span></span>

### <span data-ttu-id="d2ad7-110">Esempio 1: Visualizzare la tabella dei percorsi per il percorso principale</span><span class="sxs-lookup"><span data-stu-id="d2ad7-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="d2ad7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2ad7-111">PARAMETERS</span></span>

### <span data-ttu-id="d2ad7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ad7-112">-DefaultProfile</span></span>
<span data-ttu-id="d2ad7-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2ad7-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="d2ad7-114">-DevicePath</span></span>
<span data-ttu-id="d2ad7-115">I valori accettabili per questo parametro sono: `Primary` o `Secondary`</span><span class="sxs-lookup"><span data-stu-id="d2ad7-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="d2ad7-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="d2ad7-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="d2ad7-117">Nome del circuito ExpressRoute da esaminare.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="d2ad7-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="d2ad7-118">-PeeringType</span></span>
<span data-ttu-id="d2ad7-119">I valori accettabili per questo parametro sono: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="d2ad7-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="d2ad7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ad7-120">-ResourceGroupName</span></span>
<span data-ttu-id="d2ad7-121">Nome del gruppo di risorse che contiene il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="d2ad7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ad7-122">CommonParameters</span></span>
<span data-ttu-id="d2ad7-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ad7-124">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ad7-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="d2ad7-125">INPUTS</span></span>

### <span data-ttu-id="d2ad7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d2ad7-126">System.String</span></span>

## <span data-ttu-id="d2ad7-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2ad7-127">OUTPUTS</span></span>

### <span data-ttu-id="d2ad7-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="d2ad7-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="d2ad7-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="d2ad7-129">NOTES</span></span>

## <span data-ttu-id="d2ad7-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2ad7-130">RELATED LINKS</span></span>

[<span data-ttu-id="d2ad7-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d2ad7-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="d2ad7-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d2ad7-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="d2ad7-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="d2ad7-133">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
