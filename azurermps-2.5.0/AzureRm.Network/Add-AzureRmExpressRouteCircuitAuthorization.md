---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 9b41eb0c95c2b1693e56c8b11fee86b6e49a4609
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866314"
---
# <span data-ttu-id="42b1f-101">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="42b1f-101">Add-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="42b1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="42b1f-103">Aggiunge un'autorizzazione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="42b1f-103">Adds an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42b1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42b1f-104">SYNTAX</span></span>

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42b1f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42b1f-105">DESCRIPTION</span></span>
<span data-ttu-id="42b1f-106">Il cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** aggiunge un'autorizzazione a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="42b1f-106">The **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="42b1f-107">Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="42b1f-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="42b1f-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere la propria rete al circuito (un'autorizzazione per rete virtuale).</span><span class="sxs-lookup"><span data-stu-id="42b1f-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="42b1f-109">**Add-AzureRmExpressRouteCircuitAuthorization** aggiunge una nuova autorizzazione a un circuito e genera contemporaneamente la chiave di autorizzazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="42b1f-109">**Add-AzureRmExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="42b1f-110">Queste chiavi possono essere visualizzate in qualsiasi momento eseguendo il cmdlet Get-AzureRmExpressRouteCircuitAuthorization e, se necessario, possono quindi essere copiate e inoltrate al proprietario di rete appropriato.</span><span class="sxs-lookup"><span data-stu-id="42b1f-110">These keys can be viewed at any time by running the Get-AzureRmExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="42b1f-111">Tieni presente che, dopo aver eseguito **Add-AzureRmExpressRouteCircuitAuthorization** , devi chiamare il cmdlet Set-AzureRmExpressRouteCircuit per attivare la chiave.</span><span class="sxs-lookup"><span data-stu-id="42b1f-111">Note that, after running **Add-AzureRmExpressRouteCircuitAuthorization** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="42b1f-112">Se non si chiama **set-AzureRmExpressRouteCircuit,** l'autorizzazione verrà aggiunta al circuito, ma non verrà abilitata per l'uso.</span><span class="sxs-lookup"><span data-stu-id="42b1f-112">If you do not call **Set-AzureRmExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="42b1f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42b1f-113">EXAMPLES</span></span>

### <span data-ttu-id="42b1f-114">Esempio 1: aggiungere un'autorizzazione al circuito ExpressRoute specificato</span><span class="sxs-lookup"><span data-stu-id="42b1f-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="42b1f-115">I comandi in questo esempio aggiungono una nuova autorizzazione a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="42b1f-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="42b1f-116">Il primo comando USA **Get-AzureRmExpressRouteCircuit** per creare un riferimento a un oggetto Circuit denominato ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="42b1f-116">The first command uses **Get-AzureRmExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="42b1f-117">Il riferimento a un oggetto viene archiviato in una variabile denominata $Circuit.</span><span class="sxs-lookup"><span data-stu-id="42b1f-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="42b1f-118">Nel secondo comando viene usato il cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** per aggiungere una nuova autorizzazione (ContosoCircuitAuthorization) al circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="42b1f-118">In the second command, the **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="42b1f-119">Questo comando aggiunge l'autorizzazione ma non attiva tale autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="42b1f-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="42b1f-120">L'attivazione di un'autorizzazione richiede l'opzione **set-AzureRmExpressRouteCircuit** visualizzata nel comando finale dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="42b1f-120">Activating an authorization requires the **Set-AzureRmExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="42b1f-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42b1f-121">PARAMETERS</span></span>

### <span data-ttu-id="42b1f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b1f-122">-DefaultProfile</span></span>
<span data-ttu-id="42b1f-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42b1f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42b1f-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42b1f-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="42b1f-125">Specifica il circuito di ExpressRoute a cui questo cmdlet aggiunge l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="42b1f-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="42b1f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="42b1f-126">-Name</span></span>
<span data-ttu-id="42b1f-127">Specifica il nome dell'autorizzazione Circuit da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="42b1f-127">Specifies the name of the circuit authorization to be added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b1f-128">CommonParameters</span></span>
<span data-ttu-id="42b1f-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b1f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b1f-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42b1f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b1f-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42b1f-131">INPUTS</span></span>

### <span data-ttu-id="42b1f-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42b1f-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="42b1f-133">**Add-AzureRmExpressRouteCircuitAuthorization** accetta istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="42b1f-133">**Add-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="42b1f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42b1f-134">OUTPUTS</span></span>

### <span data-ttu-id="42b1f-135">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42b1f-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="42b1f-136">**Add-AzureRmExpressRouteCircuitAuthorization** modifica le istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="42b1f-136">**Add-AzureRmExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="42b1f-137">Note</span><span class="sxs-lookup"><span data-stu-id="42b1f-137">NOTES</span></span>

## <span data-ttu-id="42b1f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42b1f-138">RELATED LINKS</span></span>

[<span data-ttu-id="42b1f-139">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42b1f-139">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="42b1f-140">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="42b1f-140">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="42b1f-141">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="42b1f-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="42b1f-142">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="42b1f-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="42b1f-143">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42b1f-143">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
