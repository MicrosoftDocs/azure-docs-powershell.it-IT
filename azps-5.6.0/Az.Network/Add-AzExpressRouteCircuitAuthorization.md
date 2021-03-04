---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9812316b20db927dea9bfe999cad54fe002bfc93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952302"
---
# <span data-ttu-id="4e75e-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4e75e-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="4e75e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e75e-102">SYNOPSIS</span></span>
<span data-ttu-id="4e75e-103">Aggiunge un'autorizzazione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4e75e-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="4e75e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e75e-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e75e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4e75e-105">DESCRIPTION</span></span>
<span data-ttu-id="4e75e-106">Il cmdlet **Add-AzExpressRouteCircuitAuthorization** aggiunge un'autorizzazione a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4e75e-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="4e75e-107">I circuiti ExpressRoute connettono la rete locale al cloud Microsoft usando un provider di connettività invece di Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="4e75e-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="4e75e-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; queste autorizzazioni generano una chiave di autorizzazione che può essere usata dal proprietario di una rete virtuale per connettere la propria rete al circuito (un'autorizzazione per ogni rete virtuale).</span><span class="sxs-lookup"><span data-stu-id="4e75e-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="4e75e-109">**Add-AzExpressRouteCircuitAuthorization** aggiunge una nuova autorizzazione a un circuito e allo stesso tempo genera la chiave di autorizzazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="4e75e-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="4e75e-110">Queste chiavi possono essere visualizzate in qualsiasi momento eseguendo il cmdlet Get-AzExpressRouteCircuitAuthorization e, se necessario, possono essere copiate e inoltrate al proprietario della rete appropriato.</span><span class="sxs-lookup"><span data-stu-id="4e75e-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="4e75e-111">Si noti che, dopo aver eseguito **Add-AzExpressRouteCircuitAuthorization,** è necessario chiamare il cmdlet Set-AzExpressRouteCircuit per attivare la chiave.</span><span class="sxs-lookup"><span data-stu-id="4e75e-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="4e75e-112">Se non si chiama **Set-AzExpressRouteCircuit,** l'autorizzazione verrà aggiunta al circuito, ma non sarà abilitata per l'uso.</span><span class="sxs-lookup"><span data-stu-id="4e75e-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="4e75e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e75e-113">EXAMPLES</span></span>

### <span data-ttu-id="4e75e-114">Esempio 1: Aggiungere un'autorizzazione al circuito ExpressRoute specificato</span><span class="sxs-lookup"><span data-stu-id="4e75e-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="4e75e-115">I comandi di questo esempio aggiungono una nuova autorizzazione a un circuito ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="4e75e-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="4e75e-116">Il primo comando usa **Get-AzExpressRouteCircuit** per creare un riferimento a un oggetto a un circuito denominato ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="4e75e-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="4e75e-117">Il riferimento all'oggetto viene archiviato in una variabile denominata $Circuit.</span><span class="sxs-lookup"><span data-stu-id="4e75e-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="4e75e-118">Nel secondo comando viene usato il cmdlet **Add-AzExpressRouteCircuitAuthorization** per aggiungere una nuova autorizzazione (ContosoCircuitAuthorization) al circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4e75e-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="4e75e-119">Questo comando aggiunge l'autorizzazione, ma non la attiva.</span><span class="sxs-lookup"><span data-stu-id="4e75e-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="4e75e-120">L'attivazione di un'autorizzazione richiede **il set-AzExpressRouteCircuit** mostrato nel comando finale dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="4e75e-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="4e75e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e75e-121">PARAMETERS</span></span>

### <span data-ttu-id="4e75e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e75e-122">-DefaultProfile</span></span>
<span data-ttu-id="4e75e-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e75e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e75e-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e75e-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4e75e-125">Specifica il circuito ExpressRoute a cui questo cmdlet aggiunge l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="4e75e-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="4e75e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4e75e-126">-Name</span></span>
<span data-ttu-id="4e75e-127">Specifica il nome dell'autorizzazione del circuito da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="4e75e-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="4e75e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e75e-128">CommonParameters</span></span>
<span data-ttu-id="4e75e-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e75e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e75e-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e75e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e75e-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="4e75e-131">INPUTS</span></span>

### <span data-ttu-id="4e75e-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e75e-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4e75e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e75e-133">OUTPUTS</span></span>

### <span data-ttu-id="4e75e-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e75e-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4e75e-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="4e75e-135">NOTES</span></span>

## <span data-ttu-id="4e75e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e75e-136">RELATED LINKS</span></span>

[<span data-ttu-id="4e75e-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e75e-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4e75e-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4e75e-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="4e75e-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4e75e-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="4e75e-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4e75e-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="4e75e-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e75e-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
