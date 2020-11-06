---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
ms.openlocfilehash: e306faae861b8f35bff3695dc4235394764621a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510476"
---
# <span data-ttu-id="44aca-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="44aca-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="44aca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44aca-102">SYNOPSIS</span></span>
<span data-ttu-id="44aca-103">Ottiene la tabella ARP da un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="44aca-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44aca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44aca-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44aca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44aca-105">DESCRIPTION</span></span>
<span data-ttu-id="44aca-106">Il cmdlet **Get-AzureRmExpressRouteCircuitARPTable** recupera la tabella ARP da entrambe le interfacce di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="44aca-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="44aca-107">La tabella ARP fornisce un mapping dell'indirizzo IPv4 all'indirizzo MAC per un particolare peering.</span><span class="sxs-lookup"><span data-stu-id="44aca-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="44aca-108">È possibile usare la tabella ARP per convalidare la configurazione e la connettività Layer 2.</span><span class="sxs-lookup"><span data-stu-id="44aca-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="44aca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44aca-109">EXAMPLES</span></span>

### <span data-ttu-id="44aca-110">Esempio 1: visualizzare la tabella ARP per un peer ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="44aca-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="44aca-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44aca-111">PARAMETERS</span></span>

### <span data-ttu-id="44aca-112">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="44aca-112">-DevicePath</span></span>
<span data-ttu-id="44aca-113">I valori accettabili per questo parametro sono: `Primary` o `Secondary`</span><span class="sxs-lookup"><span data-stu-id="44aca-113">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="44aca-114">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="44aca-114">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="44aca-115">Nome del circuito di ExpressRoute esaminato.</span><span class="sxs-lookup"><span data-stu-id="44aca-115">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="44aca-116">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="44aca-116">-PeeringType</span></span>
<span data-ttu-id="44aca-117">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="44aca-117">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="44aca-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44aca-118">-ResourceGroupName</span></span>
<span data-ttu-id="44aca-119">Nome del gruppo di risorse contenente il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="44aca-119">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="44aca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44aca-120">-DefaultProfile</span></span>
<span data-ttu-id="44aca-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44aca-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44aca-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44aca-122">CommonParameters</span></span>
<span data-ttu-id="44aca-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44aca-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44aca-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44aca-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44aca-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44aca-125">INPUTS</span></span>

## <span data-ttu-id="44aca-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44aca-126">OUTPUTS</span></span>

### <span data-ttu-id="44aca-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="44aca-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="44aca-128">Note</span><span class="sxs-lookup"><span data-stu-id="44aca-128">NOTES</span></span>

## <span data-ttu-id="44aca-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44aca-129">RELATED LINKS</span></span>

[<span data-ttu-id="44aca-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="44aca-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="44aca-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="44aca-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="44aca-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="44aca-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
