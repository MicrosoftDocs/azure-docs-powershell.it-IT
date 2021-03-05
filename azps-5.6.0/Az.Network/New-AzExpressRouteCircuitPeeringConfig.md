---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 23dc75532c7b23c584d586b486e0d67d32af795f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992584"
---
# <span data-ttu-id="c3750-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c3750-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="c3750-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3750-102">SYNOPSIS</span></span>
<span data-ttu-id="c3750-103">Crea una nuova configurazione di peering da aggiungere a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c3750-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="c3750-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3750-104">SYNTAX</span></span>

### <span data-ttu-id="c3750-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="c3750-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3750-106">MicrosoftConfigingConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="c3750-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3750-107">MicrosoftFilteringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="c3750-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3750-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c3750-108">DESCRIPTION</span></span>
<span data-ttu-id="c3750-109">Il cmdlet **New-AzExpressRouteCircuit DigitaingConfig aggiunge** una configurazione di peering a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c3750-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="c3750-110">I circuiti ExpressRoute connettono la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="c3750-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="c3750-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3750-111">EXAMPLES</span></span>

### <span data-ttu-id="c3750-112">Esempio 1: Creare un nuovo circuito ExpressRoute con una configurazione di peering</span><span class="sxs-lookup"><span data-stu-id="c3750-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```powershell
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzExpressRouteCircuitPeeringConfig @parameters

$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    Peering=$PeerConfig
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="c3750-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3750-113">PARAMETERS</span></span>

### <span data-ttu-id="c3750-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3750-114">-DefaultProfile</span></span>
<span data-ttu-id="c3750-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3750-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3750-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="c3750-116">-LegacyMode</span></span>
<span data-ttu-id="c3750-117">Modalità legacy del peering</span><span class="sxs-lookup"><span data-stu-id="c3750-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="c3750-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="c3750-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="c3750-119">Per un PeeringType di Microsoft È necessario fornire un elenco di tutti i prefissi che si prevede di annunciare tramite la sessione BGP.</span><span class="sxs-lookup"><span data-stu-id="c3750-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="c3750-120">Vengono accettati solo i prefissi di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="c3750-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="c3750-121">È possibile inviare un elenco separato da virgole se si prevede di inviare un set di prefissi.</span><span class="sxs-lookup"><span data-stu-id="c3750-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="c3750-122">Questi prefissi devono essere registrati in un nome registro di routing (RIR/TIR.IRR).</span><span class="sxs-lookup"><span data-stu-id="c3750-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="c3750-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="c3750-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="c3750-124">Se si stanno annunciando prefissi non registrati nel numero AS di peering, è possibile specificare il numero AS con cui vengono registrati.</span><span class="sxs-lookup"><span data-stu-id="c3750-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="c3750-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="c3750-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="c3750-126">Nome del Registro di sistema di routing (RIR/TIR.IRR) in cui vengono registrati il numero AS e i prefissi.</span><span class="sxs-lookup"><span data-stu-id="c3750-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="c3750-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c3750-127">-Name</span></span>
<span data-ttu-id="c3750-128">Nome della configurazione di peering da creare.</span><span class="sxs-lookup"><span data-stu-id="c3750-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="c3750-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c3750-129">-PeerAddressType</span></span>
<span data-ttu-id="c3750-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c3750-130">PeerAddressType</span></span>

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

### <span data-ttu-id="c3750-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="c3750-131">-PeerASN</span></span>
<span data-ttu-id="c3750-132">Il numero AS del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c3750-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="c3750-133">Deve essere un ASN pubblico quando PeeringType è AzurePublicApplicationing.</span><span class="sxs-lookup"><span data-stu-id="c3750-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="c3750-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c3750-134">-PeeringType</span></span>
<span data-ttu-id="c3750-135">I valori accettabili per questo parametro sono: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c3750-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="c3750-136">-PrimaryAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c3750-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="c3750-137">Intervallo di indirizzi IP per il percorso di routing principale di questa relazione di peering.</span><span class="sxs-lookup"><span data-stu-id="c3750-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="c3750-138">Deve essere una subnet CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="c3750-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="c3750-139">Il primo indirizzo con numero dispari in questa subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="c3750-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="c3750-140">Azure configurerà il successivo indirizzo pari all'interfaccia del router di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3750-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="c3750-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c3750-141">-RouteFilter</span></span>
<span data-ttu-id="c3750-142">Si tratta di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="c3750-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="c3750-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="c3750-143">-RouteFilterId</span></span>
<span data-ttu-id="c3750-144">ID della risorsa di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="c3750-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="c3750-145">-SecondaryAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c3750-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="c3750-146">Intervallo di indirizzi IP per il percorso di routing secondario di questa relazione di peering.</span><span class="sxs-lookup"><span data-stu-id="c3750-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="c3750-147">Deve essere una subnet CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="c3750-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="c3750-148">Il primo indirizzo con numero dispari in questa subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="c3750-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="c3750-149">Azure configurerà il successivo indirizzo pari all'interfaccia del router di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3750-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="c3750-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c3750-150">-SharedKey</span></span>
<span data-ttu-id="c3750-151">Questo è un hash MD5 facoltativo usato come chiave pre-condivisa per la configurazione del peering.</span><span class="sxs-lookup"><span data-stu-id="c3750-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="c3750-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="c3750-152">-VlanId</span></span>
<span data-ttu-id="c3750-153">Id della VLAN assegnata al peering.</span><span class="sxs-lookup"><span data-stu-id="c3750-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="c3750-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3750-154">CommonParameters</span></span>
<span data-ttu-id="c3750-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3750-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3750-156">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3750-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3750-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="c3750-157">INPUTS</span></span>

### <span data-ttu-id="c3750-158">System.String</span><span class="sxs-lookup"><span data-stu-id="c3750-158">System.String</span></span>

### <span data-ttu-id="c3750-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c3750-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="c3750-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c3750-160">System.Boolean</span></span>

## <span data-ttu-id="c3750-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3750-161">OUTPUTS</span></span>

### <span data-ttu-id="c3750-162">Microsoft.Azure.Commands.Network.Models.PSCollectioning</span><span class="sxs-lookup"><span data-stu-id="c3750-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="c3750-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="c3750-163">NOTES</span></span>

## <span data-ttu-id="c3750-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3750-164">RELATED LINKS</span></span>

[<span data-ttu-id="c3750-165">Add-AzExpressRouteCircuit DigitaingConfig</span><span class="sxs-lookup"><span data-stu-id="c3750-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c3750-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3750-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="c3750-167">Remove-AzExpressRouteCircuit DigitaingConfig</span><span class="sxs-lookup"><span data-stu-id="c3750-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c3750-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3750-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
