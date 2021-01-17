---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378794"
---
# <span data-ttu-id="7b3dd-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7b3dd-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="7b3dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7b3dd-103">Rimuove un'autorizzazione di configurazione di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="7b3dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b3dd-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b3dd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b3dd-105">DESCRIPTION</span></span>
<span data-ttu-id="7b3dd-106">Il cmdlet **Remove-AzExpressRouteCircuitAuthorization** rimuove un'autorizzazione assegnata a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="7b3dd-107">Circuiti ExpressRoute connettere la rete locale a Azure usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="7b3dd-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere la propria rete al circuito.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="7b3dd-109">Può essere disponibile una sola autorizzazione per ogni rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="7b3dd-110">In qualsiasi momento, tuttavia, il proprietario del circuito può usare **Remove-AzExpressRouteCircuitAuthorization** per rimuovere l'autorizzazione assegnata a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="7b3dd-111">Quando ciò accade, la rete virtuale corrispondente non è più in grado di usare il circuito ExpressRoute per connettersi ad Azure.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="7b3dd-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b3dd-112">EXAMPLES</span></span>

### <span data-ttu-id="7b3dd-113">Esempio 1: rimuovere l'autorizzazione di un circuito da un circuito di ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7b3dd-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="7b3dd-114">In questo esempio viene rimossa un'autorizzazione Circuit da un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="7b3dd-115">Il primo comando usa il cmdlet **Get-AzExpressRouteCircuit** per creare un riferimento a un oggetto in un circuito ExpressRoute denominato ContosoCircuit e archivia il risultato nella variabile denominata $Circuit.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="7b3dd-116">Il secondo comando contrassegna l'autorizzazione Circuit ContosoCircuitAuthorization per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="7b3dd-117">Il terzo comando usa il cmdlet Set-AzExpressRouteCircuit per confermare la rimozione del circuito ExpressRoute archiviato nella variabile $Circuit.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="7b3dd-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b3dd-118">PARAMETERS</span></span>

### <span data-ttu-id="7b3dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b3dd-119">-DefaultProfile</span></span>
<span data-ttu-id="7b3dd-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b3dd-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b3dd-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7b3dd-122">Specifica l'oggetto ExpressRouteCircuit rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7b3dd-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b3dd-123">-Name</span></span>
<span data-ttu-id="7b3dd-124">Specifica il nome dell'autorizzazione Circuit che viene rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7b3dd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b3dd-125">CommonParameters</span></span>
<span data-ttu-id="7b3dd-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b3dd-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b3dd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b3dd-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b3dd-128">INPUTS</span></span>

### <span data-ttu-id="7b3dd-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b3dd-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7b3dd-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b3dd-130">OUTPUTS</span></span>

### <span data-ttu-id="7b3dd-131">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b3dd-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7b3dd-132">Note</span><span class="sxs-lookup"><span data-stu-id="7b3dd-132">NOTES</span></span>

## <span data-ttu-id="7b3dd-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b3dd-133">RELATED LINKS</span></span>

[<span data-ttu-id="7b3dd-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7b3dd-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="7b3dd-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b3dd-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="7b3dd-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7b3dd-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="7b3dd-137">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7b3dd-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="7b3dd-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b3dd-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
