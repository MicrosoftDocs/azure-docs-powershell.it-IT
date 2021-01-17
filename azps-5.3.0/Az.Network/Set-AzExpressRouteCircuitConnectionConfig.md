---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486623"
---
# <span data-ttu-id="72eea-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="72eea-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="72eea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72eea-102">SYNOPSIS</span></span>
<span data-ttu-id="72eea-103">Aggiorna una configurazione di connessione circuitale creata in Peerings privati per un circuito di Route Express.</span><span class="sxs-lookup"><span data-stu-id="72eea-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="72eea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72eea-104">SYNTAX</span></span>

### <span data-ttu-id="72eea-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72eea-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72eea-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="72eea-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72eea-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72eea-107">DESCRIPTION</span></span>
<span data-ttu-id="72eea-108">Il cmdlet **set-AzExpressRouteCircuitConnectionConfig** aggiorna una configurazione di connessione circuitale creata in peering privato per un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="72eea-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="72eea-109">In questo modo, è possibile peering due circuiti di Route Express tra aree o abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="72eea-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="72eea-110">Tieni presente che, prima di eseguire **set-AzExpressRouteCircuitConnectionConfig** , devi aggiungere la connessione Circuit tramite **Add-AzExpressRouteCircuitConnectionConfig**.</span><span class="sxs-lookup"><span data-stu-id="72eea-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="72eea-111">Inoltre, dopo aver eseguito **set-AzExpressRouteCircuitPeeringConfig**, devi chiamare il cmdlet Set-AzExpressRouteCircuit per attivare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="72eea-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="72eea-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72eea-112">EXAMPLES</span></span>

### <span data-ttu-id="72eea-113">Esempio 1: aggiornare una risorsa di connessione Circuit a un circuito ExpressRoute esistente</span><span class="sxs-lookup"><span data-stu-id="72eea-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="72eea-114">Esempio 2: impostare una configurazione di connessione circuitale tramite piping su un circuito ExpressRoute esistente</span><span class="sxs-lookup"><span data-stu-id="72eea-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="72eea-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72eea-115">PARAMETERS</span></span>

### <span data-ttu-id="72eea-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="72eea-116">-AddressPrefix</span></span>
<span data-ttu-id="72eea-117">Uno spazio di indirizzi minimo/29 per creare tunnel VxLan tra i circuiti di Route Express per i tunnel IPv4.</span><span class="sxs-lookup"><span data-stu-id="72eea-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="72eea-118">o uno spazio di indirizzi cliente minimo/125 per creare tunnel VxLan tra i circuiti di Route Express per i tunnel IPv6.</span><span class="sxs-lookup"><span data-stu-id="72eea-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="72eea-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="72eea-119">-AddressPrefixType</span></span>
<span data-ttu-id="72eea-120">Specifica la famiglia di indirizzi a cui appartiene il prefisso Address.</span><span class="sxs-lookup"><span data-stu-id="72eea-120">Specifies the address family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="72eea-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="72eea-121">-AuthorizationKey</span></span>
<span data-ttu-id="72eea-122">Chiave di autorizzazione per il circuito di routing espresso peer in un altro abbonamento.</span><span class="sxs-lookup"><span data-stu-id="72eea-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="72eea-123">L'autorizzazione sul circuito peer può essere creata usando i comandi esistenti.</span><span class="sxs-lookup"><span data-stu-id="72eea-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="72eea-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72eea-124">-DefaultProfile</span></span>
<span data-ttu-id="72eea-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72eea-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72eea-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72eea-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="72eea-127">Il circuito ExpressRoute da modificare.</span><span class="sxs-lookup"><span data-stu-id="72eea-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="72eea-128">Questo è un oggetto Azure restituito dal cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="72eea-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="72eea-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="72eea-129">-Name</span></span>
<span data-ttu-id="72eea-130">Nome della risorsa di connessione Circuit da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="72eea-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="72eea-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="72eea-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="72eea-132">ID risorsa per peering privato del circuito remoto che verrà peered con il circuito corrente.</span><span class="sxs-lookup"><span data-stu-id="72eea-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="72eea-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72eea-133">-Confirm</span></span>
<span data-ttu-id="72eea-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72eea-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72eea-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72eea-135">-WhatIf</span></span>
<span data-ttu-id="72eea-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72eea-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72eea-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72eea-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72eea-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72eea-138">CommonParameters</span></span>
<span data-ttu-id="72eea-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72eea-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72eea-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72eea-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72eea-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72eea-141">INPUTS</span></span>

### <span data-ttu-id="72eea-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72eea-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="72eea-143">System. String</span><span class="sxs-lookup"><span data-stu-id="72eea-143">System.String</span></span>

## <span data-ttu-id="72eea-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72eea-144">OUTPUTS</span></span>

### <span data-ttu-id="72eea-145">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72eea-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="72eea-146">Note</span><span class="sxs-lookup"><span data-stu-id="72eea-146">NOTES</span></span>

## <span data-ttu-id="72eea-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72eea-147">RELATED LINKS</span></span>

[<span data-ttu-id="72eea-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="72eea-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="72eea-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="72eea-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="72eea-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="72eea-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="72eea-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72eea-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="72eea-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="72eea-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
