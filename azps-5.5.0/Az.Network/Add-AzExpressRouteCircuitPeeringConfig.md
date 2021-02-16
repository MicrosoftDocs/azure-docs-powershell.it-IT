---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4d329b0521e5b0f4974c25382be53ff32267e51c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203218"
---
# <span data-ttu-id="4f041-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4f041-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="4f041-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f041-102">SYNOPSIS</span></span>
<span data-ttu-id="4f041-103">Aggiunge una configurazione di peering a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4f041-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="4f041-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f041-104">SYNTAX</span></span>

### <span data-ttu-id="4f041-105">SetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f041-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f041-106">MicrosoftConfigingConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="4f041-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f041-107">MicrosoftFilteringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="4f041-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f041-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4f041-108">DESCRIPTION</span></span>
<span data-ttu-id="4f041-109">Il cmdlet **Add-AzExpressRouteCircuitConfigingConfig** aggiunge una configurazione di peering a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4f041-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="4f041-110">I circuiti ExpressRoute connettono la rete locale al cloud Microsoft usando un provider di connettività invece di Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="4f041-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="4f041-111">Si noti che, dopo aver eseguito **Add-AzExpressRouteCircuitIingConfig,** è necessario chiamare il cmdlet Set-AzExpressRouteCircuit per attivare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="4f041-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="4f041-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f041-112">EXAMPLES</span></span>

### <span data-ttu-id="4f041-113">Esempio 1: Aggiungere un peer a un circuito ExpressRoute esistente</span><span class="sxs-lookup"><span data-stu-id="4f041-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
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

## <span data-ttu-id="4f041-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f041-114">PARAMETERS</span></span>

### <span data-ttu-id="4f041-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f041-115">-DefaultProfile</span></span>
<span data-ttu-id="4f041-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f041-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f041-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4f041-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4f041-118">Il circuito ExpressRoute da modificare.</span><span class="sxs-lookup"><span data-stu-id="4f041-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="4f041-119">Oggetto Azure restituito dal cmdlet **Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="4f041-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="4f041-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="4f041-120">-LegacyMode</span></span>
<span data-ttu-id="4f041-121">Modalità legacy del peering</span><span class="sxs-lookup"><span data-stu-id="4f041-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="4f041-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="4f041-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="4f041-123">Per un PeeringType di MicrosoftIing, è necessario fornire un elenco di tutti i prefissi che si prevede di annunciare tramite la sessione BGP.</span><span class="sxs-lookup"><span data-stu-id="4f041-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="4f041-124">Vengono accettati solo i prefissi di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="4f041-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="4f041-125">È possibile inviare un elenco separato da virgole se si prevede di inviare un set di prefissi.</span><span class="sxs-lookup"><span data-stu-id="4f041-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="4f041-126">Questi prefissi devono essere registrati in un nome registro di routing (RIR/TIR.IRR).</span><span class="sxs-lookup"><span data-stu-id="4f041-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="4f041-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="4f041-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="4f041-128">Se si stanno annunciando prefissi non registrati nel numero AS di peering, è possibile specificare il numero AS con cui vengono registrati.</span><span class="sxs-lookup"><span data-stu-id="4f041-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="4f041-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="4f041-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="4f041-130">Nome del Registro di sistema di routing (RIR/TIR.IRR) in cui vengono registrati il numero AS e i prefissi.</span><span class="sxs-lookup"><span data-stu-id="4f041-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="4f041-131">-Name</span><span class="sxs-lookup"><span data-stu-id="4f041-131">-Name</span></span>
<span data-ttu-id="4f041-132">Nome della relazione di peering da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="4f041-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="4f041-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4f041-133">-PeerAddressType</span></span>
<span data-ttu-id="4f041-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4f041-134">PeerAddressType</span></span>

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

### <span data-ttu-id="4f041-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="4f041-135">-PeerASN</span></span>
<span data-ttu-id="4f041-136">Il numero AS del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4f041-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="4f041-137">Deve essere un ASN pubblico quando PeeringType è AzurePublicApplicationing.</span><span class="sxs-lookup"><span data-stu-id="4f041-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="4f041-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="4f041-138">-PeeringType</span></span>
<span data-ttu-id="4f041-139">I valori accettabili per questo parametro sono: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="4f041-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="4f041-140">-PrimaryAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4f041-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="4f041-141">Intervallo di indirizzi IP per il percorso di routing principale di questa relazione di peering.</span><span class="sxs-lookup"><span data-stu-id="4f041-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="4f041-142">Deve essere una subnet CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="4f041-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="4f041-143">Il primo indirizzo con numero dispari in questa subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="4f041-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="4f041-144">Azure configurerà il successivo indirizzo pari all'interfaccia del router di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f041-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="4f041-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4f041-145">-RouteFilter</span></span>
<span data-ttu-id="4f041-146">Si tratta di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="4f041-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="4f041-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="4f041-147">-RouteFilterId</span></span>
<span data-ttu-id="4f041-148">ID della risorsa di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="4f041-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="4f041-149">-SecondaryAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4f041-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="4f041-150">Intervallo di indirizzi IP per il percorso di routing secondario di questa relazione di peering.</span><span class="sxs-lookup"><span data-stu-id="4f041-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="4f041-151">Deve essere una subnet CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="4f041-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="4f041-152">Il primo indirizzo con numero dispari in questa subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="4f041-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="4f041-153">Azure configurerà il successivo indirizzo pari all'interfaccia del router di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f041-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="4f041-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="4f041-154">-SharedKey</span></span>
<span data-ttu-id="4f041-155">Questo è un hash MD5 facoltativo usato come chiave pre-condivisa per la configurazione del peering.</span><span class="sxs-lookup"><span data-stu-id="4f041-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="4f041-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="4f041-156">-VlanId</span></span>
<span data-ttu-id="4f041-157">Id della VLAN assegnata al peering.</span><span class="sxs-lookup"><span data-stu-id="4f041-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="4f041-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f041-158">CommonParameters</span></span>
<span data-ttu-id="4f041-159">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f041-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f041-160">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f041-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f041-161">INPUT</span><span class="sxs-lookup"><span data-stu-id="4f041-161">INPUTS</span></span>

### <span data-ttu-id="4f041-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4f041-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="4f041-163">System.String</span><span class="sxs-lookup"><span data-stu-id="4f041-163">System.String</span></span>

### <span data-ttu-id="4f041-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4f041-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="4f041-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f041-165">System.Boolean</span></span>

## <span data-ttu-id="4f041-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f041-166">OUTPUTS</span></span>

### <span data-ttu-id="4f041-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4f041-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4f041-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="4f041-168">NOTES</span></span>

## <span data-ttu-id="4f041-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f041-169">RELATED LINKS</span></span>

[<span data-ttu-id="4f041-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4f041-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4f041-171">New-AzExpressRouteCircuit DigitaingConfig</span><span class="sxs-lookup"><span data-stu-id="4f041-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4f041-172">Remove-AzExpressRouteCircuit DigitaingConfig</span><span class="sxs-lookup"><span data-stu-id="4f041-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4f041-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4f041-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
