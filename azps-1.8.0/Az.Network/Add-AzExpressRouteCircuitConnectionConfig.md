---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bc08305d7aa604dd9c7540573ffb5a199e85b287
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402134"
---
# <span data-ttu-id="0dfc0-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0dfc0-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="0dfc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dfc0-102">SYNOPSIS</span></span>
<span data-ttu-id="0dfc0-103">Aggiunge una configurazione di connessione a un circuito al peering privato di un circuito Express Route.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="0dfc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0dfc0-104">SYNTAX</span></span>

### <span data-ttu-id="0dfc0-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="0dfc0-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dfc0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0dfc0-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dfc0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0dfc0-107">DESCRIPTION</span></span>
<span data-ttu-id="0dfc0-108">Il cmdlet **Add-AzExpressRouteCircuitConnectionConfig aggiunge** una configurazione della connessione al circuito al peering privato per un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="0dfc0-109">Ciò consente il peering di due circuiti Express Route tra aree geografiche o abbonamenti. Si noti che, dopo aver eseguito **Add-AzExpressRouteCircuitIingConfig,** è necessario chiamare il cmdlet Set-AzExpressRouteCircuit per attivare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="0dfc0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0dfc0-110">EXAMPLES</span></span>

### <span data-ttu-id="0dfc0-111">Esempio 1: Aggiungere una risorsa di connessione a un circuito ExpressRoute esistente</span><span class="sxs-lookup"><span data-stu-id="0dfc0-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="0dfc0-112">Esempio 2: Aggiungere una configurazione di connessione a un circuito tramite Piping a un circuito ExpressRoute esistente</span><span class="sxs-lookup"><span data-stu-id="0dfc0-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="0dfc0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dfc0-113">PARAMETERS</span></span>

### <span data-ttu-id="0dfc0-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0dfc0-114">-AddressPrefix</span></span>
<span data-ttu-id="0dfc0-115">Uno spazio minimo di indirizzi 29 per i clienti per creare tunnel VxLan tra i circuiti Express Route</span><span class="sxs-lookup"><span data-stu-id="0dfc0-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfc0-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="0dfc0-116">-AuthorizationKey</span></span>
<span data-ttu-id="0dfc0-117">Chiave di autorizzazione per il peer express route circuit in un altro abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="0dfc0-118">L'autorizzazione sul circuito peer può essere creata usando comandi esistenti.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="0dfc0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dfc0-119">-DefaultProfile</span></span>
<span data-ttu-id="0dfc0-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dfc0-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0dfc0-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0dfc0-122">Il circuito ExpressRoute da modificare.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="0dfc0-123">Oggetto Azure restituito dal cmdlet **Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="0dfc0-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dfc0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0dfc0-124">-Name</span></span>
<span data-ttu-id="0dfc0-125">Nome della risorsa di connessione al circuito da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-125">The name of the circuit connection resource to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfc0-126">-PeerExpressRouteCircuit Più</span><span class="sxs-lookup"><span data-stu-id="0dfc0-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="0dfc0-127">ID risorsa per il peering privato del circuito remoto che verrà peered con il circuito corrente.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dfc0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dfc0-128">-Confirm</span></span>
<span data-ttu-id="0dfc0-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfc0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dfc0-130">-WhatIf</span></span>
<span data-ttu-id="0dfc0-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0dfc0-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfc0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dfc0-133">CommonParameters</span></span>
<span data-ttu-id="0dfc0-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dfc0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dfc0-135">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dfc0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dfc0-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="0dfc0-136">INPUTS</span></span>

### <span data-ttu-id="0dfc0-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0dfc0-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="0dfc0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0dfc0-138">System.String</span></span>

## <span data-ttu-id="0dfc0-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0dfc0-139">OUTPUTS</span></span>

### <span data-ttu-id="0dfc0-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0dfc0-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0dfc0-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="0dfc0-141">NOTES</span></span>

## <span data-ttu-id="0dfc0-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0dfc0-142">RELATED LINKS</span></span>

[<span data-ttu-id="0dfc0-143">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0dfc0-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="0dfc0-144">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0dfc0-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0dfc0-145">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0dfc0-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)





[<span data-ttu-id="0dfc0-146">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0dfc0-146">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="0dfc0-147">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0dfc0-147">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
