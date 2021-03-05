---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: c8d35373c2891b9f0d3ac76ded8b4e9808f32f33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993816"
---
# <span data-ttu-id="b5529-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b5529-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="b5529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5529-102">SYNOPSIS</span></span>
<span data-ttu-id="b5529-103">Ottiene una configurazione della connessione del circuito ExpressRoute associata al peering privato di ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="b5529-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="b5529-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5529-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5529-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5529-105">DESCRIPTION</span></span>
<span data-ttu-id="b5529-106">Il cmdlet **Get-AzExpressRouteCircuitConnectionConfig** recupera la configurazione di una connessione a un circuito associato al peering privato per un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b5529-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="b5529-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5529-107">EXAMPLES</span></span>

### <span data-ttu-id="b5529-108">Esempio 1: Visualizzare la configurazione della connessione del circuito per un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="b5529-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="b5529-109">Esempio 2: Ottenere la risorsa della connessione del circuito associata a un circuito ExpressRoute usando le piping</span><span class="sxs-lookup"><span data-stu-id="b5529-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="b5529-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5529-110">PARAMETERS</span></span>

### <span data-ttu-id="b5529-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5529-111">-DefaultProfile</span></span>
<span data-ttu-id="b5529-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5529-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5529-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b5529-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b5529-114">Oggetto circuito ExpressRoute contenente la configurazione della connessione del circuito.</span><span class="sxs-lookup"><span data-stu-id="b5529-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5529-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b5529-115">-Name</span></span>
<span data-ttu-id="b5529-116">Nome della configurazione della connessione al circuito da recuperare.</span><span class="sxs-lookup"><span data-stu-id="b5529-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5529-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5529-117">CommonParameters</span></span>
<span data-ttu-id="b5529-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5529-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5529-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5529-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5529-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5529-120">INPUTS</span></span>

### <span data-ttu-id="b5529-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b5529-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b5529-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5529-122">OUTPUTS</span></span>

### <span data-ttu-id="b5529-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="b5529-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="b5529-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5529-124">NOTES</span></span>

## <span data-ttu-id="b5529-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5529-125">RELATED LINKS</span></span>

[<span data-ttu-id="b5529-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b5529-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b5529-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b5529-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b5529-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b5529-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b5529-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b5529-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b5529-130">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b5529-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)