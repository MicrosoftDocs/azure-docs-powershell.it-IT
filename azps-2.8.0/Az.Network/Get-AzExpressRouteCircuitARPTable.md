---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 04c4355caaa76776a96e2619a0080b9c32d8e98a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412215"
---
# <span data-ttu-id="da2bc-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="da2bc-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="da2bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="da2bc-103">Ottiene la tabella ARP da un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="da2bc-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="da2bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da2bc-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da2bc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="da2bc-105">DESCRIPTION</span></span>
<span data-ttu-id="da2bc-106">Il cmdlet **Get-AzExpressRouteCircuitARPTable** recupera la tabella ARP da entrambe le interfacce di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="da2bc-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="da2bc-107">La tabella ARP fornisce un mapping dell'indirizzo IPv4 all'indirizzo MAC per uno specifico peering.</span><span class="sxs-lookup"><span data-stu-id="da2bc-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="da2bc-108">È possibile usare la tabella ARP per convalidare la configurazione e la connettività di livello 2.</span><span class="sxs-lookup"><span data-stu-id="da2bc-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="da2bc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da2bc-109">EXAMPLES</span></span>

### <span data-ttu-id="da2bc-110">Esempio 1: Visualizzare la tabella ARP per un peer ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="da2bc-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="da2bc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da2bc-111">PARAMETERS</span></span>

### <span data-ttu-id="da2bc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da2bc-112">-DefaultProfile</span></span>
<span data-ttu-id="da2bc-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da2bc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da2bc-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="da2bc-114">-DevicePath</span></span>
<span data-ttu-id="da2bc-115">I valori accettabili per questo parametro sono: `Primary` o `Secondary`</span><span class="sxs-lookup"><span data-stu-id="da2bc-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="da2bc-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="da2bc-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="da2bc-117">Nome del circuito ExpressRoute da esaminare.</span><span class="sxs-lookup"><span data-stu-id="da2bc-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="da2bc-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="da2bc-118">-PeeringType</span></span>
<span data-ttu-id="da2bc-119">I valori accettabili per questo parametro sono: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="da2bc-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="da2bc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da2bc-120">-ResourceGroupName</span></span>
<span data-ttu-id="da2bc-121">Nome del gruppo di risorse che contiene il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="da2bc-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="da2bc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da2bc-122">CommonParameters</span></span>
<span data-ttu-id="da2bc-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da2bc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da2bc-124">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da2bc-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da2bc-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="da2bc-125">INPUTS</span></span>

### <span data-ttu-id="da2bc-126">System.String</span><span class="sxs-lookup"><span data-stu-id="da2bc-126">System.String</span></span>

## <span data-ttu-id="da2bc-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da2bc-127">OUTPUTS</span></span>

### <span data-ttu-id="da2bc-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="da2bc-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="da2bc-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="da2bc-129">NOTES</span></span>

## <span data-ttu-id="da2bc-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da2bc-130">RELATED LINKS</span></span>

[<span data-ttu-id="da2bc-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="da2bc-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="da2bc-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="da2bc-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="da2bc-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="da2bc-133">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
