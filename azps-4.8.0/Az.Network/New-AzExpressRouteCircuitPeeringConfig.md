---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 6561faf00104bf0892747ac97c09b5d8fc2c6f2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188485"
---
# <span data-ttu-id="c87f3-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c87f3-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="c87f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c87f3-102">SYNOPSIS</span></span>
<span data-ttu-id="c87f3-103">Crea una nuova configurazione di peering da aggiungere a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c87f3-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="c87f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c87f3-104">SYNTAX</span></span>

### <span data-ttu-id="c87f3-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c87f3-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c87f3-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="c87f3-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c87f3-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="c87f3-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c87f3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c87f3-108">DESCRIPTION</span></span>
<span data-ttu-id="c87f3-109">Il cmdlet **New-AzExpressRouteCircuitPeeringConfig** aggiunge una configurazione peering a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c87f3-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="c87f3-110">Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="c87f3-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="c87f3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c87f3-111">EXAMPLES</span></span>

### <span data-ttu-id="c87f3-112">Esempio 1: creare un nuovo circuito di ExpressRoute con una configurazione peering</span><span class="sxs-lookup"><span data-stu-id="c87f3-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
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

## <span data-ttu-id="c87f3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c87f3-113">PARAMETERS</span></span>

### <span data-ttu-id="c87f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c87f3-114">-DefaultProfile</span></span>
<span data-ttu-id="c87f3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c87f3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c87f3-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="c87f3-116">-LegacyMode</span></span>
<span data-ttu-id="c87f3-117">Modalità legacy del peering</span><span class="sxs-lookup"><span data-stu-id="c87f3-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="c87f3-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="c87f3-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="c87f3-119">Per un PeeringType di MicrosoftPeering, è necessario specificare un elenco di tutti i prefissi che si prevede di pubblicizzare durante la sessione BGP.</span><span class="sxs-lookup"><span data-stu-id="c87f3-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="c87f3-120">Vengono accettati solo i prefissi degli indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="c87f3-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="c87f3-121">Se si prevede di inviare un set di prefissi, è possibile inviare un elenco separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="c87f3-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="c87f3-122">Questi prefissi devono essere registrati in un nome del registro di sistema di routing (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="c87f3-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="c87f3-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="c87f3-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="c87f3-124">Per i prefissi pubblicitari non registrati nel numero di peering, è possibile specificare il numero di come registrato.</span><span class="sxs-lookup"><span data-stu-id="c87f3-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="c87f3-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="c87f3-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="c87f3-126">Il nome del registro di sistema di routing (RIR/IRR) a cui sono registrati il numero e i prefissi come.</span><span class="sxs-lookup"><span data-stu-id="c87f3-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="c87f3-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="c87f3-127">-Name</span></span>
<span data-ttu-id="c87f3-128">Nome della configurazione peer da creare.</span><span class="sxs-lookup"><span data-stu-id="c87f3-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="c87f3-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c87f3-129">-PeerAddressType</span></span>
<span data-ttu-id="c87f3-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c87f3-130">PeerAddressType</span></span>

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

### <span data-ttu-id="c87f3-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="c87f3-131">-PeerASN</span></span>
<span data-ttu-id="c87f3-132">Numero come del circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c87f3-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="c87f3-133">Deve essere un ASN pubblico quando PeeringType è AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="c87f3-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="c87f3-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c87f3-134">-PeeringType</span></span>
<span data-ttu-id="c87f3-135">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c87f3-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="c87f3-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c87f3-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="c87f3-137">Questo è l'intervallo di indirizzi IP per il percorso di routing principale di questa relazione peering.</span><span class="sxs-lookup"><span data-stu-id="c87f3-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="c87f3-138">Deve essere una subnet CIDR a/30.</span><span class="sxs-lookup"><span data-stu-id="c87f3-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="c87f3-139">Il primo indirizzo a numero dispari nella subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="c87f3-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="c87f3-140">Azure configurerà l'indirizzo pari al successivo nell'interfaccia di Azure router.</span><span class="sxs-lookup"><span data-stu-id="c87f3-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="c87f3-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c87f3-141">-RouteFilter</span></span>
<span data-ttu-id="c87f3-142">Si tratta di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="c87f3-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="c87f3-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="c87f3-143">-RouteFilterId</span></span>
<span data-ttu-id="c87f3-144">Questo è l'ID risorsa di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="c87f3-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="c87f3-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c87f3-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="c87f3-146">Questo è l'intervallo di indirizzi IP per il percorso di routing secondario di questa relazione peering.</span><span class="sxs-lookup"><span data-stu-id="c87f3-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="c87f3-147">Deve essere una subnet CIDR a/30.</span><span class="sxs-lookup"><span data-stu-id="c87f3-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="c87f3-148">Il primo indirizzo a numero dispari nella subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="c87f3-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="c87f3-149">Azure configurerà l'indirizzo pari al successivo nell'interfaccia di Azure router.</span><span class="sxs-lookup"><span data-stu-id="c87f3-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="c87f3-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c87f3-150">-SharedKey</span></span>
<span data-ttu-id="c87f3-151">Si tratta di un hash MD5 facoltativo usato come chiave già condivisa per la configurazione peering.</span><span class="sxs-lookup"><span data-stu-id="c87f3-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="c87f3-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="c87f3-152">-VlanId</span></span>
<span data-ttu-id="c87f3-153">Questo è il numero ID della VLAN assegnata per questo peering.</span><span class="sxs-lookup"><span data-stu-id="c87f3-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="c87f3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87f3-154">CommonParameters</span></span>
<span data-ttu-id="c87f3-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c87f3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87f3-156">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c87f3-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87f3-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c87f3-157">INPUTS</span></span>

### <span data-ttu-id="c87f3-158">System. String</span><span class="sxs-lookup"><span data-stu-id="c87f3-158">System.String</span></span>

### <span data-ttu-id="c87f3-159">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c87f3-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="c87f3-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c87f3-160">System.Boolean</span></span>

## <span data-ttu-id="c87f3-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c87f3-161">OUTPUTS</span></span>

### <span data-ttu-id="c87f3-162">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="c87f3-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="c87f3-163">Note</span><span class="sxs-lookup"><span data-stu-id="c87f3-163">NOTES</span></span>

## <span data-ttu-id="c87f3-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c87f3-164">RELATED LINKS</span></span>

[<span data-ttu-id="c87f3-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c87f3-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c87f3-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c87f3-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="c87f3-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c87f3-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c87f3-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c87f3-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
