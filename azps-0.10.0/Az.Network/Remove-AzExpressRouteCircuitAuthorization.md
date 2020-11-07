---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: ef00e209b030ed4a05ad29ccb3e768df090ea8ee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860318"
---
# <span data-ttu-id="31161-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="31161-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="31161-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31161-102">SYNOPSIS</span></span>
<span data-ttu-id="31161-103">Rimuove un'autorizzazione di configurazione di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="31161-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="31161-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31161-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31161-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31161-105">DESCRIPTION</span></span>
<span data-ttu-id="31161-106">Il cmdlet **Remove-AzExpressRouteCircuitAuthorization** rimuove un'autorizzazione assegnata a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="31161-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="31161-107">Circuiti ExpressRoute connettere la rete locale a Azure usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="31161-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="31161-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere la propria rete al circuito.</span><span class="sxs-lookup"><span data-stu-id="31161-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="31161-109">Può essere disponibile una sola autorizzazione per ogni rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="31161-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="31161-110">In qualsiasi momento, tuttavia, il proprietario del circuito può usare **Remove-AzExpressRouteCircuitAuthorization** per rimuovere l'autorizzazione assegnata a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="31161-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="31161-111">Quando ciò accade, la rete virtuale corrispondente non è più in grado di usare il circuito ExpressRoute per connettersi ad Azure.</span><span class="sxs-lookup"><span data-stu-id="31161-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="31161-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31161-112">EXAMPLES</span></span>

### <span data-ttu-id="31161-113">Esempio 1: rimuovere l'autorizzazione di un circuito da un circuito di ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="31161-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="31161-114">In questo esempio viene rimossa un'autorizzazione Circuit da un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="31161-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="31161-115">Il primo comando usa il cmdlet **Get-AzExpressRouteCircuit** per creare un riferimento a un oggetto in un circuito ExpressRoute denominato ContosoCircuit e archivia il risultato nella variabile denominata $Circuit.</span><span class="sxs-lookup"><span data-stu-id="31161-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="31161-116">Il secondo comando contrassegna l'autorizzazione Circuit ContosoCircuitAuthorization per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="31161-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="31161-117">Il terzo comando usa il cmdlet Set-AzExpressRouteCircuit per confermare la rimozione del circuito ExpressRoute archiviato nella variabile $Circuit.</span><span class="sxs-lookup"><span data-stu-id="31161-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="31161-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31161-118">PARAMETERS</span></span>

### <span data-ttu-id="31161-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31161-119">-DefaultProfile</span></span>
<span data-ttu-id="31161-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31161-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31161-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="31161-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="31161-122">Specifica l'oggetto ExpressRouteCircuit rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31161-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31161-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="31161-123">-Name</span></span>
<span data-ttu-id="31161-124">Specifica il nome dell'autorizzazione Circuit che viene rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31161-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31161-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31161-125">CommonParameters</span></span>
<span data-ttu-id="31161-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31161-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31161-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31161-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31161-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31161-128">INPUTS</span></span>

### <span data-ttu-id="31161-129">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="31161-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="31161-130">Questo cmdlet accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="31161-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="31161-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31161-131">OUTPUTS</span></span>

### <span data-ttu-id="31161-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="31161-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="31161-133">Questo cmdlet modifica le istanze esistenti dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="31161-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="31161-134">Note</span><span class="sxs-lookup"><span data-stu-id="31161-134">NOTES</span></span>

## <span data-ttu-id="31161-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31161-135">RELATED LINKS</span></span>

[<span data-ttu-id="31161-136">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="31161-136">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="31161-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="31161-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="31161-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="31161-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="31161-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="31161-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="31161-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="31161-140">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
