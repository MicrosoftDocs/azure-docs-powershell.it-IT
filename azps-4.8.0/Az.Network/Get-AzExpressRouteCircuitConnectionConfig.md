---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: f4aabb68fd1f508651406d7ccf7be91ff646d46c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188539"
---
# <span data-ttu-id="638c4-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="638c4-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="638c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="638c4-102">SYNOPSIS</span></span>
<span data-ttu-id="638c4-103">Ottiene una configurazione di connessione circuitale ExpressRoute associata a peering privato di ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="638c4-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="638c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="638c4-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="638c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="638c4-105">DESCRIPTION</span></span>
<span data-ttu-id="638c4-106">Il cmdlet **Get-AzExpressRouteCircuitConnectionConfig** recupera la configurazione di una connessione Circuit associata a un peering privato per un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="638c4-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="638c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="638c4-107">EXAMPLES</span></span>

### <span data-ttu-id="638c4-108">Esempio 1: visualizzare la configurazione della connessione Circuit per un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="638c4-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="638c4-109">Esempio 2: ottenere una risorsa di connessione circuitale associata a un circuito ExpressRoute tramite piping</span><span class="sxs-lookup"><span data-stu-id="638c4-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="638c4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="638c4-110">PARAMETERS</span></span>

### <span data-ttu-id="638c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="638c4-111">-DefaultProfile</span></span>
<span data-ttu-id="638c4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="638c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="638c4-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="638c4-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="638c4-114">L'oggetto Circuit ExpressRoute che contiene la configurazione della connessione Circuit.</span><span class="sxs-lookup"><span data-stu-id="638c4-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="638c4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="638c4-115">-Name</span></span>
<span data-ttu-id="638c4-116">Nome della configurazione della connessione circuitale da recuperare.</span><span class="sxs-lookup"><span data-stu-id="638c4-116">The name of the circuit connection configuration to be retrieved.</span></span>

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

### <span data-ttu-id="638c4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="638c4-117">CommonParameters</span></span>
<span data-ttu-id="638c4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="638c4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="638c4-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="638c4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="638c4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="638c4-120">INPUTS</span></span>

### <span data-ttu-id="638c4-121">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="638c4-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="638c4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="638c4-122">OUTPUTS</span></span>

### <span data-ttu-id="638c4-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="638c4-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="638c4-124">Note</span><span class="sxs-lookup"><span data-stu-id="638c4-124">NOTES</span></span>

## <span data-ttu-id="638c4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="638c4-125">RELATED LINKS</span></span>

[<span data-ttu-id="638c4-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="638c4-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="638c4-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="638c4-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="638c4-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="638c4-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="638c4-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="638c4-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="638c4-130">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="638c4-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)