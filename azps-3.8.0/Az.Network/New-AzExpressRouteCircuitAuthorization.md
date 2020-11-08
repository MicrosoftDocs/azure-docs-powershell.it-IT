---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022706"
---
# <span data-ttu-id="229e7-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="229e7-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="229e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="229e7-102">SYNOPSIS</span></span>
<span data-ttu-id="229e7-103">Crea un'autorizzazione per il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="229e7-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="229e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="229e7-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="229e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="229e7-105">DESCRIPTION</span></span>
<span data-ttu-id="229e7-106">Il cmdlet **New-AzExpressRouteCircuitAuthorization** crea un'autorizzazione Circuit che può essere aggiunta a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="229e7-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="229e7-107">Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="229e7-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="229e7-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere una rete al circuito.</span><span class="sxs-lookup"><span data-stu-id="229e7-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="229e7-109">Può essere disponibile una sola autorizzazione per ogni rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="229e7-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="229e7-110">Dopo aver creato un circuito ExpressRoute, è possibile usare **Add-AzExpressRouteCircuitAuthorization** per aggiungere un'autorizzazione al circuito.</span><span class="sxs-lookup"><span data-stu-id="229e7-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="229e7-111">In alternativa, puoi usare **New-AzExpressRouteCircuitAuthorization** per creare un'autorizzazione che può essere aggiunta a un nuovo circuito contemporaneamente alla creazione del circuito.</span><span class="sxs-lookup"><span data-stu-id="229e7-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="229e7-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="229e7-112">EXAMPLES</span></span>

### <span data-ttu-id="229e7-113">Esempio 1: creare una nuova autorizzazione Circuit</span><span class="sxs-lookup"><span data-stu-id="229e7-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="229e7-114">Questo comando crea una nuova autorizzazione Circuit denominata ContosoCircuitAuthorization e quindi archivia tale oggetto in una variabile denominata $Authorization.</span><span class="sxs-lookup"><span data-stu-id="229e7-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="229e7-115">Il salvataggio dell'oggetto in una variabile è importante: anche se **New-AzExpressRouteCircuitAuthorization** può creare un'autorizzazione Circuit, non può aggiungere l'autorizzazione a una route Circuit.</span><span class="sxs-lookup"><span data-stu-id="229e7-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="229e7-116">La variabile $Authorization viene invece usata New-AzExpressRouteCircuit quando si crea un nuovo circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="229e7-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="229e7-117">Per altre informazioni, vedere la documentazione relativa al cmdlet New-AzExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="229e7-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="229e7-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="229e7-118">PARAMETERS</span></span>

### <span data-ttu-id="229e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="229e7-119">-DefaultProfile</span></span>
<span data-ttu-id="229e7-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="229e7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="229e7-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="229e7-121">-Name</span></span>
<span data-ttu-id="229e7-122">Specifica un nome univoco per la nuova autorizzazione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="229e7-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="229e7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229e7-123">CommonParameters</span></span>
<span data-ttu-id="229e7-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="229e7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229e7-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="229e7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229e7-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="229e7-126">INPUTS</span></span>

### <span data-ttu-id="229e7-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="229e7-127">None</span></span>

## <span data-ttu-id="229e7-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="229e7-128">OUTPUTS</span></span>

### <span data-ttu-id="229e7-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="229e7-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="229e7-130">Note</span><span class="sxs-lookup"><span data-stu-id="229e7-130">NOTES</span></span>

## <span data-ttu-id="229e7-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="229e7-131">RELATED LINKS</span></span>

[<span data-ttu-id="229e7-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="229e7-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="229e7-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="229e7-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="229e7-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="229e7-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

