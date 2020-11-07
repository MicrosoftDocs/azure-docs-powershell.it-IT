---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: efe2a149d2ca02c075b2e0a1f73191e9e2b8859b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860994"
---
# <span data-ttu-id="2eabe-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2eabe-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="2eabe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2eabe-102">SYNOPSIS</span></span>
<span data-ttu-id="2eabe-103">Aggiunge un'autorizzazione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2eabe-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="2eabe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2eabe-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eabe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2eabe-105">DESCRIPTION</span></span>
<span data-ttu-id="2eabe-106">Il cmdlet **Add-AzExpressRouteCircuitAuthorization** aggiunge un'autorizzazione a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2eabe-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="2eabe-107">Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="2eabe-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="2eabe-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere la propria rete al circuito (un'autorizzazione per rete virtuale).</span><span class="sxs-lookup"><span data-stu-id="2eabe-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="2eabe-109">**Add-AzExpressRouteCircuitAuthorization** aggiunge una nuova autorizzazione a un circuito e genera contemporaneamente la chiave di autorizzazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2eabe-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="2eabe-110">Queste chiavi possono essere visualizzate in qualsiasi momento eseguendo il cmdlet Get-AzExpressRouteCircuitAuthorization e, se necessario, possono quindi essere copiate e inoltrate al proprietario di rete appropriato.</span><span class="sxs-lookup"><span data-stu-id="2eabe-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="2eabe-111">Tieni presente che, dopo aver eseguito **Add-AzExpressRouteCircuitAuthorization** , devi chiamare il cmdlet Set-AzExpressRouteCircuit per attivare la chiave.</span><span class="sxs-lookup"><span data-stu-id="2eabe-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="2eabe-112">Se non si chiama **set-AzExpressRouteCircuit,** l'autorizzazione verrà aggiunta al circuito, ma non verrà abilitata per l'uso.</span><span class="sxs-lookup"><span data-stu-id="2eabe-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="2eabe-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2eabe-113">EXAMPLES</span></span>

### <span data-ttu-id="2eabe-114">Esempio 1: aggiungere un'autorizzazione al circuito ExpressRoute specificato</span><span class="sxs-lookup"><span data-stu-id="2eabe-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="2eabe-115">I comandi in questo esempio aggiungono una nuova autorizzazione a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="2eabe-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="2eabe-116">Il primo comando USA **Get-AzExpressRouteCircuit** per creare un riferimento a un oggetto Circuit denominato ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="2eabe-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="2eabe-117">Il riferimento a un oggetto viene archiviato in una variabile denominata $Circuit.</span><span class="sxs-lookup"><span data-stu-id="2eabe-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="2eabe-118">Nel secondo comando viene usato il cmdlet **Add-AzExpressRouteCircuitAuthorization** per aggiungere una nuova autorizzazione (ContosoCircuitAuthorization) al circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2eabe-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="2eabe-119">Questo comando aggiunge l'autorizzazione ma non attiva tale autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="2eabe-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="2eabe-120">L'attivazione di un'autorizzazione richiede l'opzione **set-AzExpressRouteCircuit** visualizzata nel comando finale dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="2eabe-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="2eabe-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2eabe-121">PARAMETERS</span></span>

### <span data-ttu-id="2eabe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eabe-122">-DefaultProfile</span></span>
<span data-ttu-id="2eabe-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2eabe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eabe-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2eabe-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2eabe-125">Specifica il circuito di ExpressRoute a cui questo cmdlet aggiunge l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="2eabe-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="2eabe-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2eabe-126">-Name</span></span>
<span data-ttu-id="2eabe-127">Specifica il nome dell'autorizzazione Circuit da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="2eabe-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="2eabe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eabe-128">CommonParameters</span></span>
<span data-ttu-id="2eabe-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eabe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eabe-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eabe-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eabe-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2eabe-131">INPUTS</span></span>

### <span data-ttu-id="2eabe-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2eabe-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="2eabe-133">**Add-AzExpressRouteCircuitAuthorization** accetta istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="2eabe-133">**Add-AzExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="2eabe-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2eabe-134">OUTPUTS</span></span>

### <span data-ttu-id="2eabe-135">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2eabe-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="2eabe-136">**Add-AzExpressRouteCircuitAuthorization** modifica le istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="2eabe-136">**Add-AzExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="2eabe-137">Note</span><span class="sxs-lookup"><span data-stu-id="2eabe-137">NOTES</span></span>

## <span data-ttu-id="2eabe-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2eabe-138">RELATED LINKS</span></span>

[<span data-ttu-id="2eabe-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2eabe-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="2eabe-140">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2eabe-140">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="2eabe-141">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2eabe-141">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="2eabe-142">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2eabe-142">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="2eabe-143">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2eabe-143">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
