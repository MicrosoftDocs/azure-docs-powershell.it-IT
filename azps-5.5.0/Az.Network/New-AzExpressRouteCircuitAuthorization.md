---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189694"
---
# <span data-ttu-id="3dda7-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3dda7-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="3dda7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dda7-102">SYNOPSIS</span></span>
<span data-ttu-id="3dda7-103">Crea un'autorizzazione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3dda7-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="3dda7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dda7-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dda7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3dda7-105">DESCRIPTION</span></span>
<span data-ttu-id="3dda7-106">Il cmdlet **New-AzExpressRouteCircuitAuthorization** crea un'autorizzazione del circuito che può essere aggiunta a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3dda7-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="3dda7-107">I circuiti ExpressRoute connettono la rete locale al cloud Microsoft usando un provider di connettività invece di Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="3dda7-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="3dda7-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata dal proprietario di una rete virtuale per connettere una rete al circuito.</span><span class="sxs-lookup"><span data-stu-id="3dda7-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="3dda7-109">È possibile un'unica autorizzazione per ogni rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3dda7-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="3dda7-110">Dopo aver creato un circuito ExpressRoute, è possibile usare **Add-AzExpressRouteCircuitAuthorization** per aggiungere un'autorizzazione a tale circuito.</span><span class="sxs-lookup"><span data-stu-id="3dda7-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="3dda7-111">In alternativa, è possibile usare **New-AzExpressRouteCircuitAuthorization** per creare un'autorizzazione che può essere aggiunta a un nuovo circuito nello stesso momento in cui viene creato il circuito.</span><span class="sxs-lookup"><span data-stu-id="3dda7-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="3dda7-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dda7-112">EXAMPLES</span></span>

### <span data-ttu-id="3dda7-113">Esempio 1: Creare una nuova autorizzazione del circuito</span><span class="sxs-lookup"><span data-stu-id="3dda7-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="3dda7-114">Questo comando crea una nuova autorizzazione di circuito denominata ContosoCircuitAuthorization e quindi archivia l'oggetto in una variabile denominata $Authorization.</span><span class="sxs-lookup"><span data-stu-id="3dda7-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="3dda7-115">Salvare l'oggetto in una variabile è importante: anche se **New-AzExpressRouteCircuitAuthorization** può creare un'autorizzazione di circuito, non può aggiungerla a un percorso di circuito.</span><span class="sxs-lookup"><span data-stu-id="3dda7-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="3dda7-116">La variabile $Authorization viene usata New-AzExpressRouteCircuit durante la creazione di un nuovo circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3dda7-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="3dda7-117">Per altre informazioni, vedere la documentazione del cmdlet New-AzExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="3dda7-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="3dda7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dda7-118">PARAMETERS</span></span>

### <span data-ttu-id="3dda7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dda7-119">-DefaultProfile</span></span>
<span data-ttu-id="3dda7-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dda7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dda7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3dda7-121">-Name</span></span>
<span data-ttu-id="3dda7-122">Specifica un nome univoco per la nuova autorizzazione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3dda7-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="3dda7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dda7-123">CommonParameters</span></span>
<span data-ttu-id="3dda7-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dda7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dda7-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dda7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dda7-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="3dda7-126">INPUTS</span></span>

### <span data-ttu-id="3dda7-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3dda7-127">None</span></span>

## <span data-ttu-id="3dda7-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dda7-128">OUTPUTS</span></span>

### <span data-ttu-id="3dda7-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3dda7-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="3dda7-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="3dda7-130">NOTES</span></span>

## <span data-ttu-id="3dda7-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dda7-131">RELATED LINKS</span></span>

[<span data-ttu-id="3dda7-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3dda7-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="3dda7-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3dda7-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="3dda7-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3dda7-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

