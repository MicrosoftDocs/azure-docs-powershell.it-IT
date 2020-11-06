---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: aab4e78cd01e814ed8eb81b820e20bd3da4c03f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520948"
---
# <span data-ttu-id="45339-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="45339-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="45339-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45339-102">SYNOPSIS</span></span>
<span data-ttu-id="45339-103">Aggiunge una configurazione di connessione Circuit a un peering privato di un circuito di route espresso.</span><span class="sxs-lookup"><span data-stu-id="45339-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45339-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45339-104">SYNTAX</span></span>

### <span data-ttu-id="45339-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="45339-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45339-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="45339-106">SetByResourceId</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45339-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45339-107">DESCRIPTION</span></span>
<span data-ttu-id="45339-108">Il cmdlet **Add-AzureRmExpressRouteCircuitConnectionConfig** aggiunge una configurazione di connessione Circuit a peering privato per un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="45339-108">The **Add-AzureRmExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="45339-109">In questo modo, è possibile peering due circuiti di Route Express tra aree o abbonamenti. Tieni presente che, dopo aver eseguito **Add-AzureRmExpressRouteCircuitPeeringConfig** , devi chiamare il cmdlet Set-AzureRmExpressRouteCircuit per attivare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="45339-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="45339-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45339-110">EXAMPLES</span></span>

### <span data-ttu-id="45339-111">Esempio 1: aggiungere una risorsa di connessione Circuit a un circuito ExpressRoute esistente</span><span class="sxs-lookup"><span data-stu-id="45339-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="45339-112">Esempio 2: aggiungere una configurazione di connessione circuitale tramite piping a un circuito ExpressRoute esistente</span><span class="sxs-lookup"><span data-stu-id="45339-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="45339-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45339-113">PARAMETERS</span></span>

### <span data-ttu-id="45339-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="45339-114">-AddressPrefix</span></span>
<span data-ttu-id="45339-115">Uno spazio di indirizzi minimo/29 per creare tunnel VxLan tra i circuiti di Route Express</span><span class="sxs-lookup"><span data-stu-id="45339-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="45339-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="45339-116">-AuthorizationKey</span></span>
<span data-ttu-id="45339-117">Chiave di autorizzazione per il circuito di routing espresso peer in un altro abbonamento.</span><span class="sxs-lookup"><span data-stu-id="45339-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="45339-118">L'autorizzazione sul circuito peer può essere creata usando i comandi esistenti.</span><span class="sxs-lookup"><span data-stu-id="45339-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="45339-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45339-119">-DefaultProfile</span></span>
<span data-ttu-id="45339-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45339-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45339-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="45339-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="45339-122">Il circuito ExpressRoute da modificare.</span><span class="sxs-lookup"><span data-stu-id="45339-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="45339-123">Questo è un oggetto Azure restituito dal cmdlet **Get-AzureRmExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="45339-123">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="45339-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="45339-124">-Name</span></span>
<span data-ttu-id="45339-125">Nome della risorsa di connessione Circuit da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="45339-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="45339-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="45339-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="45339-127">ID risorsa per peering privato del circuito remoto che verrà peered con il circuito corrente.</span><span class="sxs-lookup"><span data-stu-id="45339-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="45339-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45339-128">-Confirm</span></span>
<span data-ttu-id="45339-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45339-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45339-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45339-130">-WhatIf</span></span>
<span data-ttu-id="45339-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45339-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45339-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45339-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45339-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45339-133">CommonParameters</span></span>
<span data-ttu-id="45339-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45339-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45339-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45339-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45339-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45339-136">INPUTS</span></span>

### <span data-ttu-id="45339-137">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="45339-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="45339-138">Parametri: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="45339-138">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="45339-139">System. String</span><span class="sxs-lookup"><span data-stu-id="45339-139">System.String</span></span>

## <span data-ttu-id="45339-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45339-140">OUTPUTS</span></span>

### <span data-ttu-id="45339-141">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="45339-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="45339-142">Note</span><span class="sxs-lookup"><span data-stu-id="45339-142">NOTES</span></span>

## <span data-ttu-id="45339-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45339-143">RELATED LINKS</span></span>

[<span data-ttu-id="45339-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="45339-144">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="45339-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="45339-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="45339-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="45339-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="45339-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="45339-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="45339-148">New-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="45339-148">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="45339-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="45339-149">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="45339-150">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="45339-150">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
