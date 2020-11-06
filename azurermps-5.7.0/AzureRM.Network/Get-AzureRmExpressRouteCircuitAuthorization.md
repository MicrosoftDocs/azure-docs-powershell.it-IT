---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 3aed1a20a8a5878819ea3634ff5d31babba3261c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515599"
---
# <span data-ttu-id="1d9b6-101">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1d9b6-101">Get-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="1d9b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d9b6-102">SYNOPSIS</span></span>
<span data-ttu-id="1d9b6-103">Ottiene informazioni sulle autorizzazioni del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-103">Gets information about ExpressRoute circuit authorizations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d9b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d9b6-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d9b6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d9b6-105">DESCRIPTION</span></span>
<span data-ttu-id="1d9b6-106">Il cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** ottiene informazioni sulle autorizzazioni assegnate a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-106">The **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="1d9b6-107">Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="1d9b6-108">Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere la propria rete al circuito (un'autorizzazione per rete virtuale).</span><span class="sxs-lookup"><span data-stu-id="1d9b6-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="1d9b6-109">Le chiavi di autorizzazione, oltre ad altre informazioni sull'autorizzazione, possono essere visualizzate in qualsiasi momento eseguendo **Get-AzureRmExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzureRmExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="1d9b6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d9b6-110">EXAMPLES</span></span>

### <span data-ttu-id="1d9b6-111">Esempio 1: ottenere tutte le autorizzazioni di ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="1d9b6-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="1d9b6-112">Questi comandi restituiscono informazioni su tutte le autorizzazioni di ExpressRoute associate a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="1d9b6-113">Il primo comando usa il cmdlet **Get-AzureRmExpressRouteCircuit** per creare un riferimento a un oggetto Circuit denominato ContosoCircuit; il riferimento all'oggetto è archiviato nella variabile $Circuit.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-113">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="1d9b6-114">Il secondo comando usa quindi il riferimento oggetto e il cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** per restituire informazioni sulle autorizzazioni associate a ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-114">The second command then uses that object reference and the **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="1d9b6-115">Esempio 2: ottenere tutte le autorizzazioni di ExpressRoute usando il cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="1d9b6-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="1d9b6-116">Questi comandi rappresentano una variante dei comandi usati nell'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="1d9b6-117">In questo caso, tuttavia, le informazioni vengono restituite solo per le autorizzazioni disponibili per l'uso, ovvero per le autorizzazioni che non sono state assegnate a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="1d9b6-118">A questo scopo, le informazioni sull'autorizzazione Circuit vengono restituite nel comando 2 e vengono inviate tramite pipe al cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="1d9b6-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="1d9b6-119">**Where-Object** seleziona solo le autorizzazioni in cui la proprietà *AuthorizationUseStatus* è impostata su available.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="1d9b6-120">Per elencare solo le autorizzazioni non disponibili, usare questa sintassi per la clausola WHERE:</span><span class="sxs-lookup"><span data-stu-id="1d9b6-120">To list only those authorizations that are not available, use this syntax for the Where clause:</span></span>

`{$_.AuthorizationUseStatus -ne "Available"}`

## <span data-ttu-id="1d9b6-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d9b6-121">PARAMETERS</span></span>

### <span data-ttu-id="1d9b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d9b6-122">-DefaultProfile</span></span>
<span data-ttu-id="1d9b6-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d9b6-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1d9b6-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="1d9b6-125">Specifica l'autorizzazione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="1d9b6-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d9b6-126">-Name</span></span>
<span data-ttu-id="1d9b6-127">Specifica il nome dell'autorizzazione del circuito ExpressRoute che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>

<span data-ttu-id="1d9b6-128">-Nome "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="1d9b6-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="1d9b6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d9b6-129">CommonParameters</span></span>
<span data-ttu-id="1d9b6-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d9b6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d9b6-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d9b6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d9b6-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d9b6-132">INPUTS</span></span>

### <span data-ttu-id="1d9b6-133">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1d9b6-133">PSExpressRouteCircuit</span></span>
<span data-ttu-id="1d9b6-134">**Get-AzureRmExpressRouteCircuitAuthorization** accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="1d9b6-134">**Get-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="1d9b6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d9b6-135">OUTPUTS</span></span>

### <span data-ttu-id="1d9b6-136">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1d9b6-136">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="1d9b6-137">**Get-AzureRmExpressRouteCircuitAuthorization** restituisce le istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="1d9b6-137">**Get-AzureRmExpressRouteCircuitAuthorization** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="1d9b6-138">Note</span><span class="sxs-lookup"><span data-stu-id="1d9b6-138">NOTES</span></span>

## <span data-ttu-id="1d9b6-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d9b6-139">RELATED LINKS</span></span>

[<span data-ttu-id="1d9b6-140">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1d9b6-140">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="1d9b6-141">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1d9b6-141">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="1d9b6-142">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1d9b6-142">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="1d9b6-143">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1d9b6-143">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
