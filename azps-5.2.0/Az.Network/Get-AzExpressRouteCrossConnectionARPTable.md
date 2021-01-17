---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 30addde4594c7b67fd5ba9c1358d64ac206a4531
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329767"
---
# <span data-ttu-id="1b5e3-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="1b5e3-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="1b5e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b5e3-102">SYNOPSIS</span></span>
<span data-ttu-id="1b5e3-103">Ottiene la tabella ARP da una connessione trasversale ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1b5e3-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="1b5e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b5e3-104">SYNTAX</span></span>

### <span data-ttu-id="1b5e3-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="1b5e3-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b5e3-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="1b5e3-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b5e3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b5e3-107">DESCRIPTION</span></span>
<span data-ttu-id="1b5e3-108">Il cmdlet **Get-AzExpressRouteCrossConnectionARPTable** recupera la tabella ARP da entrambe le interfacce di una connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1b5e3-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="1b5e3-109">La tabella ARP fornisce un mapping dell'indirizzo IPv4 all'indirizzo MAC per un particolare peering.</span><span class="sxs-lookup"><span data-stu-id="1b5e3-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="1b5e3-110">È possibile usare la tabella ARP per convalidare la configurazione e la connettività Layer 2.</span><span class="sxs-lookup"><span data-stu-id="1b5e3-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="1b5e3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b5e3-111">EXAMPLES</span></span>

### <span data-ttu-id="1b5e3-112">Esempio 1: visualizzare la tabella ARP per un peer ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="1b5e3-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="1b5e3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b5e3-113">PARAMETERS</span></span>

### <span data-ttu-id="1b5e3-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="1b5e3-114">-CrossConnectionName</span></span>
<span data-ttu-id="1b5e3-115">Nome della connessione trasversale della route espressa</span><span class="sxs-lookup"><span data-stu-id="1b5e3-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b5e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b5e3-116">-DefaultProfile</span></span>
<span data-ttu-id="1b5e3-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b5e3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b5e3-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="1b5e3-118">-DevicePath</span></span>
<span data-ttu-id="1b5e3-119">I valori accettabili per questo parametro sono: `Primary` o `Secondary`</span><span class="sxs-lookup"><span data-stu-id="1b5e3-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="1b5e3-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1b5e3-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="1b5e3-121">Connessione trasversale della Route Express</span><span class="sxs-lookup"><span data-stu-id="1b5e3-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b5e3-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="1b5e3-122">-PeeringType</span></span>
<span data-ttu-id="1b5e3-123">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="1b5e3-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="1b5e3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b5e3-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b5e3-125">Nome del gruppo di risorse che contiene la connessione trasversale ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1b5e3-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b5e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b5e3-126">CommonParameters</span></span>
<span data-ttu-id="1b5e3-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b5e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b5e3-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b5e3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b5e3-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b5e3-129">INPUTS</span></span>

### <span data-ttu-id="1b5e3-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b5e3-130">None</span></span>
<span data-ttu-id="1b5e3-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1b5e3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b5e3-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b5e3-132">OUTPUTS</span></span>

### <span data-ttu-id="1b5e3-133">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="1b5e3-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="1b5e3-134">Note</span><span class="sxs-lookup"><span data-stu-id="1b5e3-134">NOTES</span></span>

## <span data-ttu-id="1b5e3-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b5e3-135">RELATED LINKS</span></span>

[<span data-ttu-id="1b5e3-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1b5e3-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="1b5e3-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1b5e3-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
