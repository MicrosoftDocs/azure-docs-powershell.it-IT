---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189070"
---
# <span data-ttu-id="3046a-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3046a-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="3046a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3046a-102">SYNOPSIS</span></span>
<span data-ttu-id="3046a-103">Ottiene informazioni sulle autorizzazioni del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3046a-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="3046a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3046a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3046a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3046a-105">DESCRIPTION</span></span>
<span data-ttu-id="3046a-106">Il cmdlet **Get-AzExpressRouteCircuitAuthorization** ottiene informazioni sulle autorizzazioni assegnate a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3046a-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="3046a-107">Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="3046a-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="3046a-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere la propria rete al circuito (un'autorizzazione per rete virtuale).</span><span class="sxs-lookup"><span data-stu-id="3046a-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="3046a-109">Le chiavi di autorizzazione, oltre ad altre informazioni sull'autorizzazione, possono essere visualizzate in qualsiasi momento eseguendo **Get-AzExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="3046a-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="3046a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3046a-110">EXAMPLES</span></span>

### <span data-ttu-id="3046a-111">Esempio 1: ottenere tutte le autorizzazioni di ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3046a-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="3046a-112">Questi comandi restituiscono informazioni su tutte le autorizzazioni di ExpressRoute associate a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3046a-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="3046a-113">Il primo comando usa il cmdlet **Get-AzExpressRouteCircuit** per creare un riferimento a un oggetto Circuit denominato ContosoCircuit; il riferimento all'oggetto è archiviato nella variabile $Circuit.</span><span class="sxs-lookup"><span data-stu-id="3046a-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="3046a-114">Il secondo comando usa quindi il riferimento oggetto e il cmdlet **Get-AzExpressRouteCircuitAuthorization** per restituire informazioni sulle autorizzazioni associate a ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="3046a-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="3046a-115">Esempio 2: ottenere tutte le autorizzazioni di ExpressRoute usando il cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="3046a-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="3046a-116">Questi comandi rappresentano una variante dei comandi usati nell'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="3046a-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="3046a-117">In questo caso, tuttavia, le informazioni vengono restituite solo per le autorizzazioni disponibili per l'uso, ovvero per le autorizzazioni che non sono state assegnate a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3046a-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="3046a-118">A questo scopo, le informazioni sull'autorizzazione Circuit vengono restituite nel comando 2 e vengono inviate tramite pipe al cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="3046a-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="3046a-119">**Where-Object** seleziona solo le autorizzazioni in cui la proprietà *AuthorizationUseStatus* è impostata su available.</span><span class="sxs-lookup"><span data-stu-id="3046a-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="3046a-120">Per elencare solo le autorizzazioni non disponibili, usare questa sintassi per la clausola WHERE: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="3046a-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="3046a-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3046a-121">PARAMETERS</span></span>

### <span data-ttu-id="3046a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3046a-122">-DefaultProfile</span></span>
<span data-ttu-id="3046a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3046a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3046a-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3046a-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3046a-125">Specifica l'autorizzazione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3046a-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="3046a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3046a-126">-Name</span></span>
<span data-ttu-id="3046a-127">Specifica il nome dell'autorizzazione del circuito ExpressRoute che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3046a-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="3046a-128">-Nome "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="3046a-128">-Name "ContosoCircuitAuthorization"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3046a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3046a-129">CommonParameters</span></span>
<span data-ttu-id="3046a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3046a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3046a-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3046a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3046a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3046a-132">INPUTS</span></span>

### <span data-ttu-id="3046a-133">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3046a-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3046a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3046a-134">OUTPUTS</span></span>

### <span data-ttu-id="3046a-135">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3046a-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="3046a-136">Note</span><span class="sxs-lookup"><span data-stu-id="3046a-136">NOTES</span></span>

## <span data-ttu-id="3046a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3046a-137">RELATED LINKS</span></span>

[<span data-ttu-id="3046a-138">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3046a-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="3046a-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3046a-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="3046a-140">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3046a-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="3046a-141">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3046a-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)