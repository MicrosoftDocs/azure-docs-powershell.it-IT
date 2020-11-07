---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 144d70318463b7c5ffebfa6b7d942ec2a351fc24
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866050"
---
# <span data-ttu-id="12d19-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="12d19-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="12d19-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12d19-102">SYNOPSIS</span></span>
<span data-ttu-id="12d19-103">Rimuove un'autorizzazione di configurazione di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="12d19-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12d19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12d19-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12d19-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12d19-105">DESCRIPTION</span></span>
<span data-ttu-id="12d19-106">Il cmdlet **Remove-AzureRmExpressRouteCircuitAuthorization** rimuove un'autorizzazione assegnata a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="12d19-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="12d19-107">Circuiti ExpressRoute connettere la rete locale a Azure usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="12d19-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="12d19-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere la propria rete al circuito.</span><span class="sxs-lookup"><span data-stu-id="12d19-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="12d19-109">Può essere disponibile una sola autorizzazione per ogni rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="12d19-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="12d19-110">In qualsiasi momento, tuttavia, il proprietario del circuito può usare **Remove-AzureRmExpressRouteCircuitAuthorization** per rimuovere l'autorizzazione assegnata a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="12d19-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="12d19-111">Quando ciò accade, la rete virtuale corrispondente non è più in grado di usare il circuito ExpressRoute per connettersi ad Azure.</span><span class="sxs-lookup"><span data-stu-id="12d19-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="12d19-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12d19-112">EXAMPLES</span></span>

### <span data-ttu-id="12d19-113">Esempio 1: rimuovere l'autorizzazione di un circuito da un circuito di ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="12d19-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="12d19-114">In questo esempio viene rimossa un'autorizzazione Circuit da un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="12d19-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="12d19-115">Il primo comando usa il cmdlet **Get-AzureRmExpressRouteCircuit** per creare un riferimento a un oggetto in un circuito ExpressRoute denominato ContosoCircuit e archivia il risultato nella variabile denominata $Circuit.</span><span class="sxs-lookup"><span data-stu-id="12d19-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="12d19-116">Il secondo comando contrassegna l'autorizzazione Circuit ContosoCircuitAuthorization per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="12d19-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="12d19-117">Il terzo comando usa il cmdlet Set-AzureRmExpressRouteCircuit per confermare la rimozione del circuito ExpressRoute archiviato nella variabile $Circuit.</span><span class="sxs-lookup"><span data-stu-id="12d19-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="12d19-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12d19-118">PARAMETERS</span></span>

### <span data-ttu-id="12d19-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d19-119">-DefaultProfile</span></span>
<span data-ttu-id="12d19-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12d19-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12d19-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="12d19-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="12d19-122">Specifica l'oggetto ExpressRouteCircuit rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12d19-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12d19-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="12d19-123">-Name</span></span>
<span data-ttu-id="12d19-124">Specifica il nome dell'autorizzazione Circuit che viene rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12d19-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12d19-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d19-125">CommonParameters</span></span>
<span data-ttu-id="12d19-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d19-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d19-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d19-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d19-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12d19-128">INPUTS</span></span>

### <span data-ttu-id="12d19-129">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="12d19-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="12d19-130">Questo cmdlet accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="12d19-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="12d19-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12d19-131">OUTPUTS</span></span>

### <span data-ttu-id="12d19-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="12d19-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="12d19-133">Questo cmdlet modifica le istanze esistenti dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="12d19-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="12d19-134">Note</span><span class="sxs-lookup"><span data-stu-id="12d19-134">NOTES</span></span>

## <span data-ttu-id="12d19-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12d19-135">RELATED LINKS</span></span>

[<span data-ttu-id="12d19-136">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="12d19-136">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="12d19-137">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="12d19-137">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="12d19-138">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="12d19-138">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="12d19-139">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="12d19-139">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="12d19-140">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="12d19-140">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
