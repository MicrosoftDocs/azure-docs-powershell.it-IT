---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 463c1bf9e97d3e438b89cee1e87279ad4bf06ad9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678548"
---
# <span data-ttu-id="45672-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="45672-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="45672-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45672-102">SYNOPSIS</span></span>
<span data-ttu-id="45672-103">Ottiene statistiche sull'utilizzo di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="45672-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="45672-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45672-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45672-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45672-105">DESCRIPTION</span></span>
<span data-ttu-id="45672-106">Il cmdlet **Get-AzExpressRouteCircuitStat** recupera le statistiche del traffico per un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="45672-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="45672-107">Le statistiche includono il numero di byte inviati e ricevuti sia sulle route primarie che secondarie.</span><span class="sxs-lookup"><span data-stu-id="45672-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="45672-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45672-108">EXAMPLES</span></span>

### <span data-ttu-id="45672-109">Esempio 1: visualizzare le statistiche del traffico per un peer ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="45672-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="45672-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45672-110">PARAMETERS</span></span>

### <span data-ttu-id="45672-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45672-111">-DefaultProfile</span></span>
<span data-ttu-id="45672-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45672-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45672-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="45672-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="45672-114">Nome del circuito di ExpressRoute esaminato.</span><span class="sxs-lookup"><span data-stu-id="45672-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="45672-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="45672-115">-PeeringType</span></span>
<span data-ttu-id="45672-116">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="45672-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="45672-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45672-117">-ResourceGroupName</span></span>
<span data-ttu-id="45672-118">Nome del gruppo di risorse contenente il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="45672-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="45672-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45672-119">CommonParameters</span></span>
<span data-ttu-id="45672-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45672-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45672-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45672-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45672-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45672-122">INPUTS</span></span>

### <span data-ttu-id="45672-123">System. String</span><span class="sxs-lookup"><span data-stu-id="45672-123">System.String</span></span>

## <span data-ttu-id="45672-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45672-124">OUTPUTS</span></span>

### <span data-ttu-id="45672-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="45672-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="45672-126">Note</span><span class="sxs-lookup"><span data-stu-id="45672-126">NOTES</span></span>

## <span data-ttu-id="45672-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45672-127">RELATED LINKS</span></span>

[<span data-ttu-id="45672-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="45672-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="45672-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="45672-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="45672-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="45672-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
