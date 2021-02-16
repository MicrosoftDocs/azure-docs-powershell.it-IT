---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191775"
---
# <span data-ttu-id="5da39-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5da39-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="5da39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5da39-102">SYNOPSIS</span></span>
<span data-ttu-id="5da39-103">Rimuove un'autorizzazione di configurazione ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="5da39-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="5da39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5da39-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5da39-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5da39-105">DESCRIPTION</span></span>
<span data-ttu-id="5da39-106">Il cmdlet **Remove-AzExpressRouteCircuitAuthorization** rimuove un'autorizzazione assegnata a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5da39-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="5da39-107">I circuiti ExpressRoute connettono la rete locale ad Azure usando un provider di connettività invece di Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="5da39-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="5da39-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata dal proprietario di una rete virtuale per connettere la propria rete al circuito.</span><span class="sxs-lookup"><span data-stu-id="5da39-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="5da39-109">Per ogni rete virtuale può essere disponibile una sola autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="5da39-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="5da39-110">In qualsiasi momento, tuttavia, il proprietario del circuito può usare **Remove-AzExpressRouteCircuitAuthorization** per rimuovere l'autorizzazione assegnata a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5da39-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="5da39-111">In questo caso, la rete virtuale corrispondente non sarà più in grado di usare il circuito ExpressRoute per connettersi ad Azure.</span><span class="sxs-lookup"><span data-stu-id="5da39-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="5da39-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5da39-112">EXAMPLES</span></span>

### <span data-ttu-id="5da39-113">Esempio 1: Rimuovere un'autorizzazione del circuito da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="5da39-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="5da39-114">Questo esempio rimuove un'autorizzazione di circuito da un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5da39-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="5da39-115">Il primo comando usa il cmdlet **Get-AzExpressRouteCircuit** per creare un riferimento a un oggetto a un circuito ExpressRoute denominato ContosoCircuit e archivia il risultato nella variabile $Circuit.</span><span class="sxs-lookup"><span data-stu-id="5da39-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="5da39-116">Il secondo comando contrassegna l'autorizzazione del circuito ContosoCircuitAuthorization per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="5da39-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="5da39-117">Il terzo comando usa il cmdlet Set-AzExpressRouteCircuit per confermare la rimozione del circuito ExpressRoute archiviato nella $Circuit variabile.</span><span class="sxs-lookup"><span data-stu-id="5da39-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="5da39-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5da39-118">PARAMETERS</span></span>

### <span data-ttu-id="5da39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da39-119">-DefaultProfile</span></span>
<span data-ttu-id="5da39-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5da39-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5da39-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5da39-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5da39-122">Specifica l'oggetto ExpressRouteCircuit rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5da39-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5da39-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5da39-123">-Name</span></span>
<span data-ttu-id="5da39-124">Specifica il nome dell'autorizzazione del circuito rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5da39-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da39-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da39-125">CommonParameters</span></span>
<span data-ttu-id="5da39-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da39-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da39-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5da39-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da39-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="5da39-128">INPUTS</span></span>

### <span data-ttu-id="5da39-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5da39-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5da39-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5da39-130">OUTPUTS</span></span>

### <span data-ttu-id="5da39-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5da39-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5da39-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="5da39-132">NOTES</span></span>

## <span data-ttu-id="5da39-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5da39-133">RELATED LINKS</span></span>

[<span data-ttu-id="5da39-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5da39-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5da39-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5da39-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="5da39-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5da39-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5da39-137">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5da39-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5da39-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5da39-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
