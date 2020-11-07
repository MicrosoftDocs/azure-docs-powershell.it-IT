---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2fec428adb2ba8621d09a1f0ae5e762cdbe4b913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687505"
---
# <span data-ttu-id="6a594-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6a594-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="6a594-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a594-102">SYNOPSIS</span></span>
<span data-ttu-id="6a594-103">Crea un'autorizzazione per il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6a594-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a594-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a594-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a594-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a594-105">DESCRIPTION</span></span>
<span data-ttu-id="6a594-106">Il cmdlet **New-AzureRmExpressRouteCircuitAuthorization** crea un'autorizzazione Circuit che può essere aggiunta a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6a594-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="6a594-107">Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="6a594-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="6a594-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere una rete al circuito.</span><span class="sxs-lookup"><span data-stu-id="6a594-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="6a594-109">Può essere disponibile una sola autorizzazione per ogni rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6a594-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="6a594-110">Dopo aver creato un circuito ExpressRoute, è possibile usare **Add-AzureRmExpressRouteCircuitAuthorization** per aggiungere un'autorizzazione al circuito.</span><span class="sxs-lookup"><span data-stu-id="6a594-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="6a594-111">In alternativa, puoi usare **New-AzureRmExpressRouteCircuitAuthorization** per creare un'autorizzazione che può essere aggiunta a un nuovo circuito contemporaneamente alla creazione del circuito.</span><span class="sxs-lookup"><span data-stu-id="6a594-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="6a594-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a594-112">EXAMPLES</span></span>

### <span data-ttu-id="6a594-113">Esempio 1: creare una nuova autorizzazione Circuit</span><span class="sxs-lookup"><span data-stu-id="6a594-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="6a594-114">Questo comando crea una nuova autorizzazione Circuit denominata ContosoCircuitAuthorization e quindi archivia tale oggetto in una variabile denominata $Authorization.</span><span class="sxs-lookup"><span data-stu-id="6a594-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="6a594-115">Il salvataggio dell'oggetto in una variabile è importante: anche se **New-AzureRmExpressRouteCircuitAuthorization** può creare un'autorizzazione Circuit, non può aggiungere l'autorizzazione a una route Circuit.</span><span class="sxs-lookup"><span data-stu-id="6a594-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="6a594-116">La variabile $Authorization viene invece usata New-AzureRmExpressRouteCircuit quando si crea un nuovo circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6a594-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="6a594-117">Per altre informazioni, vedere la documentazione relativa al cmdlet New-AzureRmExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="6a594-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="6a594-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a594-118">PARAMETERS</span></span>

### <span data-ttu-id="6a594-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a594-119">-Name</span></span>
<span data-ttu-id="6a594-120">Specifica un nome univoco per la nuova autorizzazione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6a594-120">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="6a594-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a594-121">-DefaultProfile</span></span>
<span data-ttu-id="6a594-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a594-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a594-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a594-123">CommonParameters</span></span>
<span data-ttu-id="6a594-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a594-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a594-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a594-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a594-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a594-126">INPUTS</span></span>

### <span data-ttu-id="6a594-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6a594-127">None</span></span>
<span data-ttu-id="6a594-128">Questo cmdlet non accetta l'input da pipeline.</span><span class="sxs-lookup"><span data-stu-id="6a594-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="6a594-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a594-129">OUTPUTS</span></span>

### <span data-ttu-id="6a594-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6a594-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="6a594-131">Questo cmdlet crea istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="6a594-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="6a594-132">Note</span><span class="sxs-lookup"><span data-stu-id="6a594-132">NOTES</span></span>

## <span data-ttu-id="6a594-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a594-133">RELATED LINKS</span></span>

[<span data-ttu-id="6a594-134">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6a594-134">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="6a594-135">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6a594-135">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="6a594-136">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6a594-136">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

