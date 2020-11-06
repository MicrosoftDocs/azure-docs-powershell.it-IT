---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 8471ccd34ab5d13ad5012e9a2e29892659c297f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513699"
---
# <span data-ttu-id="10e8c-101">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="10e8c-101">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="10e8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="10e8c-103">Crea una nuova configurazione di peering da aggiungere a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="10e8c-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10e8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10e8c-104">SYNTAX</span></span>

### <span data-ttu-id="10e8c-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10e8c-105">SetByResource (Default)</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10e8c-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="10e8c-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10e8c-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="10e8c-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10e8c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10e8c-108">DESCRIPTION</span></span>
<span data-ttu-id="10e8c-109">Il cmdlet **New-AzureRmExpressRouteCircuitPeeringConfig** aggiunge una configurazione peering a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="10e8c-109">The **New-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="10e8c-110">Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico.</span><span class="sxs-lookup"><span data-stu-id="10e8c-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="10e8c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10e8c-111">EXAMPLES</span></span>

### <span data-ttu-id="10e8c-112">Esempio 1: creare un nuovo circuito di ExpressRoute con una configurazione peering</span><span class="sxs-lookup"><span data-stu-id="10e8c-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzureRmExpressRouteCircuitPeeringConfig @parameters

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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="10e8c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10e8c-113">PARAMETERS</span></span>

### <span data-ttu-id="10e8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e8c-114">-DefaultProfile</span></span>
<span data-ttu-id="10e8c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10e8c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10e8c-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="10e8c-116">-LegacyMode</span></span>
<span data-ttu-id="10e8c-117">Modalità legacy del peering</span><span class="sxs-lookup"><span data-stu-id="10e8c-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="10e8c-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="10e8c-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="10e8c-119">Per un PeeringType di MicrosoftPeering, è necessario specificare un elenco di tutti i prefissi che si prevede di pubblicizzare durante la sessione BGP.</span><span class="sxs-lookup"><span data-stu-id="10e8c-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="10e8c-120">Vengono accettati solo i prefissi degli indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="10e8c-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="10e8c-121">Se si prevede di inviare un set di prefissi, è possibile inviare un elenco separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="10e8c-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="10e8c-122">Questi prefissi devono essere registrati in un nome del registro di sistema di routing (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="10e8c-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e8c-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="10e8c-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="10e8c-124">Per i prefissi pubblicitari non registrati nel numero di peering, è possibile specificare il numero di come registrato.</span><span class="sxs-lookup"><span data-stu-id="10e8c-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="10e8c-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="10e8c-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="10e8c-126">Il nome del registro di sistema di routing (RIR/IRR) a cui sono registrati il numero e i prefissi come.</span><span class="sxs-lookup"><span data-stu-id="10e8c-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="10e8c-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="10e8c-127">-Name</span></span>
<span data-ttu-id="10e8c-128">Nome della configurazione peer da creare.</span><span class="sxs-lookup"><span data-stu-id="10e8c-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="10e8c-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="10e8c-129">-PeerAddressType</span></span>
<span data-ttu-id="10e8c-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="10e8c-130">PeerAddressType</span></span>

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

### <span data-ttu-id="10e8c-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="10e8c-131">-PeerASN</span></span>
<span data-ttu-id="10e8c-132">Numero come del circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="10e8c-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="10e8c-133">Deve essere un ASN pubblico quando PeeringType è AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="10e8c-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="10e8c-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="10e8c-134">-PeeringType</span></span>
<span data-ttu-id="10e8c-135">I valori accettabili per questo parametro sono: `AzurePrivatePeering` , `AzurePublicPeering` e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="10e8c-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="10e8c-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="10e8c-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="10e8c-137">Questo è l'intervallo di indirizzi IP per il percorso di routing principale di questa relazione peering.</span><span class="sxs-lookup"><span data-stu-id="10e8c-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="10e8c-138">Deve essere una subnet CIDR a/30.</span><span class="sxs-lookup"><span data-stu-id="10e8c-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="10e8c-139">Il primo indirizzo a numero dispari nella subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="10e8c-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="10e8c-140">Azure configurerà l'indirizzo pari al successivo nell'interfaccia di Azure router.</span><span class="sxs-lookup"><span data-stu-id="10e8c-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="10e8c-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="10e8c-141">-RouteFilter</span></span>
<span data-ttu-id="10e8c-142">Si tratta di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="10e8c-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="10e8c-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="10e8c-143">-RouteFilterId</span></span>
<span data-ttu-id="10e8c-144">Questo è l'ID risorsa di un oggetto RouteFilter esistente.</span><span class="sxs-lookup"><span data-stu-id="10e8c-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="10e8c-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="10e8c-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="10e8c-146">Questo è l'intervallo di indirizzi IP per il percorso di routing secondario di questa relazione peering.</span><span class="sxs-lookup"><span data-stu-id="10e8c-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="10e8c-147">Deve essere una subnet CIDR a/30.</span><span class="sxs-lookup"><span data-stu-id="10e8c-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="10e8c-148">Il primo indirizzo a numero dispari nella subnet deve essere assegnato all'interfaccia del router.</span><span class="sxs-lookup"><span data-stu-id="10e8c-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="10e8c-149">Azure configurerà l'indirizzo pari al successivo nell'interfaccia di Azure router.</span><span class="sxs-lookup"><span data-stu-id="10e8c-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="10e8c-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="10e8c-150">-SharedKey</span></span>
<span data-ttu-id="10e8c-151">Si tratta di un hash MD5 facoltativo usato come chiave già condivisa per la configurazione peering.</span><span class="sxs-lookup"><span data-stu-id="10e8c-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="10e8c-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="10e8c-152">-VlanId</span></span>
<span data-ttu-id="10e8c-153">Questo è il numero ID della VLAN assegnata per questo peering.</span><span class="sxs-lookup"><span data-stu-id="10e8c-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="10e8c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e8c-154">CommonParameters</span></span>
<span data-ttu-id="10e8c-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e8c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e8c-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10e8c-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e8c-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10e8c-157">INPUTS</span></span>

### <span data-ttu-id="10e8c-158">System. String</span><span class="sxs-lookup"><span data-stu-id="10e8c-158">System.String</span></span>

### <span data-ttu-id="10e8c-159">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="10e8c-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="10e8c-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10e8c-160">System.Boolean</span></span>

## <span data-ttu-id="10e8c-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10e8c-161">OUTPUTS</span></span>

### <span data-ttu-id="10e8c-162">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="10e8c-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="10e8c-163">Note</span><span class="sxs-lookup"><span data-stu-id="10e8c-163">NOTES</span></span>

## <span data-ttu-id="10e8c-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10e8c-164">RELATED LINKS</span></span>

[<span data-ttu-id="10e8c-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="10e8c-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="10e8c-166">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="10e8c-166">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="10e8c-167">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="10e8c-167">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="10e8c-168">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="10e8c-168">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)