---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 108ea2b0262c34e38ffd7ed2961e3cba9a8d59ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686062"
---
# <span data-ttu-id="06030-101">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="06030-101">Add-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="06030-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06030-102">SYNOPSIS</span></span>
<span data-ttu-id="06030-103">Aggiunge un'autorizzazione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="06030-103">Adds an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06030-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06030-104">SYNTAX</span></span>

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06030-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06030-105">DESCRIPTION</span></span>
<span data-ttu-id="06030-106">Il cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** aggiunge un'autorizzazione a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="06030-106">The **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="06030-107">Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="06030-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="06030-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere la propria rete al circuito (un'autorizzazione per rete virtuale).</span><span class="sxs-lookup"><span data-stu-id="06030-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="06030-109">**Add-AzureRmExpressRouteCircuitAuthorization** aggiunge una nuova autorizzazione a un circuito e genera contemporaneamente la chiave di autorizzazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="06030-109">**Add-AzureRmExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="06030-110">Queste chiavi possono essere visualizzate in qualsiasi momento eseguendo il cmdlet Get-AzureRmExpressRouteCircuitAuthorization e, se necessario, possono quindi essere copiate e inoltrate al proprietario di rete appropriato.</span><span class="sxs-lookup"><span data-stu-id="06030-110">These keys can be viewed at any time by running the Get-AzureRmExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="06030-111">Tieni presente che, dopo aver eseguito **Add-AzureRmExpressRouteCircuitAuthorization** , devi chiamare il cmdlet Set-AzureRmExpressRouteCircuit per attivare la chiave.</span><span class="sxs-lookup"><span data-stu-id="06030-111">Note that, after running **Add-AzureRmExpressRouteCircuitAuthorization** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="06030-112">Se non si chiama **set-AzureRmExpressRouteCircuit,** l'autorizzazione verrà aggiunta al circuito, ma non verrà abilitata per l'uso.</span><span class="sxs-lookup"><span data-stu-id="06030-112">If you do not call **Set-AzureRmExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="06030-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06030-113">EXAMPLES</span></span>

### <span data-ttu-id="06030-114">Esempio 1: aggiungere un'autorizzazione al circuito ExpressRoute specificato</span><span class="sxs-lookup"><span data-stu-id="06030-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="06030-115">I comandi in questo esempio aggiungono una nuova autorizzazione a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="06030-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="06030-116">Il primo comando USA **Get-AzureRmExpressRouteCircuit** per creare un riferimento a un oggetto Circuit denominato ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="06030-116">The first command uses **Get-AzureRmExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="06030-117">Il riferimento a un oggetto viene archiviato in una variabile denominata $Circuit.</span><span class="sxs-lookup"><span data-stu-id="06030-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="06030-118">Nel secondo comando viene usato il cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** per aggiungere una nuova autorizzazione (ContosoCircuitAuthorization) al circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="06030-118">In the second command, the **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="06030-119">Questo comando aggiunge l'autorizzazione ma non attiva tale autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="06030-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="06030-120">L'attivazione di un'autorizzazione richiede l'opzione **set-AzureRmExpressRouteCircuit** visualizzata nel comando finale dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="06030-120">Activating an authorization requires the **Set-AzureRmExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="06030-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06030-121">PARAMETERS</span></span>

### <span data-ttu-id="06030-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06030-122">-DefaultProfile</span></span>
<span data-ttu-id="06030-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06030-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06030-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="06030-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="06030-125">Specifica il circuito di ExpressRoute a cui questo cmdlet aggiunge l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="06030-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="06030-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="06030-126">-Name</span></span>
<span data-ttu-id="06030-127">Specifica il nome dell'autorizzazione Circuit da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="06030-127">Specifies the name of the circuit authorization to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06030-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06030-128">CommonParameters</span></span>
<span data-ttu-id="06030-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06030-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06030-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06030-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06030-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06030-131">INPUTS</span></span>

### <span data-ttu-id="06030-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="06030-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="06030-133">Parametri: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="06030-133">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="06030-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06030-134">OUTPUTS</span></span>

### <span data-ttu-id="06030-135">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="06030-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="06030-136">Note</span><span class="sxs-lookup"><span data-stu-id="06030-136">NOTES</span></span>

## <span data-ttu-id="06030-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06030-137">RELATED LINKS</span></span>

[<span data-ttu-id="06030-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="06030-138">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="06030-139">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="06030-139">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="06030-140">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="06030-140">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="06030-141">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="06030-141">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="06030-142">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="06030-142">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
