---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: f0e66c1e601ab63eec6d2540edd3ba0235727e9a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866255"
---
# <span data-ttu-id="0cd2a-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0cd2a-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="0cd2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0cd2a-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd2a-103">Crea un'autorizzazione per il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cd2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0cd2a-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0cd2a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cd2a-105">DESCRIPTION</span></span>
<span data-ttu-id="0cd2a-106">Il cmdlet **New-AzureRmExpressRouteCircuitAuthorization** crea un'autorizzazione Circuit che può essere aggiunta a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="0cd2a-107">Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="0cd2a-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere una rete al circuito.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="0cd2a-109">Può essere disponibile una sola autorizzazione per ogni rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="0cd2a-110">Dopo aver creato un circuito ExpressRoute, è possibile usare **Add-AzureRmExpressRouteCircuitAuthorization** per aggiungere un'autorizzazione al circuito.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="0cd2a-111">In alternativa, puoi usare **New-AzureRmExpressRouteCircuitAuthorization** per creare un'autorizzazione che può essere aggiunta a un nuovo circuito contemporaneamente alla creazione del circuito.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="0cd2a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0cd2a-112">EXAMPLES</span></span>

### <span data-ttu-id="0cd2a-113">Esempio 1: creare una nuova autorizzazione Circuit</span><span class="sxs-lookup"><span data-stu-id="0cd2a-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="0cd2a-114">Questo comando crea una nuova autorizzazione Circuit denominata ContosoCircuitAuthorization e quindi archivia tale oggetto in una variabile denominata $Authorization.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="0cd2a-115">Il salvataggio dell'oggetto in una variabile è importante: anche se **New-AzureRmExpressRouteCircuitAuthorization** può creare un'autorizzazione Circuit, non può aggiungere l'autorizzazione a una route Circuit.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="0cd2a-116">La variabile $Authorization viene invece usata New-AzureRmExpressRouteCircuit quando si crea un nuovo circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="0cd2a-117">Per altre informazioni, vedere la documentazione relativa al cmdlet New-AzureRmExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="0cd2a-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0cd2a-118">PARAMETERS</span></span>

### <span data-ttu-id="0cd2a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd2a-119">-DefaultProfile</span></span>
<span data-ttu-id="0cd2a-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cd2a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0cd2a-121">-Name</span></span>
<span data-ttu-id="0cd2a-122">Specifica un nome univoco per la nuova autorizzazione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="0cd2a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd2a-123">CommonParameters</span></span>
<span data-ttu-id="0cd2a-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd2a-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd2a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd2a-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0cd2a-126">INPUTS</span></span>

### <span data-ttu-id="0cd2a-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0cd2a-127">None</span></span>
<span data-ttu-id="0cd2a-128">Questo cmdlet non accetta l'input da pipeline.</span><span class="sxs-lookup"><span data-stu-id="0cd2a-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="0cd2a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0cd2a-129">OUTPUTS</span></span>

### <span data-ttu-id="0cd2a-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0cd2a-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="0cd2a-131">Questo cmdlet crea istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="0cd2a-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="0cd2a-132">Note</span><span class="sxs-lookup"><span data-stu-id="0cd2a-132">NOTES</span></span>

## <span data-ttu-id="0cd2a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0cd2a-133">RELATED LINKS</span></span>

[<span data-ttu-id="0cd2a-134">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0cd2a-134">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="0cd2a-135">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0cd2a-135">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="0cd2a-136">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0cd2a-136">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

