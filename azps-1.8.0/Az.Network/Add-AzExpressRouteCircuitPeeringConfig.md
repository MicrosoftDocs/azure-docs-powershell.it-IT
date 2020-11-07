---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b7b28c9d2b1dd687759ae75db64039cbfb6d5d9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678677"
---
# <span data-ttu-id="3b878-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3b878-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="3b878-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b878-102">SYNOPSIS</span></span>
<span data-ttu-id="3b878-103">Aggiunge una configurazione peering a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3b878-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="3b878-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b878-104">SYNTAX</span></span>

### <span data-ttu-id="3b878-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b878-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b878-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="3b878-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b878-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="3b878-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b878-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b878-108">DESCRIPTION</span></span>
<span data-ttu-id="3b878-109">Il cmdlet **Add-AzExpressRouteCircuitPeeringConfig** aggiunge una configurazione di peering a un circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3b878-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="3b878-110">Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="3b878-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="3b878-111">Tieni presente che, dopo aver eseguito **Add-AzExpressRouteCircuitPeeringConfig** , devi chiamare il cmdlet Set-AzExpressRouteCircuit per attivare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="3b878-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="3b878-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b878-112">EXAMPLES</span></span>

### <span data-ttu-id="3b878-113">Esempio 1: aggiungere un peer a un circuito ExpressRoute esistente</span><span class="sxs-lookup"><span data-stu-id="3b878-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="3b878-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b878-114">PARAMETERS</span></span>

### <span data-ttu-id="3b878-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b878-115">-DefaultProfile</span></span>
<span data-ttu-id="3b878-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b878-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b878-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3b878-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3b878-118">Il circuito ExpressRoute da modificare.</span><span class="sxs-lookup"><span data-stu-id="3b878-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="3b878-119">Questo è un oggetto Azure restituito dal cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="3b878-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="3b878-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="3b878-120">-LegacyMode</span></span>
<span data-ttu-id="3b878-121">Modalità legacy del peering</span><span class="sxs-lookup"><span data-stu-id="3b878-121">The legacy mode of the Peering</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b878-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="3b878-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="3b878-123">Per un PeeringType di MicrosoftPeering, è necessario specificare un elenco di tutti i prefissi che si prevede di pubblicizzare durante la sessione BGP.</span><span class="sxs-lookup"><span data-stu-id="3b878-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="3b878-124">Vengono accettati solo i prefissi degli indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="3b878-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="3b878-125">Se si prevede di inviare un set di prefissi, è possibile inviare un elenco separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="3b878-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="3b878-126">Questi prefissi devono essere registrati in un nome del registro di sistema di routing (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="3b878-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b878-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="3b878-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="3b878-128">Per i prefissi pubblicitari non registrati nel numero di peering, è possibile specificare il numero di come registrato.</span><span class="sxs-lookup"><span data-stu-id="3b878-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b878-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="3b878-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="3b878-130">Il nome del registro di sistema di routing (RIR/IRR) a cui sono registrati il numero e i prefissi come.</span><span class="sxs-lookup"><span data-stu-id="3b878-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="3b878-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b878-131">-Name</span></span>
<span data-ttu-id="3b878-132">Nome della relazione peering da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="3b878-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="3b878-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="3b878-133">-PeerAddressType</span></span>
<span data-ttu-id="3b878-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="3b878-134">PeerAddressType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b878-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="3b878-135">-PeerASN</span></span>
<span data-ttu-id="3b878-136">Numero come del circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3b878-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="3b878-137">Deve essere un ASN pubblico quando PeeringType è AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="3b878-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b878-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="3b878-138">-PeeringType</span></span>
<span data-ttu-id="3b878-139">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="3b878-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b878-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3b878-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="3b878-141">Questo è l'intervallo di indirizzi IP per il percorso di routing principale di questa relazione peering.</span><span class="sxs-lookup"><span data-stu-id="3b878-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="3b878-142">Deve essere una subnet CIDR a/30.</span><span class="sxs-lookup"><span data-stu-id="3b878-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="3b878-143">Il primo indirizzo a numero dispari nella subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="3b878-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="3b878-144">Azure configurerà l'indirizzo pari al successivo nell'interfaccia di Azure router.</span><span class="sxs-lookup"><span data-stu-id="3b878-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="3b878-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3b878-145">-RouteFilter</span></span>
<span data-ttu-id="3b878-146">Si tratta di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="3b878-146">This is an existing RouteFilter object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b878-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="3b878-147">-RouteFilterId</span></span>
<span data-ttu-id="3b878-148">Questo è l'ID risorsa di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="3b878-148">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b878-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3b878-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="3b878-150">Questo è l'intervallo di indirizzi IP per il percorso di routing secondario di questa relazione peering.</span><span class="sxs-lookup"><span data-stu-id="3b878-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="3b878-151">Deve essere una subnet CIDR a/30.</span><span class="sxs-lookup"><span data-stu-id="3b878-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="3b878-152">Il primo indirizzo a numero dispari nella subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="3b878-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="3b878-153">Azure configurerà l'indirizzo pari al successivo nell'interfaccia di Azure router.</span><span class="sxs-lookup"><span data-stu-id="3b878-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="3b878-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="3b878-154">-SharedKey</span></span>
<span data-ttu-id="3b878-155">Si tratta di un hash MD5 facoltativo usato come chiave già condivisa per la configurazione peering.</span><span class="sxs-lookup"><span data-stu-id="3b878-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="3b878-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="3b878-156">-VlanId</span></span>
<span data-ttu-id="3b878-157">Questo è il numero ID della VLAN assegnata per questo peering.</span><span class="sxs-lookup"><span data-stu-id="3b878-157">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b878-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b878-158">CommonParameters</span></span>
<span data-ttu-id="3b878-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b878-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b878-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b878-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b878-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b878-161">INPUTS</span></span>

### <span data-ttu-id="3b878-162">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3b878-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="3b878-163">System. String</span><span class="sxs-lookup"><span data-stu-id="3b878-163">System.String</span></span>

### <span data-ttu-id="3b878-164">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3b878-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="3b878-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b878-165">System.Boolean</span></span>

## <span data-ttu-id="3b878-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b878-166">OUTPUTS</span></span>

### <span data-ttu-id="3b878-167">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3b878-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3b878-168">Note</span><span class="sxs-lookup"><span data-stu-id="3b878-168">NOTES</span></span>

## <span data-ttu-id="3b878-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b878-169">RELATED LINKS</span></span>

[<span data-ttu-id="3b878-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3b878-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="3b878-171">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3b878-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3b878-172">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3b878-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3b878-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3b878-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)