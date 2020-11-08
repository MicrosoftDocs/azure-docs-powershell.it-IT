---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: e8691d31956e1ee59f692cc3d37fa1e2d5598efa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192860"
---
# <span data-ttu-id="89e4a-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="89e4a-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="89e4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="89e4a-103">Aggiunge una configurazione di connessione Circuit a un peering privato di un circuito di route espresso.</span><span class="sxs-lookup"><span data-stu-id="89e4a-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="89e4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89e4a-104">SYNTAX</span></span>

### <span data-ttu-id="89e4a-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="89e4a-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89e4a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="89e4a-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89e4a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89e4a-107">DESCRIPTION</span></span>
<span data-ttu-id="89e4a-108">Il cmdlet **Add-AzExpressRouteCircuitConnectionConfig** aggiunge una configurazione di connessione Circuit a peering privato per un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="89e4a-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="89e4a-109">In questo modo, è possibile peering due circuiti di Route Express tra aree o abbonamenti. Tieni presente che, dopo aver eseguito **Add-AzExpressRouteCircuitConnectionConfig** , devi chiamare il cmdlet Set-AzExpressRouteCircuit per attivare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="89e4a-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="89e4a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89e4a-110">EXAMPLES</span></span>

### <span data-ttu-id="89e4a-111">Esempio 1: aggiungere una risorsa di connessione Circuit a un circuito ExpressRoute esistente</span><span class="sxs-lookup"><span data-stu-id="89e4a-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="89e4a-112">Esempio 2: aggiungere una configurazione di connessione circuitale tramite piping a un circuito ExpressRoute esistente</span><span class="sxs-lookup"><span data-stu-id="89e4a-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="89e4a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89e4a-113">PARAMETERS</span></span>

### <span data-ttu-id="89e4a-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="89e4a-114">-AddressPrefix</span></span>
<span data-ttu-id="89e4a-115">Uno spazio di indirizzi minimo/29 per creare tunnel VxLan tra i circuiti di Route Express per i tunnel IPv4.</span><span class="sxs-lookup"><span data-stu-id="89e4a-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="89e4a-116">o uno spazio di indirizzi cliente minimo/125 per creare tunnel VxLan tra i circuiti di Route Express per i tunnel IPv6.</span><span class="sxs-lookup"><span data-stu-id="89e4a-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="89e4a-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="89e4a-117">-AddressPrefixType</span></span>
<span data-ttu-id="89e4a-118">Specifica la famiglia di indirizzi a cui appartiene il prefisso Address.</span><span class="sxs-lookup"><span data-stu-id="89e4a-118">This specifies the Address Family that address prefix belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: IPv4
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89e4a-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="89e4a-119">-AuthorizationKey</span></span>
<span data-ttu-id="89e4a-120">Chiave di autorizzazione per il circuito di routing espresso peer in un altro abbonamento.</span><span class="sxs-lookup"><span data-stu-id="89e4a-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="89e4a-121">L'autorizzazione sul circuito peer può essere creata usando i comandi esistenti.</span><span class="sxs-lookup"><span data-stu-id="89e4a-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="89e4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e4a-122">-DefaultProfile</span></span>
<span data-ttu-id="89e4a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89e4a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89e4a-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="89e4a-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="89e4a-125">Il circuito ExpressRoute da modificare.</span><span class="sxs-lookup"><span data-stu-id="89e4a-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="89e4a-126">Questo è un oggetto Azure restituito dal cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="89e4a-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="89e4a-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="89e4a-127">-Name</span></span>
<span data-ttu-id="89e4a-128">Nome della risorsa di connessione Circuit da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="89e4a-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="89e4a-129">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="89e4a-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="89e4a-130">ID risorsa per peering privato del circuito remoto che verrà peered con il circuito corrente.</span><span class="sxs-lookup"><span data-stu-id="89e4a-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="89e4a-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="89e4a-131">-Confirm</span></span>
<span data-ttu-id="89e4a-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89e4a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89e4a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89e4a-133">-WhatIf</span></span>
<span data-ttu-id="89e4a-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89e4a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89e4a-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89e4a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89e4a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e4a-136">CommonParameters</span></span>
<span data-ttu-id="89e4a-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e4a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e4a-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e4a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e4a-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89e4a-139">INPUTS</span></span>

### <span data-ttu-id="89e4a-140">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="89e4a-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="89e4a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="89e4a-141">System.String</span></span>

## <span data-ttu-id="89e4a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89e4a-142">OUTPUTS</span></span>

### <span data-ttu-id="89e4a-143">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="89e4a-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="89e4a-144">Note</span><span class="sxs-lookup"><span data-stu-id="89e4a-144">NOTES</span></span>

## <span data-ttu-id="89e4a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89e4a-145">RELATED LINKS</span></span>

[<span data-ttu-id="89e4a-146">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="89e4a-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="89e4a-147">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="89e4a-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="89e4a-148">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="89e4a-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="89e4a-149">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="89e4a-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="89e4a-150">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="89e4a-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)