---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 3fbfcc2ba78bb05eb64764be16bb84189afdd958
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678542"
---
# <span data-ttu-id="09004-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="09004-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="09004-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09004-102">SYNOPSIS</span></span>
<span data-ttu-id="09004-103">Ottiene una tabella di route da una connessione trasversale ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="09004-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="09004-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09004-104">SYNTAX</span></span>

### <span data-ttu-id="09004-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="09004-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09004-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="09004-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09004-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09004-107">DESCRIPTION</span></span>
<span data-ttu-id="09004-108">Il cmdlet **Get-AzExpressRouteCrossConnectionRouteTable** recupera una tabella di route dettagliata di un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="09004-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="09004-109">La tabella route mostrerà tutte le route o può essere filtrata per visualizzare le route per un tipo di peering specifico.</span><span class="sxs-lookup"><span data-stu-id="09004-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="09004-110">È possibile usare la tabella route per convalidare la configurazione e la connettività di peering.</span><span class="sxs-lookup"><span data-stu-id="09004-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="09004-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09004-111">EXAMPLES</span></span>

### <span data-ttu-id="09004-112">Esempio 1: visualizzare la tabella route per il percorso principale</span><span class="sxs-lookup"><span data-stu-id="09004-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="09004-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09004-113">PARAMETERS</span></span>

### <span data-ttu-id="09004-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="09004-114">-CrossConnectionName</span></span>
<span data-ttu-id="09004-115">Nome della connessione trasversale della route espressa</span><span class="sxs-lookup"><span data-stu-id="09004-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="09004-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09004-116">-DefaultProfile</span></span>
<span data-ttu-id="09004-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09004-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09004-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="09004-118">-DevicePath</span></span>
<span data-ttu-id="09004-119">I valori accettabili per questo parametro sono: `Primary` o `Secondary`</span><span class="sxs-lookup"><span data-stu-id="09004-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="09004-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="09004-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="09004-121">Connessione trasversale della Route Express</span><span class="sxs-lookup"><span data-stu-id="09004-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="09004-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="09004-122">-PeeringType</span></span>
<span data-ttu-id="09004-123">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="09004-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="09004-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09004-124">-ResourceGroupName</span></span>
<span data-ttu-id="09004-125">Nome del gruppo di risorse che contiene la connessione trasversale ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="09004-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="09004-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09004-126">CommonParameters</span></span>
<span data-ttu-id="09004-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09004-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09004-128">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09004-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09004-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09004-129">INPUTS</span></span>

### <span data-ttu-id="09004-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="09004-130">None</span></span>
<span data-ttu-id="09004-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="09004-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09004-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09004-132">OUTPUTS</span></span>

### <span data-ttu-id="09004-133">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="09004-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="09004-134">Note</span><span class="sxs-lookup"><span data-stu-id="09004-134">NOTES</span></span>

## <span data-ttu-id="09004-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09004-135">RELATED LINKS</span></span>

[<span data-ttu-id="09004-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="09004-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="09004-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="09004-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)